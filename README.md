# Oxcart

Hardware and design files of the Oxcart Titanium atom probe.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-green.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Funded by the ERC](https://img.shields.io/badge/Funded%20by-ERC%20Starting%20Grant%20805065-003399.svg)](https://cordis.europa.eu/project/id/805065)

The Oxcart Titanium atom probe is an open-hardware, straight-flight-path, microelectrode atom probe designed by Peter Felfer in the course of his ERC Starting Grant. You are very welcome to build your own version, remix it, or use components in your own designs. The license is GPL, so be aware that this requires you to share derivative work alike. The system is run by the [PyCCAPT](https://github.com/mehrpad/pyccapt) software package, which contains experiment and system control ([documentation](https://pyccapt.readthedocs.io/en/latest/)). Integration of Surface Concept and RoentDek detectors is implemented.

Here you can find a collection of the files you need to build this atom probe.

---

## Repository layout

All custom-designed parts live under [`CAD/`](CAD), grouped by subsystem:

| Folder | Contents |
|---|---|
| [`CAD/assemblies`](CAD/assemblies) | Full-instrument and major sub-assemblies (A-12, Oxcart-no-buffer, BC3, LL, MC laser/lid/NEG) |
| [`CAD/vacuum`](CAD/vacuum) | Chambers, pumps, vacuum parts, valves & manipulation |
| [`CAD/cryo`](CAD/cryo) | Cryo systems (MC, BC), cryo heads, cryo LL |
| [`CAD/optics-laser`](CAD/optics-laser) | Optics and the laser-upgrade stage |
| [`CAD/detector`](CAD/detector) | Detector flange and DLD assemblies |
| [`CAD/sample-handling`](CAD/sample-handling) | Sample stage & pucks, load-lock/buffer-chamber parts, transfer shuttle, automation |
| [`CAD/frame`](CAD/frame) | Instrument frame |
| [`CAD/gas-thermal`](CAD/gas-thermal) | Gas charging devices, baking equipment, lamp holder |
| [`CAD/electronics`](CAD/electronics) | Electrical & electronics parts |
| [`CAD/fasteners`](CAD/fasteners) | Custom fasteners |
| [`CAD/machining`](CAD/machining) | Manufacturing drawings (DXF/PDF) and Pocket NC CAM |
| [`CAD/measurement`](CAD/measurement) | Measurement / gauging hardware |
| [`CAD/3d-print`](CAD/3d-print) | 3D-printable model of the instrument |

Each part is provided both as a neutral **STEP** file (opens in any CAD package) and as
its editable **Fusion 360** source (`.f3z` / `.f3d`). Where multiple iterations existed,
only the latest version of each part is included.

### Off-the-shelf parts

Commercial, off-the-shelf components (optics, vacuum hardware, motion stages, fasteners,
etc.) are **not** redistributed here. They are listed by supplier and part number in
[`BOM.md`](BOM.md) so you can obtain the original models from each vendor.

### Large files

A handful of big assemblies are stored as compressed (and, in two cases, split) ZIP
archives because they exceed GitHub's 100 MB per-file limit. See
[`docs/large-files.md`](docs/large-files.md) for how to unpack them.

---

## Funding Acknowledgement

<a href="https://cordis.europa.eu/project/id/805065">
  <img src="LOGO-ERC_negatif.jpg" alt="European Research Council logo" align="right" width="280" />
</a>

The Oxcart atom probe was designed and built in the framework of the ERC project
**HydMet — *Fundamentals of Hydrogen in Structural Metals at the Atomic Scale*** ([Grant Agreement No. 805065](https://cordis.europa.eu/project/id/805065)),
funded by the European Research Council under the European Union's Horizon 2020 research and innovation programme (ERC Starting Grant, 2018–2024, host institution: Friedrich-Alexander-Universität Erlangen-Nürnberg).

> This project has received funding from the European Research Council (ERC) under the European Union's Horizon 2020 research and innovation programme (grant agreement No 805065).

If you build on, remix, or publish work that uses this hardware, please reproduce the acknowledgement above.

<br clear="right" />

---

## Strengths

- Excellent vacuum (< 10⁻¹¹ mbar)
- Next to no residual hydrogen
- Good mass resolution (limited by straight flight path)
- Highest possible detection efficiency
- Very flexible hardware for custom experiments
- Easy maintenance

## Known problems / limitations

- Currently used piezo stage lacks lift force (being replaced)
- Weight distribution on optical table too uneven to use air suspension
- Limited low-temperature capability (currently 35 K, but 20 K possible with improvements)
- Only 3 pucks in load lock currently

This machine is constantly being improved, so for the latest design iteration of all components, contact the author. Currently, a stage redesign is in progress to integrate a laser with in-situ dual-side focusing.

---

## Control software

The instrument is run by **PyCCAPT**, an open-source Python package for atom-probe experiment and system control:

- Repository: <https://github.com/mehrpad/pyccapt>
- Documentation: <https://pyccapt.readthedocs.io/en/latest/>

## Citation

If you build on or publish work using the Oxcart hardware, please cite the original instrument paper:

Felfer, P., Ott, B., Monajem, M., Dalbauer, V., Heller, M., Josten, J., & Macaulay, C. (2022). *An Atom Probe with Ultra-Low Hydrogen Background.* **Microscopy and Microanalysis**, 28(4), 1255–1263. <https://doi.org/10.1017/S1431927621013702>

```bibtex
@article{Felfer2022Oxcart,
  author  = {Felfer, Peter and Ott, Benedict and Monajem, Mehrpad and
             Dalbauer, Valentin and Heller, Martina and Josten, Jan and
             Macaulay, Chandra},
  title   = {An Atom Probe with Ultra-Low Hydrogen Background},
  journal = {Microscopy and Microanalysis},
  year    = {2022},
  volume  = {28},
  number  = {4},
  pages   = {1255--1263},
  doi     = {10.1017/S1431927621013702}
}
```
