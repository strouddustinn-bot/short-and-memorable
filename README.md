# short-and-memorable
Desktop app to help sex workers manage bookings, payments, and safety
About
SafeShift is a desktop-first app designed to help sex workers make and keep money while reducing time-wasting contacts and improving personal safety. It focuses on appointment management, message screening, deposits/no-show policies, simple bookkeeping, and privacy-first data storage. The project is intended as a harm-reduction, safety, and business-management tool — not to facilitate illegal activity. Users should follow local laws and best practices.

Key features
Private, local-first data storage (SQLite / local encrypted storage) with optional encrypted cloud sync.
Message screening: customizable filters, keyword blocking, and templated auto-responses to reduce low-quality inquiries.
Booking system: create appointment slots, require deposits, confirm/cancel flows, automated reminders.
Payments: integration-friendly hooks (Stripe/PayPal/other processors) for deposits and payouts (implementors must use legal, compliant processors).
No-show / cancellation policies: automated fees and balance adjustments.
Simple income & expense tracking with export (CSV) for accounting.
Safety tools: check-in timers, emergency contact quick-dial (link to phone), session logs for personal safety records.
Profile privacy helpers: anonymized public text, selective image handling, metadata scrubbing.
Offline-first desktop experience (works without internet for core features).
Role-based access: single-user or manager modes (for people who have support staff).
Extensible plugin/hooks for additional integrations (calendars, messaging clients, verification services).
Why a desktop app?
Keeps sensitive data primarily on the user’s device, reducing reliance on third-party servers.
Better control over backups/encryption and offline usage.
Easier integration with local payment hardware or native OS features.
Security & privacy
Encrypt local database at rest (AES-256 or equivalent). Encrypt backups and any cloud-sync data end-to-end if you add syncing.
Minimize stored PII; provide clear settings for what to keep locally vs. discard.
Do not store payment card numbers directly — integrate with PCI-compliant processors.
Provide an option to securely erase logs or data wipe for quick cleanup.
Include clear privacy policy and guidance for users about what the app does and does not store.
Legal & ethical notice
This software is a tool for business management and harm reduction. It must not be used to facilitate illegal activities.
Implementors and users must comply with local laws and the terms of service of any payment or communication providers used.
Include local resources and hotlines in-app for users who need legal, medical, or safety assistance.
Getting started (developer / contributor)
Clone the repo git clone https://github.com/<owner>/<repo>.git
Recommended stack (examples — pick one):
Electron + React/Preact + SQLite (local-first, cross-platform)
Tauri + Svelte + SQLite (smaller binary, Rust-backed)
.NET MAUI or WPF (Windows-native) for Windows-first builds
Install dependencies and run in dev:
npm install
npm run dev
Build desktop releases:
npm run build
electron-builder / tauri build (depending on stack)
Testing: unit tests for core business logic (bookings, deposits, message filters) and integration tests for payment flows (mock processors).
User installation (end users)
Download the installer for your OS from Releases.
Run installer and follow setup.
On first run, choose a local master password (used to encrypt local data).
Optionally enable encrypted cloud sync and set up your payment processor account.
Configuration & usage
Create your profile (use anonymized display name if desired).
Set your availability calendar and appointment durations.
Configure message filters and auto-responders to screen low-quality requests.
Set deposit and cancellation/no-show policies (deposit amounts, refund rules, grace times).
Link to a payment processor for collecting deposits.
Use the income dashboard to track earnings and run CSV exports for taxes.
Accessibility & UX notes
Prioritize simple flows for fast booking and quick emergency actions.
Large-font mode, high-contrast theme, and keyboard accessibility recommended.
Offline-first UI so core features work without connectivity.
Roadmap (short-term ideas)
Mobile companion app or responsive web client for quick checks.
Encrypted cloud sync (end-to-end) with per-device keys.
Integrations: calendar (Google/Apple), messaging gateways, identity/verification providers (opt-in).
Template marketplace for response templates and policies.
Localization and translations.
Contributing
Open to contributors. Please open issues for feature requests or bugs.
Follow code style and add tests for critical flows (payments, bookings, data encryption).
Include a Code of Conduct and Contribution Guide in the repo.
Acknowledgments & resources
Provide links to local sex-worker safety and legal support organizations.
Link to harm-reduction best-practices resources and privacy guides.
License
Choose an appropriate license (e.g., MIT, Apache 2.0). If you want to prioritize privacy and community control, consider a license that fits your goals.
Template files to include in repo
README.md (this file)
CONTRIBUTING.md
CODE_OF_CONDUCT.md
PRIVACY_POLICY.md
SECURITY.md (how to report security issues)
sample-config.json (with safe defaults)
migrations/ and docs/
