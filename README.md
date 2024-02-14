# OCP-NET-Falcon

1. License

Contributions to this Specification are made under the terms and conditions set forth in Open Web Foundation Contributor License Agreement ("OWF CLA 1.0") ("Contribution License") by:

Google

Usage of this Specification is governed by the terms and conditions set forth in the Open Web Foundation Final Specification Agreement ("OWFa 1.0").

...

4. Scope

This specification describes the Falcon transport protocol that provides reliable transport for RDMA Operations and NVMe commands.

Not in scope are:

* Details of changes in RDMA and NVMe layers in support of Falcon.
* Details of applications’ use of Falcon.
* Details of implementing Falcon in software stacks or hardware NICs.

5. Overview

This specification describes the Falcon protocol that provides reliable transport for RDMA Operations and NVMe commands. Falcon is a connection-oriented, request-response transport protocol that provides end-to-end reliable transfer and per-connection security to upper layer protocols (ULPs) such as RDMA and NVMe. A Falcon connection can either be ordered or unordered. Falcon includes a programmable congestion control engine that can be used to implement state-of-the-art congestion control algorithms. Falcon authenticates and encrypts all ULP data on a per-connection basis using the Paddywhack Security Protocol (PSP) or the IPSEC ESP protocol. The following sections describe key architectural concepts of Falcon in further detail.