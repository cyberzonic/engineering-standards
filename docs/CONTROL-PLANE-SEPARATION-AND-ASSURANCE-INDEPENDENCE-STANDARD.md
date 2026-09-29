# CyberZonic Control-Plane Separation & Assurance Independence Standard

Standard ID: CZ-ENG-CONTROL-SEPARATION-001
Date: 2026-09-29
Status: OWNER_AUTHORIZED_PENDING_INDEPENDENT_REVIEW

## Principle

CyberZonic uses specialised control domains that report into a common Mission Control experience.

A new control domain must not automatically replace an existing one.

## Required separation

- Mission Control: aggregate visibility, coordination and authorised control.
- Domain control plane: domain-specific state/reconciliation.
- Execution Fabric: work execution/remediation.
- Chronyx: durable context/evidence/provenance.
- Product Assurance & Warranty: independent release acceptance.
- Independent Security Assurance: independent security testing/retest.
- Release authority: promotion/publication decision.

## Additive integration rule

When a new capability such as CZ-MRCL is introduced:
1. preserve existing Mission Control functions;
2. expose the new domain as a first-class Mission Control view;
3. normalise state/evidence interfaces;
4. retain domain authority boundaries;
5. avoid duplicated competing "single panes of glass";
6. avoid deleting a specialist control merely because its status becomes visible centrally.

## Evidence authority

Mission Control may display a PASS only when the authoritative domain source has produced that PASS.

It may not derive PASS from absence of alerts, lack of open issues or successful implementation CI alone.

## Independent assurance rule

Implementation, UAT/Warranty, third-party security assurance and final release authority must remain distinguishable in evidence and identity.

One actor or automation may assist multiple stages, but it must not erase required independent review boundaries or claim independence where none exists.

## Fail-closed rule

If the authoritative domain cannot be resolved or evidence is stale/contradictory, Mission Control must show UNKNOWN/EVIDENCE_REQUIRED/BLOCKED rather than infer green.
