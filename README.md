# GridCraft web (GitHub Pages)

This repository hosts the official [GridCraft](https://github.com/storytold/gridcraft) web (WebAssembly) build from the ArtCraft team and the GridCraft contributors, so we can open it in a browser from GitHub Pages.

**Live site:** https://antojitos-ahumados.github.io/gridcraft-web/

**Pinned version:** 0.18.0 (`v0.18.0` from [storytold/gridcraft](https://github.com/storytold/gridcraft/releases/tag/v0.18.0)).

The published site is the unmodified official `gridcraft-web-0.18.0.zip`, served from the `gh-pages` branch. GridCraft is alpha software. It needs a modern browser with WebGPU or WebGL2. Files you open stay in your browser; this site does not upload workbooks.

## License and credit

GridCraft is dual-licensed under [MIT](LICENSE-MIT) or [Apache-2.0](LICENSE-APACHE), at your option. Copyright (c) 2026 ArtCraft Team and the GridCraft contributors. Required notices are in [NOTICE](NOTICE). Bundled third-party material is listed in [ATTRIBUTION.md](ATTRIBUTION.md).

This repository does not include the ArtCraft wordmark or logos, which are trademarks of the ArtCraft Team.

Upstream project: [github.com/storytold/gridcraft](https://github.com/storytold/gridcraft) · [getartcraft.com/apps/gridcraft](https://getartcraft.com/apps/gridcraft)

## How to bump the version

From a clone of this repository, publish a newer official web zip to the `gh-pages` branch:

```sh
./scripts/publish-gh-pages.sh 0.19.0
```

The script downloads `gridcraft-web-<version>.zip` from the official `storytold/gridcraft` release, checks its SHA-256 against that release's `SHA256SUMS.txt`, and replaces the `gh-pages` branch.

An equivalent GitHub Actions workflow is in [`scripts/deploy-pages.yml`](scripts/deploy-pages.yml). Once that file is moved to `.github/workflows/deploy-pages.yml` and Pages is set to build from GitHub Actions, bumping is a one-line change to `GRIDCRAFT_VERSION` in the workflow, then a push or a manual **Run workflow**.

## WordCraft

WordCraft is not hosted here yet. Either publish path can later unpack `wordcraft-web-*.zip` into the `/wordcraft/` path on this same Pages site, leaving GridCraft at the site root.
