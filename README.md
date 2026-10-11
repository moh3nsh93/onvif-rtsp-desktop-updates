# ONVIF RTSP Desktop

ONVIF RTSP Desktop turns a Windows PC into an ONVIF-discoverable RTSP video source. Use it to send the desktop capture to a compatible NVR or RTSP client on your local network.

This repository is the public update and release channel for the application.

## Download

Download the latest stable Windows x64 installer from [GitHub Releases](https://github.com/moh3nsh93/onvif-rtsp-desktop-updates/releases).

The installer asset must be named exactly:

`OnvifRtspDesktop-Setup-x64.exe`

The in-app updater uses this asset name and verifies the downloaded installer against the SHA-256 digest reported by GitHub Releases. Installer binaries are distributed as release assets, not committed to this repository.

## Features

- Captures the Windows desktop and provides configurable H.264 main and sub streams over RTSP.
- Exposes ONVIF Device and Media services and WS-Discovery for compatible NVRs.
- Configures stream resolution, frame rate, bitrate, and RTSP TCP/UDP transport.
- Supports ONVIF/RTSP access credentials and optional Windows output-audio streaming.
- Displays the local network address and copyable stream URLs, with diagnostics for encoding and listening ports.
- Provides system-tray controls and an optional start-after-sign-in setting.
- Retrieves optional software announcements from the product website. The announcement cache refreshes every 24 hours; announcement-service failures do not stop streaming.
- Checks for stable application updates from GitHub Releases.

Available resolution, frame rate, and stream quality depend on the capture hardware, encoder, network, and receiving device.

## Installation and first run

1. Download `OnvifRtspDesktop-Setup-x64.exe` from the latest stable release's **Assets** section.
2. Run the installer. Approve the Windows Firewall configuration when prompted so ONVIF discovery and RTSP connections can reach the PC.
3. Launch ONVIF RTSP Desktop and activate a valid license in **Settings → About & License** while connected to the internet.
4. Configure streams and credentials in **Settings → Network & access**, then start streaming.
5. Add the displayed RTSP URL to your NVR/client, or discover the source through ONVIF.

The x64 installer is self-contained; a separate .NET installation is not required. Settings and license data are stored for the current Windows user.

## Licensing and offline use

A valid license must be activated before streaming. Activation and signed, device-bound entitlements are provided by the product's license service. After online activation, the application can continue to verify its entitlement locally for up to seven days without internet access. Online renewal checks are made when needed and no more often than once every 24 hours.

To move a license to another computer, deactivate the current device while it can reach the license service. The number of activations is subject to the license plan.

## Network and troubleshooting

- Allow the installer to add the required Windows Firewall rules. If you choose custom ports, create corresponding inbound rules yourself.
- Ensure the NVR and computer can communicate over the LAN; guest Wi-Fi or VLAN isolation can prevent discovery and streaming.
- If ONVIF discovery fails, check firewall rules and network isolation, then try adding the displayed RTSP URL directly.
- If video does not start, verify the selected encoder and stream settings, credentials, and that the selected ports are not already in use.
- Performance and compatibility vary by NVR model, Windows capture source, encoder, and available network bandwidth.

## Security

Release builds obfuscate managed application metadata and strings to raise the effort required for reverse engineering. Obfuscation cannot make a client-side application impossible to inspect or modify. License decisions are backed by the online service and signed entitlements; the signing private key is not included in the application.

Download installers only from this repository's Releases. Keep your license key private.

## Release channels

- **Stable:** production releases, for example `v1.1.0`.
- **Beta/Test:** pre-releases for testing, for example `v1.1.0-beta.1`. Beta releases are marked **Pre-release** on GitHub and may be less reliable than stable versions.

## Third-party notices

The application bundles FFmpeg with GPL-enabled components, including libx264. See `THIRD-PARTY-NOTICES.txt` installed with the application for applicable notices and source information. Review and comply with the relevant license terms before redistributing the software.

## Support

For product information and support, visit [CCTV Negahe Bartar](https://cctvnegahebartar.com).
