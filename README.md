# OnvifRtspDesktop Updates

Public update repository for OnvifRtspDesktop.

## Release channels

- **Stable**: production releases
- **Beta/Test**: pre-releases for testing

## Installer filename

The Windows x64 installer must use exactly:

`OnvifRtspDesktop-Setup-x64.exe`

## GitHub Releases

The application updater should use GitHub Releases as the source for update packages.

Recommended tags:
- Stable: `v1.0.0`, `v1.0.1`, ...
- Beta: `v1.1.0-beta.1`, `v1.1.0-beta.2`, ...

For a beta/test release, mark the GitHub Release as **Pre-release**.

Do not commit installer binaries directly to the repository when a GitHub Release asset can be used instead.
