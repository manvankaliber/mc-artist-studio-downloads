# MC Artist Studio downloads

This public repository hosts Windows and Linux builds published from the private MC Artist Studio source repository.

- Official releases are stable GitHub Releases and update the stable Tauri feed at `latest.json`.
- Beta releases are prereleases. Their current installer details and signed updater manifest live in `channels/beta/release.json` and `channels/beta/latest.json`.
- Canary builds update a rolling Windows-only prerelease after pushes to `main`. Its installer details and signed updater manifest live in `channels/canary/release.json` and `channels/canary/latest.json`.
- Nightly releases are Windows-only prereleases. Their current installer details and signed updater manifest live in `channels/nightly/release.json` and `channels/nightly/latest.json`.

The editor repository manually dispatches official and beta builds, publishes a rolling canary after relevant pushes to `main` (or a manual dispatch), and runs a nightly build once daily. This repository publishes each payload branch, updates the preview feed pointers, and calls the Vercel deploy hook after official releases so the website archive refreshes.
