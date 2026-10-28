<div align="center">

<img src="snap/gui/concat.png" alt="Concat logo" width="128" />

# Concat

**A native video editor with local AI tools.**

[![concat](https://snapcraft.io/concat/badge.svg)](https://snapcraft.io/concat)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64 and arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Concat](https://github.com/jub0t/Concat), a desktop application for editing videos, adding captions and creating voiceovers.

</div>

---

## Getting Started

<a href="https://snapcraft.io/concat"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install concat
concat
```

Launch from the terminal or your application menu.

## Configure

Manage preferences and AI models in the app. There are no `snap set` options.

| Optional access | Command |
| --- | --- |
| Microphone for voiceovers | `sudo snap connect concat:audio-record` |
| Media and projects on removable storage | `sudo snap connect concat:removable-media` |

Models download when needed and remain under `~/snap/concat/common/.local/share/` between updates.

## Limitations

- Existing settings and models from a native installation are not imported automatically.
- Use the file picker for locations outside the snap's permitted folders.
- Application updates are managed by snapd.

## Build

```bash
git clone https://github.com/sidalit/concat-snap.git
cd concat-snap
sudo snap install snapcraft --classic
snapcraft pack
```

Desktop compilation can exceed 12 GiB of RAM.

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/concat-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/jub0t/Concat/issues).

## License

Snap packaging: [MIT](https://github.com/sidalit/concat-snap/blob/main/LICENSE).
