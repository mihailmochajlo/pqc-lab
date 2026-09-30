# Lab: OQS TLS bench

**Phase:** 1 · **Status:** not started

## Goal

Stand up liboqs + oqs-provider for OpenSSL 3 and measure what changes in a TLS 1.3 handshake across three configurations:

1. Classical — X25519 key exchange, ECDSA P-256 certificate
2. Hybrid — X25519MLKEM768 key exchange, classical certificate
3. Pure PQ — ML-KEM-768 key exchange, ML-DSA-65 certificate chain

Metrics: ClientHello / ServerHello / Certificate sizes (bytes), total handshake bytes, TCP segments / round trips, handshake latency (p50/p95 over ≥1000 runs), CPU time per handshake.

## Done when

- [ ] Reproducible setup (Dockerfile or script) that anyone can run from this folder
- [ ] Measurement script that outputs a CSV for all three configurations
- [ ] Results table + at least one chart committed in `results/`
- [ ] Explanation of every notable jump (e.g. which message crosses an MTU / initial congestion window boundary)
- [ ] Results used in the Phase 1 public write-up in `writing/`
