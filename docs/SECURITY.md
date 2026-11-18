# Hibi Security and Privacy Notes

## Privacy objective

Hibi is intended to keep personal diary content private. The repository may be public; user entries, photos, exports, vault passphrases, encryption keys, and credentials must never be committed.

## Intended design

- Journal content is encrypted in the browser before persistent storage.
- Local persistence uses browser storage.
- An optional cloud service stores ciphertext rather than plaintext diary text.
- Cloud access is scoped to the authenticated owner using database row-level security.
- Backups are encrypted and require the vault passphrase to restore.
- The vault passphrase and derived keys are not uploaded as recoverable plaintext.

## Important boundaries

- Authentication is not encryption. A database policy alone does not prevent a service operator or database leak from exposing plaintext.
- End-to-end encryption depends on correct key derivation, nonce handling, authenticated encryption, recovery design, and all application paths avoiding plaintext upload.
- Browser extensions, malware, compromised devices, screenshots, and a person with access to an unlocked device are outside the protection offered by a client-side vault.
- Losing the only passphrase or recovery material may make data permanently unrecoverable.
- IndexedDB is not a guaranteed backup. Browser storage can be cleared or evicted; export and restore must be tested.
- Local browser data can be read by scripts running in the same origin. Keep dependencies updated and use a restrictive Content Security Policy.

## Release requirements

Before relying on Hibi for real private records:
1. Review the cryptographic design and implementation.
2. Test wrong-passphrase, tampered-record, nonce, and backup cases.
3. Test account isolation using two separate Supabase users.
4. Verify that Supabase receives ciphertext only.
5. Run security and database advisors.
6. Test synchronization conflict handling and recovery on a second device.
7. Review dependencies, CSP, service-worker caching, and deployment configuration.

This document describes intended safeguards. It is not a security audit or a claim that the application has been independently certified.
