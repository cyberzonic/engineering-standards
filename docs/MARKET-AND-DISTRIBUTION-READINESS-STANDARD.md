# CyberZonic Market & Distribution Readiness Standard

Standard ID: CZ-ENG-MRCL-001
Date: 2026-09-29
Status: OWNER_AUTHORIZED_PENDING_INDEPENDENT_REVIEW

## Purpose

A passing build is not sufficient evidence for market readiness.

## Mandatory controls

M1 Corporate truth — public products must link to authoritative current CyberZonic corporate/legal/contact/support/privacy/security information.

M2 Canonical product identity — every release surface must resolve to the same governed product/suite identity while permitting platform-specific IDs and build numbers.

M3 Corporate Footprint Manifest — every commercial product must maintain governed identity, URL, publisher, store, signing, support, social and release references. Unknown values must be explicit.

M4 Brand asset authority — marketplace/store/social/application assets must come from approved sources. Teams must not recreate master/product marks or improvise names.

M5 Platform publisher ownership — external publisher/developer accounts must be organisation-governed, least-privilege, recoverable and protected by MFA.

M6 Package and signing identity — every binary/package release must identify suite version, source SHA, package/bundle ID, platform version/build, artefact hash, signing/notarisation identity and distribution channel.

M7 Release-candidate parity — UAT, Warranty, security assurance and store submission must test the same candidate or have explicit reviewed equivalence proof.

M8 UAT independence — implementation teams may supply evidence but cannot solely certify final UAT/Warranty acceptance.

M9 Independent security assurance — where third-party testing is required, assessor independence and exact scope/build/environment are mandatory; material findings need remediation/retest or authorised residual-risk acceptance.

M10 Public metadata consistency — product name, publisher, logos, screenshots, pricing labels, privacy/support URLs, company information and claims must be consistent across corporate site, product site, docs, stores, social channels and installers.

M11 Legal/privacy/data declarations — required terms, licensing/EULA, privacy, data-use, security/support policies and store data declarations must match actual behaviour.

M12 Store-preview lifecycle — applicable preview/private/test channels must exercise install/purchase/activation/update/suspension/cancellation/uninstall or equivalent before public publication.

M13 Marketing launch gate — marketing/social launch must not precede availability/support readiness in a way that creates unsupported claims.

M14 Post-launch continuity — every public product must have monitoring, support, vulnerability intake, incident response, updates, rollback/revocation and public-information drift controls.

M15 Sanity reconciliation — CZ-MRCL must fail a launch gate when evidence across repositories/channels disagrees even if each subsystem is locally green.

## Platform coverage

Includes Microsoft Marketplace, Apple App Store/TestFlight/notarised macOS, Google Play, Chrome Web Store, Edge Add-ons, Mozilla AMO, cloud marketplaces, direct download, package repositories, enterprise/private distribution and future channels.

## Scope rule

A product may launch on a subset of surfaces only when excluded surfaces are explicit and public marketing/support claims match the declared launch scope.

A product is market ready only for the scope for which all mandatory CZ-MRCL gates have evidence.
