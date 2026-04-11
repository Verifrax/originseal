# ORIGINSEAL

Primitive ID: PRIM-001  
Package: @verifrax/originseal  
Binary: originseal

Verifrax primitive — origin sealing primitive for deterministic irreversible systems.

---

## Terminal planes

- **[ANAGNORIUM](https://github.com/Verifrax/ANAGNORIUM)** — terminal recognition
- **[REGRESSORIUM](https://github.com/Verifrax/REGRESSORIUM)** — terminal recourse

## Status

Current release status: pre-stable primitive release line.

Canonical release target:

package version: 0.1.0  
tag: v0.1.0

ORIGINSEAL is part of the Verifrax primitive layer and follows the canonical primitive governance, naming, version, and packaging rules.

---

## Purpose

ORIGINSEAL establishes the first deterministic origin anchor of an artifact.

Before custody, time ordering, verification, attestation, judgment, or termination can occur, an artifact must have a fixed origin moment.

ORIGINSEAL provides that anchor.

---

## What This Primitive Does

- seals the first identifiable origin state of an artifact
- binds the artifact to a deterministic origin identity
- emits a stable origin result that downstream primitives can consume

---

## What This Primitive Does Not Do

- does not preserve custody
- does not determine temporal ordering beyond origin
- does not verify correctness
- does not witness or attest
- does not judge validity
- does not terminate lifecycle

---

## Behavioral Contract

Invocation model:

executable: originseal  
package: @verifrax/originseal  
runtime: CLI-first

The primitive operates on explicit artifact input.

If no valid input artifact exists, ORIGINSEAL must not produce a fabricated origin state.

Exit codes:

0 — origin sealed successfully  
non-zero — invocation failed or contract violated

---

## Usage

Install:

npm install -g @verifrax/originseal

Execute:

originseal artifact.json

stdin example:

cat artifact.json | originseal

---

## Determinism Guarantees

For identical canonical input, ORIGINSEAL must produce identical origin output.

No hidden environmental state may influence the result.

---

## Security Model

ORIGINSEAL prevents ambiguity about the first existence of an artifact.

It does not protect against later lifecycle risks such as custody loss, verification failure, or governance disputes.

Those responsibilities belong to downstream primitives.

---

## Relationship to Other Primitives

Canonical primitive order:

1 originseal  
2 archicustos  
3 kairoclasp  
4 limenward  
5 validexor  
6 attestorium  
7 irrevocull  
8 guillotine

Repositories:

https://github.com/Verifrax/originseal  
https://github.com/Verifrax/archicustos  
https://github.com/Verifrax/kairoclasp  
https://github.com/Verifrax/limenward  
https://github.com/Verifrax/validexor  
https://github.com/Verifrax/attestorium  
https://github.com/Verifrax/irrevocull  
https://github.com/Verifrax/guillotine

---

## Installation

npm install -g @verifrax/originseal

---

## License

MIT

## Adjacent sovereign surfaces

This repository is part of the Verifrax sovereign stack and remains bounded relative to:

- **[ANAGNORIUM](https://github.com/Verifrax/ANAGNORIUM)** for terminal recognition
- **[REGRESSORIUM](https://github.com/Verifrax/REGRESSORIUM)** for terminal recourse

