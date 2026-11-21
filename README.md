# Smart Shift Desktop — Official Downloads

This public repository is the **distribution-only** channel for the Windows application. The source code and build configuration stay in the private repository **taimesut/smart-shift-desktop**.

## Installation

When the first stable release is published, download **SmartShift-Setup-X.Y.Z.exe** from the Releases section. Do not download installers from third-party mirrors.

## Updates

Smart Shift checks the latest stable release when starting. For users running a signed production build, the app will show **Cập nhật ngay / Để sau** when a newer version is available. Clicking to update downloads the installer and verifies its hash against a signed manifest before installing.

Each release must contain:

- SmartShift-Setup-X.Y.Z.exe — Windows x64 installer.
- manifest.json — version, size and SHA-256 digest.
- manifest.sig — Ed25519 signature of the exact manifest bytes.

The public repository should never contain Python source code, API keys, signing private keys or internal SOC data.

**Current status:** The Python desktop pilot is being tested. A signed Windows installer will appear here only after validation and maintainer configuration of release secrets. The initial pilot is not yet equivalent to the SOC Web production roster solver.
