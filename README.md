# Cloud Foundations Masterclass ☁️

**Beyond the basics: from cloud adoption frameworks to an end-to-end healthcare enterprise architecture.**

This repository explains what cloud foundations and landing zones are, why enterprises need them, how the major cloud providers approach them, and how those foundations support a real-world-style enterprise design.

> **Case-study notice:** The healthcare software provider used throughout this repository is entirely hypothetical. The architecture is an educational target-state reference, not a representation of any real company's internal systems or a production-certified solution.

## The four cloud platforms

| Platform | Adoption framework | Landing-zone / foundation approach |
|---|---|---|
| Microsoft Azure | Cloud Adoption Framework (CAF) | Azure Landing Zones |
| Amazon Web Services | AWS CAF | AWS Control Tower + Landing Zone Accelerator (LZA) |
| Google Cloud | Google Cloud adoption guidance | Enterprise Foundations + Cloud Foundation Fabric FAST |
| Oracle Cloud Infrastructure | OCI CAF | OCI Core Landing Zone |

## The practical enterprise example

The masterclass applies the cloud foundations to a hypothetical global healthcare software provider that builds and operates a multi-tenant Electronic Health Record (EHR) platform for hospitals.

The end-to-end design covers:

- Corporate enterprise architecture: Workday HR, IGA, Microsoft Entra ID, optional Active Directory Domain Services and SAP S/4HANA.
- Hospital clinician identity federation and separate patient CIAM.
- Shared SaaS control plane and tenant-isolated clinical data plane.
- EHR application services, FHIR APIs, patient identity / MPI integration and clinical data stores.
- Hospital integration with LIS, RIS / PACS, pharmacy, HIE and partner systems using HL7 v2, FHIR, DICOM and DICOMweb.
- Network zones, hybrid connectivity, DNS, ingress / egress and segmentation.
- Security, privacy, data governance, clinical safety and audit.
- Terraform / infrastructure automation, DevSecOps and policy as code.
- SRE, observability, backup, disaster recovery, high availability and FinOps.
- TOGAF ADM, ArchiMate-aligned viewpoints, architecture decisions, delivery roadmap and production-readiness gates.

**Important architecture boundary:** Workday, identity services and SAP support the provider's corporate operations. They are not a linear application chain and do not become the clinical transaction path. Hospital identity authenticates clinicians; the EHR handles clinical workflows; patient identity is separate.

## Start with the complete case study

👉 **[End-to-End Healthcare Software Enterprise — Reference Architecture](docs/healthcare-enterprise-reference-architecture.md)**

This is the central practical example: business capabilities, system-of-record boundaries, architecture planes, user journeys, integration catalogue, data, network, security, implementation, operations and production gates.

## Learning path

1. Understand cloud foundations, landing zones and the framework stack.
2. Compare Azure, AWS, Google Cloud and OCI foundation patterns.
3. Study the end-to-end healthcare enterprise case study.
4. Map the architecture to TOGAF ADM and ArchiMate viewpoints.
5. Turn the target design into a provider-specific implementation backlog.
6. Add tested Terraform modules, diagrams, ADRs and deployment walkthroughs as the repository evolves.

## Repository contents

- `docs/healthcare-enterprise-reference-architecture.md` — complete enterprise case-study blueprint.
- `LINKEDIN-POST.md` — launch post ready to copy and paste.
- Provider-specific learning modules and implementation examples will be expanded as they are validated.

## Scope and quality statement

This is an independent educational project. It is not vendor-endorsed, a certification guide, a compliance attestation, or a claim that generic architecture is production-ready. Cloud services and provider guidance change; verify current official documentation. Any real deployment requires customer-specific architecture, security, privacy, legal, clinical safety, capacity, resilience and operational validation.

**Repository:** https://github.com/tripathies/cloud-foundations-masterclass
