# Oxcart

Hardware and design files of the Oxcart Titanium atom probe.

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-green.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Funded by the ERC](https://img.shields.io/badge/Funded%20by-ERC%20Starting%20Grant%20805065-003399.svg)](https://cordis.europa.eu/project/id/805065)

The Oxcart Titanium atom probe is an open-hardware, straight-flight-path, microelectrode atom probe designed by Peter Felfer in the course of his ERC Starting Grant. You are very welcome to build your own version, remix it, or use components in your own designs. The license is GPL, so be aware that this requires you to share derivative work alike. The system is run by the PyCCAPT software package, which contains experiment and system control. Integration of Surface Concept and RoentDek detectors is implemented.

Here you can find a collection of the files you need to build this atom probe.

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
