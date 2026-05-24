# TODO

## KiBot CI/Docs Pipeline

- DRC job: fail (pre-ERC finds 7 ERC errors)
- ERC job: fail (pre-DRC finds 6 DRC errors)
- Fab job: fail (pre-ERC finds 7 ERC errors)
- gen-kibot-index: skipped
- deploy-pages: skipped

### ERC Errors (7)

- power_pin_not_driven (x3)
- pin_not_driven: Input pin not driven by any Output pins (x4)

### DRC Errors (6)

- footprint_type_mismatch: expected SMD, actual Through hole (x3)
- starved_thermal: incomplete thermal relief connections (x3)
