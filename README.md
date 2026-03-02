```
PRIM-006
ORIGINSEAL
Origin sealing

STATUS: REGISTERED
REGISTRY: https://speedkit.eu
SNAPSHOT: https://speedkit.eu/REGISTRY_SNAPSHOT.json
```

Registered artifact. Identity governed by SPEEDKIT registry.

STATUS: FINAL

---

Registered artifact. Identity governed by SPEEDKIT registry.

STATUS: FINAL

---

**ORIGINSEAL v0.0.0** is an origin primitive.

It does not decide.
It does not verify.
It does not witness.
It does not execute.
It does not enforce.

It **seals origin**.

ORIGINSEAL exists to mark the first irreversible moment something comes into being.

---

## Philosophy

Most disputes do not begin at failure.
They begin at origin.

ORIGINSEAL exists to answer a question that must only be answered once:

> **Where did this come from, originally?**

Not who claims it now.
Not who modified it later.
Not who interprets it.

Only origin.

Once sealed, origin cannot be replaced.

---

## What ORIGINSEAL Is

ORIGINSEAL is a **provenance primitive**.

It binds:

* Initial input (stdin)
* Repository identity
* Timestamp
* First observer context

Into a single, immutable origin record.

The result is **genesis evidence**.

---

## What It Is Not

* Not a verifier
* Not a validator
* Not a judge
* Not a witness of ongoing state
* Not a versioning system
* Not an access control mechanism

Anything that evaluates, modifies, or approves content is out of scope.

---

## Behavior

* Consumes input exclusively via `stdin`
* Refuses silent invocation
* Requires explicit declaration of origin intent
* Records the first sealing event only
* Appends origin records to an immutable ledger
* Emits exactly one verdict
* Exits immediately after sealing

No retries.
No flags.
No configuration.

---

## Verdicts

ORIGINSEAL emits exactly one of the following:

* `SEALED` — origin successfully recorded
* `DENIED` — origin cannot be sealed (invalid or ambiguous)

The verdict concerns **genesis**, not correctness.

---

## Usage

ORIGINSEAL is never run casually.
It is invoked only at the moment of creation.

```sh
<origin-context> | ./originseal.sh
```

### Example

```sh
echo "initial publication of artifact" | ./originseal.sh
```

If origin conditions are satisfied:

```text
SEALED
```

If origin is ambiguous or already sealed:

```text
DENIED
```

---

## Contract

Once sealed:

* Origin is fixed
* Later claims are subordinate
* Disputes shift from authorship to custody
* Responsibility attaches permanently

ORIGINSEAL guarantees **non-replaceable origin**.

---

## Relationship to Other Artifacts

* **GUILLOTINE** — executes
* **IRREVOCULL** — judges
* **ATTESTORIUM** — witnesses
* **VALIDEXOR** — verifies
* **LIMENWARD** — guards transitions
* **ORIGINSEAL** — seals genesis

Each artifact occupies exactly one irreversible role.
None overlap.

---

## Warning

Sealing origin creates ownership gravity.

Once sealed, you cannot claim ignorance.
You cannot claim coincidence.
You cannot claim replacement.

That is the point.

---

## About

ORIGINSEAL is a minimal, deterministic origin-sealing primitive for irreversible systems.

If origin does not matter, do not use it.
If it does, nothing else is sufficient.

---

## Responsibility Boundary

This software is provided under the MIT License.

The MIT License permits use, copying, modification, and redistribution of the code, but it does not provide assurance, certification, audit defense, operational guarantees, or liability coverage.

Use of this software in environments where failure, compliance, legal exposure, or irreversible decisions matter requires an accountable party.

The original maintainer is available for assurance, adaptation, and responsibility when such accountability is required.

Contact: contact@speedkit.eu

Authoritative signed records are issued separately and are not produced by the software.
