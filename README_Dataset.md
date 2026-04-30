# V16 Connected-Beacon Dataset

**OSINT // TLP:CLEAR · DATASET**

A 301-certificate × 45-field documentary census of Spain's connected V16 certification ecosystem, anchored to the DGT whitelist and built outward through corporate-register resolution, web-surface review, EU Declaration of Conformity recovery, carrier identification, and per-row evidentiary annotation.

| | |
|---|---|
| **File** | `V16_Dataset_v1.0.csv` |
| **Records** | 301 (one per active homologation on the DGT whitelist at cut-off) |
| **Fields** | 45 columns (regulatory, corporate, manufacturer, laboratory, signatory, supply-chain) |
| **Enrichment volume** | ~915,000 characters of structured per-row notes |
| **Format** | UTF-8 CSV; semicolon-delimited; double-quote text qualifier; one header row |
| **Cut-off** | Dataset cut-off 10 March 2026; certificate dates Dec 2022 – Feb 2026 |
| **Sources** | DGT V16 connected-beacon whitelist; certificate PDFs; Spanish and UK corporate registers; applicant, manufacturer, and sampled brand websites; EU Declarations of Conformity; user manuals; public laboratory and carrier documentation where recoverable |
| **Licence** | Compiled from public-record sources; published for research use under the same OSINT // TLP:CLEAR handling as the parent investigation |

Companion to **V16-INV-2026-001 — *Spain's V16: The First National Mandate for a Connected Emergency Beacon***. Primary quantitative corpus for the parent investigation and documentary basis for the Chapter 2 structural analysis, with cross-references into the corporate, forensic, carrier, and compliance findings developed elsewhere in the report.

## What this dataset is

This is a primary-source documentary intelligence product: a structured census of every active homologation on Spain's *Listado oficial de dispositivos V-16 conectados homologados*: the national whitelist of connected V16 emergency beacons published by the Dirección General de Tráfico. The DGT whitelist is the public anchor for the dataset, but not its limit: each certificate is treated as an entry point into the applicant, manufacturer, laboratory, signatory, carrier, manual, EU Declaration of Conformity, and public web-surface record around that homologation.

The dataset takes the active DGT whitelist at cut-off as its population boundary and resolves every homologation to a single row. For each row it records 45 structured fields drawn from the certificate PDF, Spanish and UK corporate registers, applicant and manufacturer web surfaces, sampled brand web surfaces, EU Declarations of Conformity, user manuals, public laboratory records, and carrier/operator references where recoverable.

It is the primary quantitative substrate on which the investigation rests. It is published as a standalone artefact because it is independently useful (see *Why this dataset exists* below).

## Why this dataset exists

The DGT publishes the whitelist as a list of certificate numbers and PDFs on a single web page. That page is the authoritative public surface, but it is not analytically tractable. A reader who wants to understand manufacturer concentration, applicant topology, laboratory and signatory concentration, carrier exposure, brand fragmentation, or the relationship between commercial brands and underlying OEM platforms must read the register certificate by certificate and then resolve each entity outward across separate public sources.

The dataset was built to perform that outward resolution systematically. Each certificate was treated as an entry point from which: applicant and manufacturer entities were cross-walked against corporate registers; public websites were identified and reviewed where they existed; user manuals, EU Declarations of Conformity, and operator references were retrieved where recoverable; and anomalies, absences, inconsistencies, and evidentiary limits were recorded in the notes fields.

The result is a structured public-record dataset of the certification ecosystem around the whitelist: the regulator's list supplies the population boundary, while the enrichment fields document what could be established through open sources about the entities, documents, websites, and supplementary evidence attached to each homologation.

## Headline structure of the population

These figures are the population-level reading made possible by the dataset's enrichment layers. Each aggregate is independently verifiable from the structured fields, while per-row provenance, website observations, documentary absences, and evidentiary limits live in the notes fields.

### Volume and timing

| Dimension | Value |
|---|---|
| Active certificates (corpus size) | 301 |
| Earliest certificate | 22 December 2022 |
| Most recent certificate | 25 February 2026 |
| Issued in 2025 | 220 (≈73%) — a regulatory-deadline curve |
| Issued in 2026 (to cut-off) | 27 |

### Laboratory split

| Laboratory | Certificates |
|---|---|
| IDIADA | 235 (78%) |
| LCOE | 66 (22%) |

The 78/22 split was administratively created by a 2022 DGT *Directriz* (developed at Chapter 2 §2.6 of the parent investigation).

### Manufacturer geography

| Region | Approximate share |
|---|---|
| Chinese manufacturers | ≈88% (264 of 301) |
| Spanish manufacturers | ≈11% (33 of 301) |
| Other / unattributed | ≈1% (4 of 301) |

Top four Chinese manufacturers — Ningbo Chakesi, Yuyao Jiming, Ningbo Yinzhou Wilton, Ningbo Tianqi — account for 179 of the 301 certificates (59.5%), all in the Zhejiang corridor.

### Applicant topology

| Applicant of record | Certificates · share |
|---|---|
| Limburg Technology Limited (UK) | 104 · 34.6% |
| Ledel Solutions Co., LTD (UK) | 33 · 11.0% |
| Premier Auto Accessory SL (ES) | 32 · 10.6% |
| Mirovi, S.L. (ES) | 12 · 4.0% |
| JBM Campllong S.L. (ES) | 7 · 2.3% |
| …distinct applicants overall | 57 |

Three of the applicants — Limburg, Ledel, and Finder V16 Solution Limited (1 certificate, included on structural grounds) — are UK private limited companies filing dormant accounts under section 480 of the Companies Act 2006. Together they hold 138 of 301 certificates (45.8%). This is the structural basis of Chapter 4 of the parent investigation (the dormant-applicant pattern).

### Brand fragmentation

| Dimension | Value |
|---|---|
| Distinct commercial brand strings | 211 |
| Distinct model strings | 103 |
| Largest brand by certificate count | 7 (multiple brands tie) |

Brand fragmentation is downstream of manufacturer concentration: a small number of OEM platforms surface under many commercial brands. The 211 brand strings are a marketing surface, not a count of distinct hardware lines.

### Signatory surface

| Role | Distinct names · note |
|---|---|
| IDIADA — performed by | 1 (Joan Fonts Sala) · all 235 IDIADA certificates |
| IDIADA — revised by | 1 (Ramon Santafè Guiu) · all 235 IDIADA certificates |
| LCOE — performed by | 1 (José Manuel Díaz Martín) · all 66 LCOE certificates |
| LCOE — revised by | 1 (Javier Fadrique López) · all 66 LCOE certificates |

Four named individuals sign every certificate in the corpus. This is the quantitative substrate of the structural-narrowness finding (KJ-A in the parent investigation).

### Carrier landscape

| Carrier | Recoverable references |
|---|---|
| Telefónica (incl. estimated/variant strings) | ≈59 of 74 certificates with recoverable carrier |
| Vodafone | ≈8 |
| Orange | ≈5 |
| Multi-operator | 1 |

The recoverable carrier landscape is Telefónica-dominant. Most rows do not record an operator: carrier identification depends on verifiable documentation being accessible within reasonable search across the public record, which is not the case for every product.

## Schema

Each row is one homologation. Fields are grouped into seven blocks: row identification, certificate, brand, applicant, manufacturer, laboratory, and supplementary documentation. The schema is designed to preserve both the regulator's certificate record and the outward public-record resolution performed around each certificate.

**VOID convention.** Throughout this dataset, `VOID` in a structured field indicates that the field is not populated. This covers two distinct situations that are not separately coded in the structured column: (a) the information was sought in reasonable search and not located; and (b) the field is not applicable to the row. Where the reason for absence is analytically significant, it is recorded in the corresponding notes field for that row.

### Row identification and certificate

| Field | Type | Description |
|---|---|---|
| `row_id` | integer | Sequential row identifier within the dataset (1–301). |
| `cert_date` | date (Spanish) | Date of the homologation certificate as printed on the PDF (Spanish format, e.g., "22 diciembre 2022"). |
| `cert_number` | text | Certificate identifier as issued. IDIADA format: "PC" + YY + MM + 4-digit serial (e.g., `PC25100380`). LCOE format: YYYY + MM + 4-digit serial + "Gn" (e.g., `LCOE 2022110790G1`). |
| `model` | text | Model designation as printed on the certificate. |
| `commercial_brand` | text | Commercial brand under which the device is marketed (often distinct from the registered trademark holder). |

### Brand block

| Field | Type | Description |
|---|---|---|
| `brand` | text | Trademark holder or registered brand entity. |
| `brand_CIF` | text | Spanish corporate identifier (CIF/NIF) of the brand entity, where identifiable. |
| `brand_address` | text | Registered address of the brand entity. |
| `brand_incorporation_date` | date | Brand entity incorporation date as recorded in the relevant register. |
| `brand_incorporation_name` | text | Original name of the brand entity at incorporation, where this differs from the current name. |
| `brand_activity` | text | Declared CNAE economic-activity code and description for the brand entity. |
| `brand_notes` | text | Free-form annotation on the brand entity, including website findings where sampled, product-page observations, public documentation links, brand/certificate mapping issues, and anomalies. |

### Applicant block (*solicitante*)

The *solicitante* is the applicant of record on the certificate: the legal entity that requested the homologation and is named on the certificate's first page. Under the EU Radio Equipment Directive 2014/53/EU framework, the applicant of record is normally the manufacturer or the authorised representative; the analytic treatment of the applicant–manufacturer relationship in this corpus is developed in Chapter 4 of the parent investigation.

| Field | Type | Description |
|---|---|---|
| `solicitante` | text | Applicant of record as named on the certificate. |
| `solicitante_CIF` | text | Spanish CIF/NIF (or UK Companies House number where the applicant is UK-incorporated). |
| `solicitante_address` | text | Registered address of the applicant of record. |
| `solicitante_incorporation_date` | date | Applicant incorporation date. |
| `solicitante_activity` | text | Declared economic-activity code (CNAE for Spanish entities; SIC for UK entities). |
| `solicitante_notes` | text | Free-form annotation including applicant website findings, corporate-register observations, public documentation located or not located, applicant–manufacturer relationship notes, and cross-references to the parent investigation. |

### Manufacturer block (*fabricante*)

| Field | Type | Description |
|---|---|---|
| `fabricante` | text | Manufacturer named on the certificate. |
| `fabricante_CIF` | text | Manufacturer corporate identifier where applicable (predominantly empty for Chinese manufacturers). |
| `fabricante_address` | text | Manufacturer registered address. |
| `fabricante_incorporation_date` | date | Manufacturer incorporation date where recoverable. |
| `fabricante_activity` | text | Declared economic-activity code where recoverable. |
| `fabricante_notes` | text | Free-form annotation including manufacturer website findings where available, supply-chain observations, OEM cross-references, public corporate baseline notes, and documentation gaps. |

### Laboratory block

| Field | Type | Description |
|---|---|---|
| `testing_lab` | text | Testing laboratory: IDIADA or LCOE. |
| `lab_CIF` | text | Laboratory corporate identifier (`A43581610` for IDIADA; `G80455231` for F2I2/LCOE). |
| `lab_address` | text | Laboratory registered address. |
| `lab_incorporation_date` | date | Laboratory incorporation date. |
| `lab_incorporation_name` | text | Original name of the laboratory entity at incorporation, where applicable. |
| `lab_activity` | text | Declared CNAE economic-activity code. |
| `lab_notes` | text | Free-form annotation including institutional designation, accreditation scopes, and notified-body status. |

### Signatory and certificate-handling block

| Field | Type | Description |
|---|---|---|
| `performed_by_person` | text | Name of the technician who performed the testing (printed on the certificate). |
| `performed_by_role` | text | Role of the performing technician. |
| `revised_by_person` | text | Name of the technician who reviewed and signed the certificate. |
| `revised_by_role` | text | Role of the reviewing technician. |
| `signature_date` | date | Date of certificate signature (where this differs from `cert_date`). |
| `cert_notes` | text | Free-form annotation including discrepancies between the date printed on the PDF and the date displayed on the DGT public registry. Value `VOID` where no anomaly was observed. |
| `extension_info` | text | Indicates whether the certificate has been extended/amended (*extensión*), with the substantive nature of the change. Value `NO` where no extension is recorded. |

### Supplementary documentation

| Field | Type | Description |
|---|---|---|
| `cert_url` | URL | Direct URL to the certificate PDF as published by the DGT. |
| `eu_DoC` | text | Whether an EU Declaration of Conformity was located in collection. Value `VOID` where the field has been actively walked and no DoC was located. Per-row notes carry the provenance where the reason is analytically significant. |
| `eu_DoC_URL` | URL | URL to the EU Declaration of Conformity, where retrieved. |
| `manual_URL` | URL | URL to the user manual, where retrieved. |
| `manual_notes` | text | Free-form annotation on manual provenance, retrieval source, certificate consistency, operator references, product-variant ambiguity, and documentation limitations. |
| `operadora` | text | Carrier/operator identified for the device, where recoverable. Value `VOID` where the field has been actively walked and no operator information was located. A "(est.)" suffix flags an estimated attribution. |
| `operadora_notes` | text | Free-form annotation on operator provenance, including whether the carrier reference derives from a manual, applicant/manufacturer website, product documentation, indirect inference, or other public source. |

## How each row was built

Each row is the result of a certificate-anchored public-record walk consisting of, in sequence:

- Indexed retrieval of the source certificate PDF from the DGT public surface, with the certificate treated as the baseline record for the homologation.
- Field-level extraction of certificate metadata (number, date, model, applicant, manufacturer, laboratory, signatories) from the PDF.
- Cross-walk to the relevant corporate register: BORME and Spanish corporate-registry baselines for Spanish entities; UK Companies House for UK entities; other public registers where applicable.
- Cross-walk to the applicant, manufacturer, and sampled brand baseline, including registered address, declared activity, public corporate identifiers, and web surface where recoverable from the open record.
- Retrieval of EU Declarations of Conformity, user manuals, product pages, and operator information.
- Annotation in the relevant notes field of website findings, documentation gaps, anomalies, cross-references, product-variant issues, operator provenance, and supporting evidence encountered during collection.

## Known limitations

The dataset is a documentary census of the public record at a specific moment. The following limitations are inherent to that scope and should guide use:

- **Cut-off discipline.** The dataset is fixed to 10 March 2026. The DGT whitelist is a live register and the live version will diverge from this snapshot over time.
- **Public-record only.** Every cell in the dataset is derived from public-record or publicly accessible web material. No invoice data, banking record, market-surveillance correspondence, judicial filing, confidential communication, or classified material was used.
- **Operator coverage.** The operator field is populated where verifiable carrier information could be recovered within reasonable search across the public record.
- **Website coverage is asymmetric by design.** Applicant and manufacturer web surfaces were walked systematically where identifiable. Brand web surfaces were reviewed on a sampled and relevance-driven basis considering certificate visibility, product documentation, public claims, manuals, DoCs, or marketplace anomalies. Absence of a brand note should not be read as proof that no public-facing brand material exists.
- **Encoding and free-form fields.** Notes fields contain unstructured prose. The file is delivered in UTF-8 and uses semicolon as the field delimiter to accommodate the natural-language commas in the prose fields.
- **Withdrawn certificates.** The dataset is scoped to the active whitelist (the DGT *vigente* listing) at cut-off. The nine certificates revoked in Q1 2026 (the January and March waves treated at Chapter 7 §7.4 of the parent investigation) sit in the DGT *vigencia finalizada* listing and are not included as active rows in this corpus.
- **No personal data.** The dataset does not contain Spanish DNI fields. Where a DNI may have appeared in a working-file artefact during compilation, it has been omitted under the policy at Appendix A §A.7 of the parent investigation.

## Use and citation

The dataset is published as a research artefact under the same OSINT // TLP:CLEAR handling as the parent investigation. It may be redistributed, queried, joined with other public datasets, and used for further analytic work. Three requests of any downstream user:

- **Cite the source.**
- **Preserve the cut-off.** Always state the dataset version and cut-off date when reporting figures derived from it; the live DGT whitelist will diverge.
- **Read the notes.** The notes fields carry per-row provenance, website observations, documentation gaps, variant issues, and evidentiary qualifications without which the structured columns can mislead. Numerical aggregates derived without reading the notes will misrepresent the corpus.

## Companion report

This dataset is the primary quantitative substrate of this investigation. The report develops the structural reading built from this corpus and joins it to three further evidence streams: three forensic sub-corpora totalling 27 documents (six-file test-report, four-document ancillary, 17-document Declarations of Conformity), a seven-app mobile corpus, and the three-company UK Companies House set. Readers using the dataset for substantive analytic work are encouraged to consult the parent investigation, particularly Chapter 2 (the structural reading of the dataset) and Appendix A (the methodology, including source grading, confidence framing, and the intelligence-gaps register).

## Legal posture

The dataset records what the public record and publicly accessible web surface showed at collection. No row is intended as a characterisation of any party. Website findings, documentation gaps, and anomalies recorded in the notes fields are observations of the public record, not allegations against any party. Legal or regulatory characterisation, where it arises, is a matter for the competent administrative or judicial authority.

Any party named is invited to submit a written correction to **belinda.alvarez.research@protonmail.com**. Substantiated corrections will be incorporated into the next versioned release of the dataset, with attribution and dating. The legal framework under which the dataset is published is set out at Appendix A §A.9 of the parent investigation.

---

**File:** `V16_Dataset_v1.0.csv`
**Companion to:** V16-INV-2026-001 · v1.0-public · 31 March 2026
**Corrections:** belinda.alvarez.research@protonmail.com
**Handling:** OSINT // TLP:CLEAR
