# Lab: teaching ML-KEM in Python

**Phase:** 1 · **Status:** not started

## Goal

Implement ML-KEM (FIPS 203) in plain Python straight from the specification, for understanding only: no optimisations, no constant-time guarantees, never for production use. Cover all three parameter sets (ML-KEM-512, -768, -1024).

Components: NTT and polynomial arithmetic over R_q, byte encoding/decoding, compression, sampling (SampleNTT, SamplePolyCBD), K-PKE, and ML-KEM KeyGen / Encaps / Decaps including implicit rejection.

## Done when

- [ ] Every function maps to a named algorithm in FIPS 203 (algorithm number in the docstring)
- [ ] Passes the official NIST ACVP test vectors for KeyGen, Encaps, and Decaps for all three parameter sets
- [ ] Unit tests run with `pytest` from this folder
- [ ] Short `NOTES.md`: what surprised you, where the spec was hardest to follow, how sizes follow from parameters
