# Bibliography

Grouped by phase. Prefer primary sources. Local PDFs go in `papers/` (git-ignored); name them `<year>-<first-author>-<short-title>.pdf`.

## Phase 1 — PQC foundations

- [FIPS 203 — ML-KEM](https://csrc.nist.gov/pubs/fips/203/final) — primary source on the KEM and its parameters
- [FIPS 204 — ML-DSA](https://csrc.nist.gov/pubs/fips/204/final) — primary source on lattice signatures
- [FIPS 205 — SLH-DSA](https://csrc.nist.gov/pubs/fips/205/final) — primary source on hash-based signatures
- [Open Quantum Safe](https://openquantumsafe.org/) — liboqs, oqs-provider; test bench for PQ TLS experiments
- [IETF PQUIP WG](https://datatracker.ietf.org/wg/pquip/about/) — PQ use in protocols
- [IETF TLS WG documents](https://datatracker.ietf.org/wg/tls/documents/) — hybrid key exchange and PQ certificate drafts
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
- [IonQ — ECDLP-256 resource estimate (2026)](https://arxiv.org/abs/2609.05625) — latest ECDLP estimate
- Craig Gidney's blog (algassert.com), Quantum Computing Report, The Quantum Insider — tracking progress without the noise

## Phase 4 — Niche and market

- [Monero research-lab issue #159 — PQ signatures](https://github.com/monero-project/research-lab/issues/159) — open discussion
- [BIP-360](https://github.com/bitcoin/bips/blob/master/bip-0360.mediawiki) — Bitcoin PQ migration proposal
- Ethereum research forum (post-quantum tag) — open discussion

## All phases

- IACR ePrint (PQC sections) — recent papers
- Real World Crypto (talk videos) — practitioner talks
- PQCrypto conference — academic venue
