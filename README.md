# GridCraft web (GitHub Pages)

This repository hosts the official [GridCraft](https://github.com/storytold/gridcraft) web (WebAssembly) build from the ArtCraft team and the GridCraft contributors, so we can open it in a browser from GitHub Pages.

**Live site:** https://antojitos-ahumados.github.io/gridcraft-web/

**Pinned version:** 0.18.0 (`v0.18.0` from [storytold/gridcraft](https://github.com/storytold/gridcraft/releases/tag/v0.18.0)).

GridCraft is alpha software. It needs a modern browser with WebGPU or WebGL2. Files you open stay in your browser; this site does not upload workbooks.

## License and credit

GridCraft is dual-licensed under [MIT](LICENSE-MIT) or [Apache-2.0](LICENSE-APACHE), at your option. Copyright (c) 2026 ArtCraft Team and the GridCraft contributors. Required notices are in [NOTICE](NOTICE). Bundled third-party material is listed in [ATTRIBUTION.md](ATTRIBUTION.md).

This repository redistributes the unmodified official `gridcraft-web-*.zip` release. It does not include the ArtCraft wordmark or logos, which are trademarks of the ArtCraft Team.

Upstream project: [github.com/storytold/gridcraft](https://github.com/storytold/gridcraft) · [getartcraft.com/apps/gridcraft](https://getartcraft.com/apps/gridcraft)

## How to bump the version

1. In [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml), change `GRIDCRAFT_VERSION` at the top to the new release version, without a leading `v` (for example `0.19.0`).
2. Commit and push to `main`, or open the Actions tab and choose **Run workflow**.
3. The workflow downloads `gridcraft-web-<version>.zip` from the official release, checks its SHA-256 against that release's `SHA256SUMS.txt`, unpacks it, and deploys it to Pages.

## WordCraft

WordCraft is not hosted here yet. The workflow is set up so a later change can pin `WORDCRAFT_VERSION` and unpack `wordcraft-web-*.zip` into the `/wordcraft/` path on this same Pages site, leaving GridCraft at the site root.
