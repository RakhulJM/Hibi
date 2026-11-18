# Hibi — Agile Working Agreement

Hibi is developed as a small, evolving product. We use Scrum-inspired iterations while keeping the process lightweight for a solo developer.

## Product goal

Create a private, customizable journaling space that protects personal writing, works offline, and can synchronize encrypted data across devices when the user enables a correctly configured cloud backend.

## Working cadence

- Iteration length: one week.
- Planning: select a small set of backlog items that support one iteration goal.
- Daily check: briefly inspect progress, blockers, and the next useful task.
- Review: demonstrate working increments and check acceptance criteria.
- Retrospective: record one practice to keep and one improvement for the next iteration.
- Refinement: split oversized stories and clarify acceptance criteria before selecting them.

## Product backlog

| Priority | Epic | Example user story | Acceptance criteria |
|---|---|---|---|
| P0 | Vault | As the owner, I want to unlock my diary with a private passphrase. | Correct passphrase unlocks; incorrect passphrase is rejected; key material is not stored in plaintext. |
| P0 | Journal | As the owner, I want to create, edit, search, and delete entries. | Entries persist locally and display their date and update time. |
| P0 | Backup | As the owner, I want an encrypted backup I can restore. | Export contains ciphertext; wrong passphrase cannot restore; invalid backup is rejected. |
| P1 | Themes | As the owner, I want to switch visual themes. | Theme selection persists without changing journal content. |
| P1 | PWA | As the owner, I want to install Hibi on my devices. | Manifest, icons, service worker, and offline app shell pass browser checks. |
| P1 | Sync | As the owner, I want encrypted cross-device synchronization. | Server receives ciphertext only; RLS isolates users; conflicts are detected. |
| P2 | Memories | As the owner, I want to collect photos and captions. | Media storage and backup behavior are explicit and tested. |
| P2 | Mood and calendar | As the owner, I want to review moods and entries over time. | Views are derived from saved records and can be filtered by date. |
| P2 | Customization | As the owner, I want to personalize layout and typography. | Preferences persist independently of journal records. |

## Definition of Ready

A backlog item is ready when:
- The user value is clear.
- Acceptance criteria are testable.
- Dependencies and privacy implications are identified.
- The item is small enough to finish in one iteration.

## Definition of Done

A backlog item is done when:
- The implementation meets the acceptance criteria.
- Relevant tests pass.
- Errors and empty states are handled.
- Accessibility and responsive behavior are checked where applicable.
- Documentation is updated.
- No private diary data, keys, or secrets are committed.

## Release principle

Security-sensitive work is not considered done because the UI appears to work. Encryption, recovery, offline behavior, synchronization, and access controls require tests and explicit review before release.
