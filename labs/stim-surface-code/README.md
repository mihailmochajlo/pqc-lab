# Lab: surface-code memory in Stim

**Phase:** 3 · **Status:** not started

## Goal

Build rotated surface-code memory experiments in Stim at code distances 3, 5, and 7, decode with PyMatching, and reproduce the shape of the error-suppression curve from Google's "Quantum error correction below the surface code threshold" (logical error per cycle vs distance; suppression factor Λ).

## Done when

- [ ] Notebook generates circuits, samples, decodes, and plots logical error rate per round vs physical error rate for d = 3, 5, 7
- [ ] Threshold estimate from the crossing point, and Λ computed at a chosen physical error rate
- [ ] Explicit comparison with the paper's numbers, with reasons for any gap (noise model, decoder, leakage)
- [ ] Notebook published (repository + rendered version) and linked from a short write-up
