# Gyakuten Saiban 2 English GBA

English localization project for **Gyakuten Saiban 2 (逆転裁判2)** on Game Boy Advance.

## Build strategy

The project keeps the original Japanese ROM out of the repository. The build workflow obtains the public disassembly source, applies local patches from `patches/`, builds the ROM, and verifies the resulting binary.

The upstream disassembly documents the matching Japanese ROM as SHA-1:

`F7A156DBED52D3EDB8104112AE40E6E2AACA57F9`

The localization work will target the script/font/UI layers while preserving the game's existing engine and asset structure.

## Repository layout

- `patches/` — localization changes applied to the upstream source during CI
- `.github/workflows/build.yml` — reproducible build workflow
- `docs/` — notes and translation/build documentation

## Important

Do not commit a copyrighted Japanese ROM dump to this repository. A legally obtained ROM is used locally as the build/reference input where needed.

## Build

GitHub Actions builds the project automatically. The resulting ROM is published as a workflow artifact for project testing.
