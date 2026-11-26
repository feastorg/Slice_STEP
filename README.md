<div align="center">
  <!-- Title: -->
  <a href="https://github.com/uwo-fast">
    <img src="https://github.com/uwo-fast/.github/blob/main/branding/FAST%20Logo%20Orange%20on%20White%20Transparent.png" height="100">
  </a>
  <h2><a href="https://github.com/uwo-fast/Slice_STEP"> STEP Slice </a></h2>
  <!-- Labels: -->
  <!-- First row: -->
  <a href="https://github.com/uwo-fast/.github/blob/main/collaborating.md">
    <img src="https://img.shields.io/badge/Collaborators-Welcome-lightgreen" alt="Collaborators">
  </a>
  <a href="https://github.com/uwo-fast/.github/blob/main/contributing.md">
    <img src="https://img.shields.io/badge/Contributions-Welcome-lightgreen" alt="Contributions">
  </a>
  <a href="https://www.appropedia.org/Category:FAST_literature_reviews">
    <img src="https://img.shields.io/badge/Appropedia-Lit_Review-white" alt="Appropedia">
  </a>
  <a href="https://certification.oshwa.org/">
    <img src="https://img.shields.io/badge/OSHWA-Incomplete-cc3300?style=flat-square" height="20" alt="OSHWA">
    <!-- img src="https://img.shields.io/badge/OSHWA-Certified-darkgreen?style=flat-square" height="20" alt="OSHWA" -->       <!-- img src="https://img.shields.io/badge/OSHWA-Pending-darkorange?style=flat-square" height="20" alt="OSHWA" -->
  </a>
  <a href="https://osf.io/">
    <img src="https://img.shields.io/badge/OSF-Project-lightblue" alt="OSF">
  </a>
  <a href="https://doi.org">
    <img src="https://img.shields.io/badge/Paper-Unsubmitted-ff0066" alt="Paper">
  </a>
  <!-- Second row: -->
  <br>
  <a href="https://github.com/uwo-fast/Slice_STEP/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/uwo-fast/Slice_STEP" alt="License">
  </a>
  <a href="https://github.com/uwo-fast/Slice_STEP">
    <img src="https://img.shields.io/github/repo-size/uwo-fast/Slice_STEP" alt="Repo Size">
  </a>
  <a href="https://github.com/uwo-fast/Slice_STEP/issues">
    <img src="https://img.shields.io/github/issues/uwo-fast/Slice_STEP" alt="Issues">
  </a>
  <a href="https://github.com/uwo-fast/Slice_STEP/network/members">
    <img src="https://img.shields.io/github/forks/uwo-fast/Slice_STEP?style=social" alt="Forks">
  </a>
  <a href="https://github.com/uwo-fast/Slice_STEP/stargazers">
    <img src="https://img.shields.io/github/stars/uwo-fast/Slice_STEP?style=social" alt="Stars">
  </a>
  <!-- Short description: -->
  <h3>Stepper Motor Driver Carrier Slice for BREAD.</h3>
</div>


## Introduction
[Provide a brief introduction to the project, including the motivation and goals. Explain the significance and context of the research.]

## Project Overview
[Describe the project in more detail. This section can be split into subsections if necessary.]

## Ratings

Motor supply (VMOT, the board's M_POWER net) comes from one of two sources,
picked by a jumper on J5:

| J5 jumper | Drivers powered from | VMOT range |
| --- | --- | --- |
| pins 2-3 (OUT-12V) | BREAD bus +12V (J1 pins 2 and 9) | 12 V, as the bus supplies |
| pins 1-2 (CUSTOM-OUT) | CUSTOM PWR terminal J6 (+ pin 1, - pin 2) | 8-35 V |

J5 pin 1 is CUSTOM, pin 2 is M_POWER (OUT), pin 3 is +12V. Fit one jumper
only. No position ties the CUSTOM supply to the bus.

- 8-35 V is the A4988 carrier's motor supply range (Pololu #1182). The
  CUSTOM input's bypass capacitor C3 is rated 50 V (10 uF X7R).
- In 12 V mode all four drivers draw through the bus feed; its narrowest
  stretch is 1.0 mm of 1 oz copper, about 2.4 A in total for a 10 C rise
  (IPC-2221 estimate). The M_POWER runs to the drivers are 1.5 mm, about
  3.2 A on the same basis.

## Installation
[Provide instructions for installing any necessary software or hardware components.]

## Usage
[Explain how to use the project. Include examples and screenshots if applicable.]

### Basic Usage
[Provide basic usage instructions.]

### Advanced Usage
[Provide advanced usage instructions, including any optional features or configurations.]

## Documentation
[Link to the detailed documentation if available. Provide instructions on how to access and navigate the documentation.]

## Contributing
[Explain how others can contribute to the project. Include guidelines for submitting issues, pull requests, and any coding standards.]

### Code of Conduct
[Link to the project's code of conduct if available.]

## License
[State the license under which the project is distributed. Include a link to the full license text.]

## Acknowledgements
[Acknowledge any contributors, collaborators, funding sources, or organizations that supported the project.]

## Contact
[Provide contact information for the project maintainer(s) or lead researcher(s). Include an email address or a link to a contact form.]

---

<div align="center">
  <p>
    <img src="https://img.shields.io/badge/Developed_by-UWO--FAST-orange" alt="Developed by UWO-FAST">
    <img src="https://img.shields.io/badge/Powered_by-Open_Source-blue" alt="Powered by Open Source">
  </p>
</div>
