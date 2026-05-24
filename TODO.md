# TODO

## Pass 1 — CI Pipeline

- [x] Pipeline added
- [x] DRC: FAIL — 6 errors (footprint_type_mismatch x3, starved_thermal x3)
- [x] ERC: FAIL — 7 errors (power_pin_not_driven x3, pin_not_driven x4)
- [ ] Fab: SKIPPED (blocked by ERC pre-flight)
- [ ] gen-kibot-index: SKIPPED
- [ ] deploy-pages: SKIPPED

## Pass 2 — Pre-Fab Review

- [ ] Fix 3x footprint_type_mismatch (expected SMD, actual Through hole)
- [ ] Fix 3x starved_thermal (incomplete thermal relief connections)
- [ ] Fix 3x power_pin_not_driven ERC errors
- [ ] Fix 4x pin_not_driven ERC errors (input pins not driven by output)
- [ ] Verify BOM completeness and sourcing
- [ ] Confirm board outline and mounting holes
- [ ] Footprint verification against datasheets
- [ ] Design review sign-off
