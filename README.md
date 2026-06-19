# MeshCore Homebrew Tap

Homebrew formulae for MeshCore tools.

## Usage

```sh
brew tap meshcore-cz/tap
brew install mc              # meshcore-go terminal client
brew install hopbackd        # Hopback web backend
brew install hopback-agent   # Hopback radio bridge
```

Or in one step without tapping first:

```sh
brew install meshcore-cz/tap/mc
```

Upgrade with `brew upgrade mc` (etc.).

## Supported platforms

Bottled as prebuilt binaries for macOS (Apple Silicon and Intel) and Linux
(`arm64` and `amd64`).

## How it works

Each formula installs the prebuilt binary from its project's GitHub Release:

| Formula          | Source repo                  | Command         |
| ---------------- | ---------------------------- | --------------- |
| `mc`             | `meshcore-cz/meshcore-go`    | `mc`            |
| `hopbackd`       | `meshcore-cz/hopback`        | `hopbackd`      |
| `hopback-agent`  | `meshcore-cz/hopback`        | `hopback-agent` |

The formulae are generated and updated automatically by each project's release
workflow via [`scripts/render-formula.sh`](scripts/render-formula.sh) — do not
edit `Formula/*.rb` by hand.
