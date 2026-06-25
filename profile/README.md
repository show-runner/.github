# Show Runner

**The show must go on.**

Show Runner is an open engineering project for explaining, operating, and automating digital trust systems through the metaphor of backstage theatre.

Where Code Smell Detective investigates software quality after something smells wrong, Show Runner keeps identity, PKI, certificates, trust, and access running before the audience ever notices a problem.

It is not about solving a mystery.

It is about keeping the curtain up.

---

## What Show Runner Is About

Show Runner focuses on the operational lifecycle of digital trust:

- Certificate issuance
- Certificate renewal
- Certificate rotation
- Certificate revocation
- Trust chain management
- Root and intermediate CA operations
- Provisioning
- mTLS
- Identity verification
- Relying party validation
- Policy compliance
- Runtime health

The project began from educational work around `step-ca`, PKI, and certificates, but its scope is broader than any single tool.

`step-ca` can be one production.

`cert-manager` can be another.

A Kubernetes mTLS environment can be another.

The subject is the whole backstage machinery of digital trust.

---

## The Core Metaphor

Show Runner uses a backstage theatre metaphor inspired by live productions.

In a theatre, success means the audience experiences the performance without seeing the chaos backstage.

In PKI, success means certificates renew, identities verify, trust chains validate, and services keep communicating without drama.

The best show is often the one where nothing breaks.

---

## Show Runner vs Code Smell Detective

| Code Smell Detective | Show Runner |
|---|---|
| Investigates | Operates |
| Finds what went wrong | Keeps things running |
| Detective noir | Backstage theatre |
| Reactive | Proactive |
| Investigation | Production |
| Evidence board | Show control console |
| Verdict | Current state |
| Recommendation | Next cue |

These projects are siblings, not twins.

They can share foundations from the Open Engineering Platform, but they express different operating models.

Code Smell Detective asks:

> What went wrong, and why?

Show Runner asks:

> What needs to happen next so the show goes on?

---

## Productions, Not Investigations

The main unit of Show Runner is a **Production**.

A Production is a live operational context that must be prepared, rehearsed, run, monitored, recovered, and eventually retired.

A Production may be:

- A certificate authority
- A Kubernetes cluster using cert-manager
- A service mesh using mTLS
- A workload onboarding flow
- A root CA ceremony
- A certificate renewal process
- A production PKI environment
- A demonstration or educational scenario

A Production does not end with a verdict.

It runs until closing night.

---

## Production Lifecycle

```text
Designed
  ↓
Prepared
  ↓
Rehearsed
  ↓
Curtain Up
  ↓
Running
  ↓
Responding to Cues
  ↓
Recovering
  ↓
Encore
  ↓
Closing Night
  ↓
Archived
```

This matches how certificate and trust systems really behave.

Certificates are not issued once and forgotten.

They are issued, used, renewed, rotated, trusted, revoked, and retired in continuous loops.

---

## Show Control

Show Runner is centered around a **Show Control** model.

A show control console answers questions such as:

- Which productions are running?
- Which certificates are healthy?
- Which renewals are coming up?
- Which trust anchors are active?
- Which provisioners are admitting new actors?
- Which revocations require attention?
- Which services depend on this trust chain?
- Which cues need to fire next?

This is operational awareness, not forensic analysis.

---

## Characters

The Show Runner protagonist is deliberately unnamed.

The Show Runner can be:

- A human operator
- A platform engineer
- A Kubernetes controller
- An automated workflow
- A service account
- A CA process
- A production activity itself

Other characters represent operational responsibilities.

| Character | Responsibility |
|---|---|
| Reggie the Renewer | Automated certificate renewal |
| Roger the Revoker | Revocation, retirement, and credential decommissioning |
| Sandy the Signer | Certificate authority signing |
| Ingrid the Issuer | Intermediate CA issuance work |
| Rory the Root | Root CA authority and ceremonies |
| Percy the Provisioner | Provisioning and admission |
| Kevin the Key Keeper | Private key custody |
| Trevor the Truster | Trust store management |
| Derek the Decoder | Encoding, ASN.1, DER, PEM, and certificate readability |
| Bertie the Baseline | Rules, requirements, and compliance |
| Vera the Verifier | Relying party validation |
| Wally the Verifier | Relying party validation |

The characters are backstage crew.

Their job is not to solve crimes.

Their job is to make sure the show happens.

---

## Departments

Characters naturally group into operational departments.

```text
Production
├── Certificate Department
├── Trust Department
├── Identity Department
├── Provisioning Department
├── Security Department
├── Compliance Department
├── Renewal Department
├── Revocation Department
└── Audience Services
```

Departments coordinate through cues.

A cue is an operational signal that something must happen.

Examples:

```text
Certificate expires in 14 days
  → Cue Reggie
  → Renew certificate
  → Reload service
  → Show continues
```

```text
New workload appears
  → Cue Percy
  → Verify identity
  → Cue Sandy
  → Issue certificate
  → Actor enters stage
```

```text
Private key suspected compromised
  → Cue Roger
  → Revoke certificate
  → Cue Reggie
  → Replace certificate
  → Cue Trevor
  → Update trust status
  → Show continues
```

---

## Managers, Not Detectors

Show Runner prefers operational managers over diagnostic detectors.

Potential repositories may include:

- `certificate-manager`
- `renewal-manager`
- `trust-manager`
- `provisioning-manager`
- `revocation-manager`
- `policy-manager`
- `stage-monitor`
- `stage-console`
- `show-control`
- `productions`
- `characters`
- `systems`
- `scripts`
- `cues`
- `backstage`

A detector says:

> Something may be wrong.

A manager says:

> I will keep this part of the show continuously healthy.

That aligns Show Runner with reconciliation loops used by Kubernetes controllers, cert-manager, Crossplane, and modern platform engineering systems.

---

## Relationship to the Open Engineering Platform

Show Runner is intended to fit into the broader Open Engineering Platform ecosystem.

It introduces and exercises a key architectural idea:

> **Production is the runtime counterpart to Story.**

A Story explains what happened.

A Production manages what is happening.

This distinction may become useful beyond Show Runner itself:

- PixStars performances are productions.
- PKIStars demonstrations are productions.
- Code Smell Detective investigations can be run as productions.
- Platform automation can be modeled as productions.
- Live engineering operations can be controlled as productions.

Show Runner therefore helps define an Operations Kernel alongside the Investigation Kernel.

```text
Investigation Kernel
Observe → Investigate → Collect Evidence → Correlate → Explain → Report

Operations Kernel
Observe → Compare → Plan → Execute → Monitor → Reconcile
```

---

## Guiding Principle

Show Runner exists to make digital trust understandable, operable, and resilient.

The show succeeds when:

- certificates renew before expiry,
- trust chains validate,
- keys remain protected,
- identities are admitted correctly,
- relying parties keep trusting,
- revocations are handled cleanly,
- services keep communicating,
- and the audience never sees the panic backstage.

**The show must go on.**

