# Antech Diagnostics (antech-diagnostics)

Antech Diagnostics operates North America's largest veterinary reference laboratory network, alongside in-house diagnostic instruments and consumables, veterinary imaging, expert medical consulting, and the HealthTracks diagnostics platform. Antech is part of **Mars Petcare** (Mars Veterinary Health), which acquired Antech through Mars' 2017 purchase of VCA, Inc., where Antech was VCA's reference laboratory subsidiary. Mars has since expanded the diagnostics group with Heska, SYNLAB Vet, Cerba Vet / ANTAGENE, and VetZ.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/antech-diagnostics/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/antech-diagnostics/refs/heads/main/apis.yml)

## Access Model — Partner-Gated, No Public Developer Portal

Antech does **not** publish a public, self-serve developer portal or API reference. Its programmatic surface is a **partner-gated laboratory integration** — commonly configured inside veterinary practice information management systems (PIMS) as **"Antech V3"** — that lets veterinary software submit lab requisitions to Antech and receive results back into the patient's medical record.

- **Who uses it:** PIMS vendors such as Vetspire, Cornerstone, DaySmart Vet, NaVetor, ezyVet, and NectarVet integrate against it under partner agreements.
- **Authentication:** A practice enables the integration inside its PIMS using an Antech **Account Number**, **Username**, **Password**, and **Clinic ID** (found in the Antech portal under Account Settings > Clinic Profile > Clinic ID).
- **Flow:** The PIMS submits a requisition; the order shows as *In Progress* in the Antech online portal; once samples are processed, results (including MIC and S/I/R interpretations for microbiology) are pushed back automatically.
- **No published endpoints:** Antech discloses no base URL, endpoint paths, protocol details, schemas, or OpenAPI document publicly. Access is arranged through Antech business development / partner channels.

Because of this, the APIs below are **logical groupings modeled from documented PIMS integration behavior**, not from an Antech-published specification. No `openapi/`, `plans/`, `rate-limits/`, `finops/`, or `collections/` artifacts were fabricated.

## Tags

- Veterinary
- Diagnostics
- Laboratory
- Reference Lab
- Lab Results
- Animal Health
- PIMS Integration
- Mars Petcare

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs (Modeled)

### Antech Lab Orders API

Modeled partner-gated surface for submitting laboratory requisitions (test orders) electronically to Antech's reference lab from a veterinary PIMS. Carries the ordering clinic, patient, and requested test codes/panels.

- **Human URL:** [https://www.antechdiagnostics.com/reference-lab/healthtracks/](https://www.antechdiagnostics.com/reference-lab/healthtracks/)

### Antech Lab Results API

Modeled partner-gated surface for delivering completed diagnostic results back to the ordering PIMS, where they land in the patient's medical record — analyte values, reference ranges, and microbiology MIC / S/I/R interpretations.

- **Human URL:** [https://www.antechdiagnostics.com/reference-lab/healthtracks/](https://www.antechdiagnostics.com/reference-lab/healthtracks/)

### Antech Patients API

Modeled patient and client demographic exchange that accompanies a requisition — species, breed, sex, and owner details linked from the PIMS so results map back to the correct animal record.

- **Human URL:** [https://www.antechdiagnostics.com/reference-lab/healthtracks/](https://www.antechdiagnostics.com/reference-lab/healthtracks/)

### Antech Reference Data & Test Catalog API

Modeled reference surface exposing Antech's test catalog — test codes, panels, and species/breed reference data — so a PIMS can map its inventory items to the correct Antech tests.

- **Human URL:** [https://www.antechdiagnostics.com/reference-lab/](https://www.antechdiagnostics.com/reference-lab/)

## Common Properties

- [Website](https://www.antechdiagnostics.com/)
- [LinkedIn](https://www.linkedin.com/company/antech-diagnostics)
- [Portal](https://online.antechdiagnostics.com/)
- [Documentation](https://www.antechdiagnostics.com/reference-lab/healthtracks/)
- [Support](https://antechonlinesupport.freshdesk.com/support/solutions)
- [Parent — Mars Petcare](https://www.mars.com/made-by-mars/petcare)

## Pricing

No public, self-serve pricing. Diagnostic testing is billed per test/panel via the clinic's Antech account; integration access is arranged through Antech business development / partner channels (contact-sales). No published plans or rate-limit tiers exist to catalog.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
