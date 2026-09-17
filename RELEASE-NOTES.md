# Dovra Beta — beta-20260916

Free experimental Windows x64 portable build with an English interface. This is a Beta, not a stable release or a formal Dovra product version. The underlying Chromium technical version is `153.0.8010.48`.

## Downloads

- `Dovra-Beta-20260916-win-x64.zip`: complete browser, launcher and offline notices.
- `Dovra-Toolkit-beta-20260916.zip`: optional companion toolkit; no browser included.
- `SHA256SUMS.txt`: SHA-256 checksums for the release assets.
- Component source and relinking archives: listed in [SOURCE-MATERIALS.md](SOURCE-MATERIALS.md).

GitHub's automatic repository source ZIP/tarball contains repository files, not the compiled browser or the full Chromium source tree.

## Verified scope

Tested environment: Windows Server 2022 x64, OS build 20348.5139; NVIDIA GeForce GTX 650 / ANGLE Direct3D 11.

Accepted tests: English built-in pages and the engine version were checked; the version, Settings, credits and GPU pages were visually reviewed. Targeted checks covered eight credits entries with complete licence text and expanded display, Canvas output, a WebGL 2 draw/readback, short local PCM and FLAC playback, and test localStorage retained after a graceful close and reopen. These were browser checks, not a test of the packaged launcher's first-use terms dialog or a clean-machine installation.

The tested CDP endpoint listened only on 127.0.0.1, rejected the tested foreign Host requests and foreign/null WebSocket Origin handshakes, and permitted the trusted local client. A foreign-Origin HTTP request returned 200 without an Access-Control-Allow-Origin response header; it was not rejected at the HTTP layer. Local programs can still control the browser through CDP. This is not authentication or protection from local malware.

The reviewed idle NetLog fields recorded WPAD activity and no external destination host. This finite observation is not a zero-network or zero-telemetry guarantee. WebGL success does not verify all WebGPU, DXIL, GPU, codec or sandbox paths. Nonfatal SharedImageManager::ProduceSkia mailbox messages were observed; the sampled drawing and playback checks completed..

Signing status: `Start-Dovra.exe`, `bin/chrome.exe` and `bin/chrome.dll` are unsigned (NotSigned). A checksum identifies bytes; it is not a trusted publisher signature..

The test scope is finite. Windows 10/11 client systems, a standard-user installation, every GPU, every media format and every website are not claimed to have been tested. Site compatibility, preserved login state and uninterrupted operation are not guaranteed.

## Use and limitations

Use this build for lawful workflows and authorized testing. Keep backups and a separate browser for important browsing. Configurable browser parameters do not grant access or guarantee anonymity.

The build does not provide a Dovra automatic updater. Google Safe Browsing is disabled in this candidate; do not rely on it for remote phishing or malware checks. The privacy notice explains the reviewed background-service settings and their limits. No universal zero-network or zero-telemetry guarantee is made.

Read the offline terms when starting the package. Project terms do not replace component licences or remove applicable open-source modification and relinking rights. The companion toolkit has a separate MIT licensing scope.

Project: https://dovra.dev/ · Support: dovra.dev@gmail.com
