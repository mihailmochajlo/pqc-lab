# Bibliography

Grouped by phase. Prefer primary sources. Local PDFs go in `papers/` (git-ignored); name them `<year>-<first-author>-<short-title>.pdf`.

## Phase 1 — PQC foundations

- [FIPS 203 — ML-KEM](https://csrc.nist.gov/pubs/fips/203/final) — primary source on the KEM and its parameters
- [FIPS 204 — ML-DSA](https://csrc.nist.gov/pubs/fips/204/final) — primary source on lattice signatures
- [FIPS 205 — SLH-DSA](https://csrc.nist.gov/pubs/fips/205/final) — primary source on hash-based signatures
- [Open Quantum Safe](https://openquantumsafe.org/) — liboqs, oqs-provider; test bench for PQ TLS experiments
- [IETF PQUIP WG](https://datatracker.ietf.org/wg/pquip/about/) — PQ use in protocols
- [IETF TLS WG documents](https://datatracker.ietf.org/wg/tls/documents/) — hybrid key exchange and PQ certificate drafts
- [RFC 10024 — Post-Quantum Traditional (PQ/T) Hybrid Key Agreement Mechanisms for TLS 1.3](https://www.rfc-editor.org/info/rfc10024) (Aug 2026, Proposed Standard; was draft-ietf-tls-ecdhe-mlkem) — defines X25519MLKEM768, SecP256r1MLKEM768, SecP384r1MLKEM1024
- [RFC 9954](https://www.rfc-editor.org/info/rfc9954) — the hybrid key exchange framework in TLS 1.3 that RFC 10024 builds on
- [draft-ietf-tls-mlkem](https://datatracker.ietf.org/doc/draft-ietf-tls-mlkem/) — pure ML-KEM (non-hybrid) key agreement for TLS 1.3
- [draft-ietf-sshm-mlkem-hybrid-kex — PQ/T Hybrid Key Exchange with ML-KEM in SSH](https://datatracker.ietf.org/doc/draft-ietf-sshm-mlkem-hybrid-kex/) (-10, in RFC Editor queue, Informational) — mlkem768x25519-sha256 and NIST-curve variants
- [draft-ietf-lamps-pq-composite-sigs — Composite ML-DSA for use in X.509 PKI](https://datatracker.ietf.org/doc/draft-ietf-lamps-pq-composite-sigs/) (-19, in RFC Editor queue) — ML-DSA combined with RSA, ECDSA, Ed25519, Ed448
- [Cloudflare blog: post-quantum](https://blog.cloudflare.com/tag/post-quantum/) — engineering write-ups of real deployment
- Serious Cryptography, 2nd ed. — Jean-Philippe Aumasson — fast catch-up on general cryptography

## Phase 2 — Migration in real systems

- [NIST SP 1800-38 / NCCoE Migration to PQC](https://www.nccoe.nist.gov/crypto-agility-considerations-migrating-post-quantum-cryptographic-algorithms) — what organisational migration looks like
- [CNSA 2.0 FAQ (NSA)](https://media.defense.gov/2022/Sep/07/2003071836/-1/-1/0/CSI_CNSA_2.0_FAQ_.PDF) — US national-security deadlines
- [NCSC UK — PQC migration timelines](https://www.ncsc.gov.uk/guidance/pqc-migration-timelines) — UK deadlines
- [CycloneDX CBOM](https://cyclonedx.org/capabilities/cbom/) — cryptography inventory format
- [postquantum.com](https://postquantum.com/) — policy and market analysis, vendor-claim teardowns

## Phase 3 — The quantum side

- Nielsen & Chuang, *Quantum Computation and Quantum Information*, ch. 1–5, 10 — foundations and error correction
- [John Preskill — Ph229 lecture notes](http://theory.caltech.edu/~preskill/ph229/) — foundations and error correction
- [Stim](https://github.com/quantumlib/Stim) — stabilizer circuit simulator
- [PyMatching](https://github.com/oscarhiggott/PyMatching) — MWPM decoder
- [Qualtran](https://github.com/quantumlib/Qualtran) — resource estimation
- [Google Quantum AI — Quantum error correction below the surface code threshold (Nature)](https://www.nature.com/articles/s41586-024-08449-y) — key paper to take apart
- [Roetteler et al. 2017 — Quantum resource estimates for computing elliptic curve discrete logarithms](https://arxiv.org/abs/1706.06752) — ECDLP baseline estimate
- [Google Quantum AI — Securing Elliptic Curve Cryptocurrencies against Quantum Vulnerabilities: Resource Estimates and Mitigations](https://arxiv.org/abs/2603.28846) (Mar 2026) — ECDLP-256 with <1,200 logical qubits; [blog post](https://research.google/blog/safeguarding-cryptocurrency-by-disclosing-quantum-vulnerabilities-responsibly/)
- [IonQ — Computing 256-bit elliptic curve discrete logarithms in 26 days on a fault-tolerant trapped-ion quantum computer with 20,000 qubits](https://arxiv.org/abs/2609.05625) (Sep 2026) — latest ECDLP estimate
- [Gidney — Magic state cultivation: growing T states as cheap as CNOT gates](https://arxiv.org/abs/2409.17595) — the cultivation protocol modern estimates rely on
- [Chan, Strikis, Sun, Cai — Diagnosing and Restoring the Degraded Fault Distance of Magic State Cultivation](https://arxiv.org/abs/2609.17706) (Sep 2026) — T-state cultivation fault-distance issue and fix
- Craig Gidney's blog (algassert.com), Quantum Computing Report, The Quantum Insider — tracking progress without the noise

## Phase 4 — Niche and market

- [Monero research-lab issue #159 — PQ signatures](https://github.com/monero-project/research-lab/issues/159) — open discussion
- [BIP-360](https://github.com/bitcoin/bips/blob/master/bip-0360.mediawiki) — Bitcoin PQ migration proposal
- Ethereum research forum (post-quantum tag) — open discussion

## All phases

- IACR ePrint (PQC sections) — recent papers
- Real World Crypto (talk videos) — practitioner talks
- PQCrypto conference — academic venue
