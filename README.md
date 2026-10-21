# telly brand

The telly wordmark and everything drawn from it: app icons, TV banners and splash screens for every
telly app. One source, so the logo is the same everywhere.

| File | What it is |
|---|---|
| `telly-wordmark.svg` | The wordmark: "telly" in [Roboto](https://github.com/googlefonts/roboto) Black (v2.138), letter spacing −0.02em, as outlines |
| `make-wordmark.swift` | Makes `telly-wordmark.svg` from Roboto Black (`Roboto-LICENSE.txt`, Apache 2.0) |
| `make-assets.swift` | Draws every icon, banner and splash into the app repos |

## Drawing the assets

Check out the app repos next to this one, then run from the folder that holds them:

```bash
swift telly-brand/make-assets.swift
```

| App | What it draws |
|---|---|
| [telly-android](https://github.com/tellyteam/telly-android) | Launcher icons, Fire TV and Android TV banners, the splash wordmark |
| [telly-apple](https://github.com/tellyteam/telly-apple) | The iPad icon and every size of the Mac icon |
| [telly-lg](https://github.com/tellyteam/telly-lg) | The LG TV icons and splash |

The apps also draw the wordmark itself as a vector, copied from `telly-wordmark.svg`: an Android
vector drawable (`telly_wordmark.xml`), the iPad and Mac asset catalog's `Wordmark` image, and the
LG app's `Wordmark.svelte`.

To change the wordmark, change `make-wordmark.swift` and run it with Roboto Black:

```bash
swift make-wordmark.swift path/to/Roboto-Black.ttf telly-wordmark.svg
```

## Licence

The scripts and artwork are free software under the [GNU General Public License v3.0](LICENSE).
Roboto is licensed under the Apache License 2.0 (`Roboto-LICENSE.txt`).
