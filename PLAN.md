# Plan: Quantum Security Expertise in 12 Months

> English mirror of the Claude Doc "План: экспертность в квантовой безопасности за 12 месяцев":
> https://claude.ai/code/artifact/b916a49a-9e9c-4960-bb37-62b0dc0b7612
> The doc is the canonical version. Last synced: 2026-09-30.

## Goal and principles

By **2027-09-30**, be a credible candidate for roles such as PQC migration engineer / lead or cryptography engineer, with a portfolio of one real migration project, public write-ups, and open-source contributions. Budget: 8–12 hours per week, about 450 hours over the year.

Principles the plan rests on:

- **One main track.** Post-quantum cryptography (PQC) gets 70% of the time; quantum computing as such gets 30% — just enough to read primary sources and not depend on other people's summaries.
- **Projects over courses.** Every phase ends with an artefact you can show: code, a write-up, a talk. Knowledge without an artefact counts as not done.
- **Build on what already exists:** authentication and PKI experience, distributed systems, the weekly quantum-threat digest. None of this starts from zero.
- **Public from month one:** short write-ups in the open, so that by the end of the year there is a trail that recruiters and clients can find.

## Phase 1 (Oct–Dec 2026): PQC foundations

**Outcome:** you understand the three standard NIST algorithms from the inside and can explain to a colleague why an ML-DSA signature weighs 2.4 KB and what that breaks in a real protocol.

### What to study

- **Maths, exactly as much as needed:** lattices, the LWE and Module-LWE problems, why they are considered resistant to quantum attacks; hash-based signatures (SLH-DSA) as the lattice-free "insurance" option.
- **NIST standards:** FIPS 203 (ML-KEM, key encapsulation), FIPS 204 (ML-DSA, signatures), FIPS 205 (SLH-DSA). Read the documents themselves, not summaries: the sections on parameters, sizes, and implementation requirements.
- **Hybrid schemes:** how classical X25519 and ML-KEM combine in a single key exchange, and why (protection against flaws in the new algorithm). IETF drafts: hybrid key exchange in TLS 1.3, ML-KEM in SSH, composite signatures for X.509.
- **Engineering pitfalls:** key and signature sizes vs. MTU and protocol limits, side-channel attacks on lattice implementations, deterministic vs. randomised signatures, randomness quality.

### Practice (main phase artefact)

- [ ] Stand up an Open Quantum Safe test bench: liboqs + oqs-provider for OpenSSL. Measure sizes and handshake time for classical, hybrid, and pure-PQ TLS. Write the results up briefly.
- [ ] Implement a teaching ML-KEM in Python from the FIPS 203 specification (no optimisations, for understanding only); check against NIST test vectors.
- [ ] Publish the first public write-up: "What actually changes in the TLS handshake when moving to ML-KEM", with your own measurements.

### Checkpoint (end of December)

You can answer without preparation: how ML-KEM differs from ML-DSA in purpose and structure; why hybrid rather than pure PQ; which three things break when certificate size grows fivefold.

## Phase 2 (Jan–Mar 2027): Migration in real systems

**Outcome:** you have carried out an end-to-end migration of one real system and speak the language of those who hire for these roles: inventory, crypto-agility, regulatory deadlines.

### What to study

- **What migration looks like in a large organisation:** cryptographic inventory (CBOM — cryptographic bill of materials), prioritisation by secret lifetime, a phased plan. References: NIST SP 1800-38, NCCoE Migration to PQC, CISA and UK NCSC guidance.
- **The regulatory map asked about in interviews:** CNSA 2.0 (US, defence sector), US federal deadlines 2030–2031, French ANSSI from 2027, the EU PQC roadmap and NIS2, banking requirements (DORA in the EU).
- **PKI and certificates:** composite and hybrid certificates, Merkle Tree Certificates (Google/Cloudflare proposal, backed by Apple in September 2026), why signatures are harder to migrate than key exchange.
- **Hardware side:** what HSMs and cloud KMS (AWS KMS, Azure Key Vault, Google Cloud KMS) support in PQ algorithms; firmware and secure boot.
- **Identity and tokens — your strong suit:** JWT/JWS with ML-DSA, FIDO2/passkeys and PQ, OAuth/OIDC, where signature size breaks headers and cookies.

### Practice (main phase artefact)

- [ ] Carry out a full PQ migration of Alpha Clarity's authentication and external channels: inventory all cryptography in the system, hybrid TLS at the edge, PQ token signatures where possible, a plan for the rest. Documentation in the repository in English, as is the project convention.
- [ ] Write a small cryptography inventory tool for a codebase and its dependencies (output in CycloneDX CBOM format) and publish it.
- [ ] Publish a migration write-up: what broke, what had to be deferred, what it cost in hours.

### Checkpoint (end of March)

You can sketch a migration plan for an unfamiliar mid-sized system in an hour and justify the order of steps by data lifetime and regulatory deadlines. From this point you can start applying for PQC roles without waiting for the end of the plan.

## Phase 3 (Apr–Jun 2027): The quantum side

**Outcome:** you read a paper like "256-bit ECDLP in 26 days" on your own and can name its three weakest assumptions. The goal is not to become a quantum engineer but to stop depending on summaries when assessing the threat.

### What to study

- **Basics:** qubits, gates, measurement, entanglement, the quantum Fourier transform and Shor's algorithm — the first chapters of Nielsen & Chuang or Preskill's lectures. Enough to derive yourself why Shor breaks elliptic curves while Grover only halves the effective length of symmetric keys.
- **Error correction:** what a logical qubit, threshold, and code distance are; surface code vs. qLDPC; why magic states are the bottleneck; what a decoder does and why it must run in real time. Google's "Quantum error correction below the surface code threshold" is mandatory, with every number taken apart.
- **Resource estimates:** how an algorithm turns into "this many qubits, this many days": Toffoli-gate counts, magic-state factories, machine clock speed. Take apart three ECDLP-256 estimates — Roetteler et al. 2017, Google (March 2026), IonQ (September 2026) — and understand what drives the numbers down.
- **Hardware modalities, one page each:** superconducting, trapped ions, neutral atoms, photonics — clock speed, fidelity, connectivity, scaling limits.

### Practice (main phase artefact)

- [ ] Build a surface-code memory experiment in Stim at distances 3, 5, 7, decode with PyMatching, and reproduce the error-suppression curve from the Google paper. Publish the notebook.
- [ ] Run a resource estimate for Shor on P-256 in the Azure Quantum Resource Estimator and in Qualtran; compare with published numbers and explain the discrepancies.
- [ ] Revisit your own CRQC timeline estimate and record it with a rationale — this becomes the baseline for the weekly digest.

### Checkpoint (end of June)

Given a press release about a "breakthrough", you find the primary source in ten minutes and say which of the eight digest blockers it moves, and by how much.

## Phase 4 (Jul–Sep 2027): Specialisation and going to market

**Outcome:** you have a narrow niche where people know you, and a portfolio you can take into both hiring and consulting.

### Niche: post-quantum security of blockchains and digital assets

Why this one: experts are few, demand is growing from funds, exchanges, and protocols, and you already have a base from the digest and trading-systems experience. Study: BIP-360 and the Bitcoin migration debate, Ethereum's plans for PQ signatures and account abstraction, the Zcash roadmap, Monero Research Lab discussions on Raccoon and the turnstile, and the problem of exposed public keys and dormant coins.

### Practice (main phase artefacts)

- [ ] Write a long-form analysis: "What exactly Monero/Bitcoin/Ethereum lose when a CRQC appears, and in what order", with attack-cost estimates based on Phase 3.
- [ ] Make one visible open-source contribution: a PR to liboqs / oqs-provider, or to a PQ library in Rust/Go, or a review of an MRL proposal.
- [ ] Speak at a local meetup or conference (in Dublin: OWASP, security meetups, crypto communities) with a talk on the Phase 2 migration.
- [ ] Rebuild CV and profiles for PQC engineer / cryptography engineer / security architect (PQC) roles: migration project, inventory tool, publications, open-source contributions.

### Where to look for work

Cloud providers and CDNs (cryptography teams at Cloudflare, AWS, Google, Microsoft), HSM and PKI vendors (Thales, Entrust, DigiCert, Keyfactor), banks and payment systems with PQ programmes, specialist PQC companies (PQShield, SandboxAQ, QuSecure), crypto exchanges and custodians. In Ireland most of them have offices or hire remotely.

### Checkpoint (end of September 2027)

At least three interviews or consulting requests on PQC topics that came through publications or referrals, not cold applications.

## Weekly rhythm and checkpoints

At 10 hours per week this split works: 4 hours of theory and primary-source reading, 4 hours on the current phase's practical project, 1 hour on the Monday digest (read it and open one primary source from it), 1 hour writing down what you understood — public write-ups are assembled from these notes. Theory without a project fades within a month, so if time is short, cut theory, not practice.

A phase is closed only when its main artefact is published and the checkpoint question is passed. If a phase overruns by more than a month, trim the next phase rather than shifting everything: phases 1 and 2 matter more for the goal than 3 and 4.

Roadmap (the doc has a chart; summary here):

| Phase | Months | Gate artefact |
| --- | --- | --- |
| 1 — PQC foundations | Oct–Dec 2026 | OQS TLS bench + write-up "What changes in the TLS handshake with ML-KEM" |
| 2 — Migration in real systems | Jan–Mar 2027 | Alpha Clarity PQ migration + CBOM tool + migration write-up (after this, start applying) |
| 3 — The quantum side | Apr–Jun 2027 | Stim surface-code notebook + P-256 resource estimate + revised CRQC estimate |
| 4 — Niche and market | Jul–Sep 2027 | Blockchain CRQC analysis + OSS contribution + talk + CV |

## Materials library

| Phase | Material | Why |
| --- | --- | --- |
| 1 | [FIPS 203 ML-KEM](https://csrc.nist.gov/pubs/fips/203/final), [FIPS 204 ML-DSA](https://csrc.nist.gov/pubs/fips/204/final), [FIPS 205 SLH-DSA](https://csrc.nist.gov/pubs/fips/205/final) | Primary sources on algorithms and parameters |
| 1 | [Open Quantum Safe](https://openquantumsafe.org/) — liboqs, oqs-provider | Test bench for PQ TLS experiments |
| 1 | [IETF PQUIP](https://datatracker.ietf.org/wg/pquip/about/) and [TLS WG](https://datatracker.ietf.org/wg/tls/documents/) | Drafts on hybrid key exchange and PQ certificates |
| 1 | [Cloudflare blog: post-quantum](https://blog.cloudflare.com/tag/post-quantum/) | Best engineering write-ups of real deployment |
| 1 | Serious Cryptography, 2nd ed. (Aumasson) | Fast catch-up on general cryptography |
| 2 | [NIST SP 1800-38 / NCCoE Migration to PQC](https://www.nccoe.nist.gov/crypto-agility-considerations-migrating-post-quantum-cryptographic-algorithms) | What organisational migration looks like |
| 2 | [CNSA 2.0 FAQ](https://media.defense.gov/2022/Sep/07/2003071836/-1/-1/0/CSI_CNSA_2.0_FAQ_.PDF), [NCSC UK PQC migration timelines](https://www.ncsc.gov.uk/guidance/pqc-migration-timelines) | Regulatory deadlines |
| 2 | [CycloneDX CBOM](https://cyclonedx.org/capabilities/cbom/) | Cryptography inventory format |
| 2 | [postquantum.com](https://postquantum.com/) | Policy and market analysis, vendor-claim teardowns |
| 3 | Nielsen & Chuang, ch. 1–5, 10; [Preskill's lectures](http://theory.caltech.edu/~preskill/ph229/) | Foundations of quantum computing and error correction |
| 3 | [Stim](https://github.com/quantumlib/Stim), [PyMatching](https://github.com/oscarhiggott/PyMatching), [Qualtran](https://github.com/quantumlib/Qualtran) | Code simulation, decoding, resource estimation |
| 3 | [Google: QEC below the surface code threshold](https://www.nature.com/articles/s41586-024-08449-y), [Roetteler et al. 2017](https://arxiv.org/abs/1706.06752), [IonQ ECDLP-256 (2026)](https://arxiv.org/abs/2609.05625) | Key papers to take apart |
| 3 | Craig Gidney's blog (algassert.com), Quantum Computing Report, The Quantum Insider | Tracking progress without the noise |
| 4 | [Monero research-lab: PQ signatures #159](https://github.com/monero-project/research-lab/issues/159), [BIP-360](https://github.com/bitcoin/bips/blob/master/bip-0360.mediawiki), Ethereum research forum (post-quantum tag) | Open discussions to take part in |
| all | IACR ePrint (PQC sections), Real World Crypto (talk videos), PQCrypto | Conferences and recent work |
