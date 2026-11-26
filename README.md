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
- Every figure below is the total VMOT current of all four drivers
  together, not a per-driver figure (IPC-2221 estimate, 1 oz outer copper,
  20 C rise unless stated). All of it passes through the J5 jumper, so it
  is also capped by the rating of the shunt fitted there.
- 12 V mode: the bus feed's narrowest stretch is 1.0 mm, about 3.2 A
  (2.4 A for a 10 C rise).
- CUSTOM mode: the run from J6 pin 1 to J5 pin 1 is 1.5 mm, about 4.3 A.
- From J5 pin 2, M_POWER carries all four drivers through a 1.9 mm neck
  between J4 pin 8 and J5 pin 3 (about 5.2 A), then a pour at least 4.2 mm
  wide to C6 (drivers 1-3), then 2.5 mm to drivers 2 and 1. Each pin 8
  takes its own driver's current only.
- So the board carries about 3 A in total in 12 V mode and about 4 A in
  CUSTOM mode, shared by however many drivers run at once.

## Microstep mode

Each driver's step resolution is set by three solder jumpers on the back
of the board, beside that driver's MS1-MS3 pins (labelled MS1, MS2, MS3;
JP1-3 for driver 1 up to JP10-12 for driver 4). Closing a jumper ties that
pin to VDD (+5V). The A4988 pulls MS1-MS3 down internally, so an open
jumper reads low.

| MS1 | MS2 | MS3 | Step |
| --- | --- | --- | --- |
| open | open | open | full (default) |
| closed | open | open | 1/2 |
| open | closed | open | 1/4 |
| closed | closed | open | 1/8 |
| closed | closed | closed | 1/16 |

The Nano does not drive these pins: A6 and A7 are analog-input-only on the
ATmega328P, and D13 is left free.

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
