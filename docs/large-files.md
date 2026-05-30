# Large / compressed CAD files

A few of the full-instrument assemblies are too large to store uncompressed on GitHub
(GitHub rejects any single file over 100 MB). These are therefore committed as
**compressed ZIP archives** instead of the raw `.step` / `.f3z` file. Open the archive
to obtain the original CAD file.

All affected files live in [`CAD/assemblies/`](../CAD/assemblies) and
[`CAD/3d-print/3D-Print Oxcart/`](../CAD/3d-print).

## Single-file archives

Most are ordinary single ZIPs — just unzip:

```bash
unzip "A-12 v129.step.zip"
```

| Archive | Extracts to |
|---|---|
| `A-12 v129.step.zip` | `A-12 v129.step` (≈275 MB) |
| `Oxcart - no buffer v2.step.zip` | `Oxcart - no buffer v2.step` (≈78 MB) |
| `MC NEG assembly v178.step.zip` | `MC NEG assembly v178.step` (≈62 MB) |
| `F(ake)oxcart v2.step.zip` | `F(ake)oxcart v2.step` (≈218 MB) |

## Split (multi-part) archives

Two files were still over 100 MB even when compressed (the `.f3z` Fusion archives are
already compressed internally), so they are stored as **split ZIP archives**. The pieces
are `…​.z01`, `…​.z02`, … and the final `…​.zip`. **You need all parts in the same folder.**

| Archive set | Parts | Extracts to |
|---|---|---|
| `A-12 v129.f3z.zip` + `A-12 v129.f3z.z01` | 2 | `A-12 v129.f3z` |
| `F(ake)oxcart v2.f3z.zip` + `F(ake)oxcart v2.f3z.z01` | 2 | `F(ake)oxcart v2.f3z` |

Recombine and extract with the `zip` tool:

```bash
# 1. join the split parts back into a single normal zip
zip -s 0 "A-12 v129.f3z.zip" --out joined.zip
# 2. extract it
unzip joined.zip          # -> "A-12 v129.f3z"
```

(7-Zip and most GUI archive tools can also open split `.zip`/`.z01` sets directly if
all parts are present in the same directory.)

## Why it's done this way

This keeps the whole instrument — including the heaviest assemblies — inside a single
plain Git repository with no external hosting or Git LFS quota required. The trade-off is
that these few files must be unzipped before opening in your CAD package.
