# Lab: CBOM inventory tool

**Phase:** 2 · **Status:** not started

## Goal

A small command-line tool that scans a codebase and its dependencies for cryptographic usage and emits a CycloneDX CBOM (cryptographic bill of materials). Scope for v1: Python and C#/.NET (source calls into crypto APIs, dependency manifests, certificates and keys in the repo, TLS configuration), with each finding classified as quantum-vulnerable, quantum-safe, or unknown.

## Done when

- [ ] Output validates against the CycloneDX 1.6 schema (cryptographic-asset components)
- [ ] Run against the Alpha Clarity codebase as part of the Phase 2 migration, with the resulting CBOM reviewed by hand for false positives/negatives
- [ ] Test suite with fixture repos covering each detector
- [ ] Published: public repository with README, licence, and install instructions
