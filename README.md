# homeos-plugin-homebrew-cask

![License](https://img.shields.io/badge/license-MIT%20OR%20Apache--2.0-blue)

A [homeos](https://github.com/hainet50b/homeos) plugin for [Homebrew Cask](https://docs.brew.sh/Homebrew-Cask), which installs macOS GUI applications and binary distributions via `brew install --cask`. Pair with the [homebrew plugin](https://github.com/hainet50b/homeos-plugin-homebrew) when a package is a Formula instead of a Cask.

## Usage

Add the plugin to your homeos repository:

```sh
homeos plugin add homebrew-cask
```

Create a package using this plugin:

```sh
homeos package add firefox --plugin homebrew-cask --param name=firefox
```

## Parameters

| Parameter | Description |
|-----------|-------------|
| `name` | Homebrew Cask name (e.g., `firefox`) |

## Actions

| Action | Command |
|--------|---------|
| install | `brew install --cask {{name}}` |
| update | `brew upgrade --cask {{name}}` |
| uninstall | `brew uninstall --cask {{name}}` |

> [!NOTE]
> Homebrew Cask is macOS only. Templates are provided as `.sh` files for use under macOS's default shell. Linuxbrew does not officially support Cask.

## License

Licensed under either of

 * Apache License, Version 2.0
   ([LICENSE-APACHE](LICENSE-APACHE) or <http://www.apache.org/licenses/LICENSE-2.0>)
 * MIT license
   ([LICENSE-MIT](LICENSE-MIT) or <http://opensource.org/licenses/MIT>)

at your option.

## Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.
