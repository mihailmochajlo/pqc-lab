# Phase 1 — PQC foundations (Oct–Dec 2026)

**Outcome:** understand the three NIST standard algorithms from the inside; explain why an ML-DSA signature weighs 2.4 KB and what that breaks in a real protocol.

## Topics

### Maths (only as much as needed)
- [ ] Lattices: basic intuition, bases, short vectors
- [ ] LWE and Module-LWE; why they are believed quantum-resistant
- [ ] Hash-based signatures (SLH-DSA) as the lattice-free fallback

### NIST standards (read the documents, not summaries)
- [ ] FIPS 203 — ML-KEM: parameter sets, sizes, implementation requirements
- [ ] FIPS 204 — ML-DSA: parameter sets, sizes, implementation requirements
- [ ] FIPS 205 — SLH-DSA: parameter sets, sizes, trade-offs

### Hybrid schemes
- [ ] X25519 + ML-KEM combination in one key exchange, and why hybrid
- [ ] IETF draft: hybrid key exchange in TLS 1.3
- [ ] IETF draft: ML-KEM in SSH
- [ ] IETF draft: composite signatures for X.509

### Engineering pitfalls
- [ ] Key/signature sizes vs MTU and protocol limits
- [ ] Side-channel attacks on lattice implementations
- [ ] Deterministic vs randomised signatures
- [ ] Randomness quality

## Practice (gate artefacts)
- [ ] OQS TLS bench: classical vs hybrid vs pure-PQ sizes and handshake times → [labs/oqs-tls-bench](../../labs/oqs-tls-bench/)
- [ ] Teaching ML-KEM in Python, checked against NIST test vectors → [labs/mlkem-python](../../labs/mlkem-python/)
- [ ] Public write-up: "What actually changes in the TLS handshake when moving to ML-KEM"

## Checkpoint (end of December)
- [ ] How does ML-KEM differ from ML-DSA in purpose and structure?
- [ ] Why hybrid rather than pure PQ?
- [ ] Which three things break when certificate size grows fivefold?
