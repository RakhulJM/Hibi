# Hibi Release Checklist

## Source and build
- [ ] Full source tree is committed.
- [ ] Lockfile is committed.
- [ ] TypeScript checks pass.
- [ ] Unit and integration tests pass.
- [ ] Production build succeeds.
- [ ] GitHub Actions checks pass.

## Privacy and security
- [ ] No diary content, photos, secrets, credentials, or backups are tracked by Git.
- [ ] Vault encryption and wrong-passphrase behavior are tested.
- [ ] Backup export and restore are tested, including tampering and wrong passphrase.
- [ ] Plaintext journal content is never sent to Supabase.
- [ ] RLS is enabled and tested with at least two accounts.
- [ ] Recovery and key-loss consequences are documented.

## User experience
- [ ] Journal create, edit, delete, and search work.
- [ ] Theme and customization preferences persist.
- [ ] Mobile and desktop layouts are checked.
- [ ] Empty, loading, and error states are understandable.
- [ ] Keyboard navigation and accessible labels are checked.

## PWA and sync
- [ ] Manifest and icon assets are valid.
- [ ] Service worker installs and updates safely.
- [ ] Offline behavior is tested in a real browser.
- [ ] Cross-device sync and conflict handling are tested.
