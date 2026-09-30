# Phase 2 — Migration in real systems (Jan–Mar 2027)

**Outcome:** one real system migrated end to end; fluent in inventory, crypto-agility, and regulatory deadlines.

## Topics

### Organisational migration
- [ ] Cryptographic inventory (CBOM — cryptographic bill of materials)
- [ ] Prioritisation by secret/data lifetime; phased migration plan
- [ ] NIST SP 1800-38 / NCCoE Migration to PQC
- [ ] CISA guidance
- [ ] UK NCSC guidance and migration timelines

### Regulatory map
- [ ] CNSA 2.0 (US defence sector)
- [ ] US federal deadlines 2030–2031
- [ ] France: ANSSI requirements from 2027
- [ ] EU PQC roadmap and NIS2
- [ ] Banking: DORA (EU)

### PKI and certificates
- [ ] Composite and hybrid certificates
- [ ] Merkle Tree Certificates (Google/Cloudflare proposal)
- [ ] Why signatures are harder to migrate than key exchange

### Hardware
- [ ] HSM PQ support; firmware and secure boot
- [ ] Cloud KMS PQ support: AWS KMS, Azure Key Vault, Google Cloud KMS

### Identity and tokens
- [ ] JWT/JWS with ML-DSA
- [ ] FIDO2 / passkeys and PQ
- [ ] OAuth/OIDC: where signature size breaks headers and cookies

## Practice (gate artefacts)
- [ ] Alpha Clarity PQ migration: crypto inventory, hybrid TLS at the edge, PQ token signatures where possible, plan for the rest (docs in English in that repo)
- [ ] CBOM inventory tool (CycloneDX output), published → [labs/cbom-tool](../../labs/cbom-tool/)
- [ ] Public write-up of the migration: what broke, what was deferred, cost in hours

## Checkpoint (end of March)
- [ ] Sketch a migration plan for an unfamiliar mid-sized system in one hour, ordered by data lifetime and regulatory deadlines
