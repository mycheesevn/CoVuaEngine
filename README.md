# CovuaEngine — Stockfish Corresponding Source

## Purpose

This folder is the corresponding-source mirror for the Stockfish engine
binary served by the Chess game at chess.synerworlds.com, provided in
compliance with the GNU General Public License v3 (GPLv3).

## Play it live

This engine powers the computer opponent in **Chess at SynerWorlds** —
play against it free in your browser, no downloads:

- **Chess:** https://chess.synerworlds.com
- **All SynerWorlds games:** https://synerworlds.com

## Provenance

- Engine: Stockfish 19, via nmrugg/stockfish.js version 19.0.1 — the npm
  package `stockfish`.
- Upstream repositories:
  - https://github.com/nmrugg/stockfish.js
  - https://github.com/official-stockfish/Stockfish
- Shipped flavor: "lite-single" — single-threaded, with the embedded lite
  NNUE network `nn-61e7af4bb97d` by Chris Bao, CC0 per the file header in
  the shipped JS.
- Shipped files, in `package/bin/`:
  - `stockfish-19-lite-single.js` (28,230 bytes)
  - `stockfish-19-lite-single.wasm` (1,845,971 bytes)

## Unmodified files

The shipped files are used unmodified. Their SHA-256 checksums are listed
in `SHA256SUMS.txt` and can be verified against the files in `package/bin/`.

The `package/` directory contains the corresponding source as distributed
in the npm package: `Copying.txt`, `README.md`, `package.json`, `index.js`,
`scripts/cli.js`, `scripts/findEngine.js`, and the shipped lite-single
loader in `bin/`. No other engine flavors are included, because they are
not shipped by the game.

One exception: the compiled `stockfish-19-lite-single.wasm` binary itself
is not stored in this git repository (our publishing tooling moves text
only). The unmodified binary is served by the game at
https://chess.synerworlds.com/stockfish/stockfish-19-lite-single.wasm and
is also included in the npm package `stockfish@19.0.1`; its SHA-256 in
`SHA256SUMS.txt` lets anyone verify the served file byte-for-byte.

## License

- Engine: GPLv3. The full license text is in `package/Copying.txt`.
- Embedded NNUE network: CC0.

## Note

Prepared 2026-10-26 and published to
https://github.com/mycheesevn/CoVuaEngine, mirroring the CotuongEngine
pattern used for Pikafish.
