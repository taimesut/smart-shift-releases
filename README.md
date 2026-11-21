# Smart Shift Desktop — Windows Releases

Public distribution channel for signed Windows desktop installers built from private `taimesut/smart-shift-desktop`.

## Demo/Beta and Stable

| Channel | GitHub release type | Tag example |
|---|---|---|
| Demo / Beta | **Prerelease** | `v0.3.0-beta.1` |
| Stable | **Normal release** | `v0.3.0` |

Open the [Releases page](https://github.com/taimesut/smart-shift-releases/releases) to download an installer.

Every signed release should include these **assets**:

- `SmartShift-Setup-X.Y.Z[-beta.N].exe` — Windows installer.
- `manifest.json` — signed metadata including channel, version, SHA-256 and byte count.
- `manifest.sig` — detached Ed25519 signature for the manifest.

## In-app update behavior

Choose **Demo / Beta** to see newer Beta and Stable releases, or **Ổn định / Stable** to see only newer Stable releases. The application checks at startup and via **Kiểm tra cập nhật**. When a newer signed release is available it offers **Cập nhật ngay** / **Để sau**.

**Important:** Legacy 0.2.0 and unsigned GitHub Actions trial installers cannot self-update because they do not contain the public verification key. Testers must manually install the **first signed Beta** once; all following updates can use in-app update.

Source code, private signing keys, API keys and SOC employee data must **not** be uploaded to this public repository.

**Current status:** No release is published until the maintainer configures `UPDATE_SIGNING_KEY_B64` and `PUBLISH_TOKEN` secrets in the **private** source repository and pushes a matching signed version tag. Do not download unofficial binaries.
