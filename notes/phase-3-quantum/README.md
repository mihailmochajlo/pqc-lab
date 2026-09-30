# Phase 3 — The quantum side (Apr–Jun 2027)

**Outcome:** read a paper like "256-bit ECDLP in 26 days" unaided and name its three weakest assumptions.

## Topics

### Basics
- [ ] Qubits, gates, measurement, entanglement
- [ ] Quantum Fourier transform
- [ ] Shor's algorithm: derive why it breaks elliptic curves
- [ ] Grover: why it only halves effective symmetric key length
- [ ] Nielsen & Chuang ch. 1–5, 10 / Preskill lectures

### Error correction
- [ ] Logical qubit, threshold, code distance
- [ ] Surface code vs qLDPC
- [ ] Magic states as the bottleneck
- [ ] Decoders and why real-time decoding matters
- [ ] Google, "Quantum error correction below the surface code threshold" — every number taken apart

### Resource estimates
- [ ] Toffoli counts, magic-state factories, machine clock speed
- [ ] ECDLP-256: Roetteler et al. 2017
- [ ] ECDLP-256: Google (March 2026)
- [ ] ECDLP-256: IonQ (September 2026)
- [ ] What drives the numbers down between estimates

### Hardware modalities (one page each)
- [ ] Superconducting
- [ ] Trapped ions
- [ ] Neutral atoms
- [ ] Photonics

## Practice (gate artefacts)
- [ ] Stim surface-code memory d=3,5,7 + PyMatching, reproduce Google's suppression curve; publish notebook → [labs/stim-surface-code](../../labs/stim-surface-code/)
- [ ] Shor on P-256 resource estimate in Azure Quantum Resource Estimator and Qualtran; explain gaps vs published numbers
- [ ] Revise CRQC estimate with rationale → `digest/crqc-estimate.md` (local only)

## Checkpoint (end of June)
- [ ] Press release → primary source in 10 minutes → which of the eight blockers it moves, and by how much
