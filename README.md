# GiFo-RFC-0140 (V1.2.1)

G-AGT Integration Profile - Combined Credential- and Platform-bound Enforcement (CCPE)

New Request for Comments of Gimel Foundation (GiFo RFC) - Establishung G-AGT Integration Profile - Combined Credential- and Platform-bound Enforcement (CCPE)

Abstract of RFC: Today, there are many attempts to govern AI through new toolkits and solutions. Many of 
these represent a platform-bound enforcement of policies, initiated by hooks. These
attempts, though, are not necessarily sufficient to meet cybersecurity requirements and
regulations like the EU AI Act amongst others, which requires to ensure that AI systems
developed or used within the EU are safe, trustworthy, and under control (see also GiFo-
RFC 0130). Next to a platform bound-enforcement of policies, it requires a credential-
bound enforcement of the specific authority an AI system is supposed to have to act,
decide and enter transactions. To integrate both, this is what this Request for Comment
0140 is about.

This document specifies CCPE-A, the first profile in the Combined Credential- and Platform-Bound 
Enforcement (CCPE) family: GAuth's credential-bound enforcement (Phase 1) chained to an enterprise 
governance toolkit (AGT-class engine) as the platform-bound Phase 2 evaluator. The sibling profile 
for standalone Policy-as-Code engines is published as GiFo-RFC 0150 (CCPE-B).

The G-AGT integration profile defines how a typical Agent Governance Toolkit (AGT) -
exemplified by Microsoft's AGT and informed by publicly available operational
governance solutions - integrates with the GAuth authorization architecture (GiFo-RFCs
0110, 0111, 0115, 0116, 0117, and 0118). G-AGT specifies two integration scenarios and
acknowledges a dynamic third:

- Scenario “AGT Engine”: AGT serves as an access control vehicle within GAuth's
PEP extension point - analogous to how an OAuth engine (e.g., Ory Hydra) serves
as the authorization vehicle in GAuth's Type A adapter slot.
- Scenario “AGT Bridge”: Full AGT runs standalone with its native capabilities
active (policy evaluation, execution rings, trust scoring, kill switch, circuit
breakers). AGT calls into GAuth's PEP for credential-bound delegation
enforcement decisions.
- “Dynamic” Scenario: In a dynamic future, AGT implementations (or successors)
could integrate the full GAuth specification suite (RFCs 0110-0118). 

Under all scenarios, the GAuth PEP (Policy Enforcement Point) remains the authoritative
governance control plane. G-AGT positions GAuth as the authority and policy layer that
AGT's runtime hooks call into.

This specification excludes AI-enabled governance, web3 integration as well as
DNA_based identities and PQC associated, consistently with all other GiFo-RFCs. All
trust scoring, policy evaluation, and governance functions defined herein are
deterministic and rule-based. AI/ML-enhanced governance capabilities are available
exclusively through proprietary Type C adapters (Slot 5) under separate license.

You are more than welcome to contribute !

Legal Provisions for users of this page

Please see the Legal Provisions under https://gimelfoundation.com

In particular the following terms apply:

GiFo RFC 0080 Legal Provisions for the Gimel Foundation

GiFo RFC 0090 Legal Provisions Related to Gimel Foundation Documents

GiFo RCC 0100 Rights Contributors Provide to the Gimel Foundation
