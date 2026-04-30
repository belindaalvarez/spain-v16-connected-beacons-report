# Spain's V16: The First National Mandate for a Connected Emergency Beacon

*An OSINT investigation of the V16 ecosystem's regulation, certification, supply chains, cybersecurity, public discourse, and enforcement environment.*

**OSINT // TLP:CLEAR**

| | |
|---|---|
| **Document ID** | V16-INV-2026-001 · v1.0-public |
| **Author** | Belinda Álvarez, PhD · Independent Researcher |
| **Collection close** | 31 March 2026 (dataset cut-off 10 March 2026) |
| **Length** | 159 pages · 8 chapters · 8 appendices · 54 exhibits · 11 documented intelligence gaps |
| **Handling** | OSINT // TLP:CLEAR · public distribution |
| **Corrections** | belinda.alvarez.research@protonmail.com (right of reply open-ended) |

## About this investigation

From 1 January 2026, Spanish road law requires approximately 28 million drivers to carry a connected V16 emergency beacon that transmits its activation to the Dirección General de Tráfico's DGT 3.0 traffic-information platform. It is the first national mandate of its kind globally.

This document is a primary-source documentary investigation of that regime. It assembles four corpora: 1) A 301-certificate × 45-field documentary census of the DGT connected-V16 whitelist, manually extended through corporate-register resolution, public web-surface review, manual and EU Declaration of Conformity recovery, carrier references, and per-row evidentiary notes; 2) Three forensic sub-corpora totalling 27 documents (six-file test-report, four-document ancillary, seventeen-document Declarations of Conformity) covered in Chapter 3; 3) A seven-app mobile corpus (Chapter 6); 4) The three-company UK Companies House set underpinning Chapter 4. The report reads each against the EU and Spanish legal framework that governs it. No classified, confidential, or non-public material is used at any point.

The investigation finds that Spain's connected V16 ecosystem is structurally narrow on every major dimension, from manufacturer concentration through a two-laboratory structure to a four-name signatory surface and a single institutional whitelist. It also rests on a certification regime in which 45.8 per cent of admitted devices are registered to three UK private limited companies filing dormant accounts at Companies House. The mandate itself is exposed on two independent EU-law tracks, including a procedural non-notification finding confirmed on the European Parliament record by Commission Executive Vice-President Séjourné on 19 February 2026 that engages the binding *CIA Security International* disapplication remedy. The overall domestic architecture is coherent and judicially corrected. None of these vulnerabilities has been tested in litigation as of the collection close.

## Four key judgements

All findings are stated as documentary facts about the public record. No individual or entity is characterised as having engaged in wrongdoing; legal or regulatory characterisation, where it arises, is a matter for the competent administrative or judicial authority.

**KJ-A. Structural narrowness as accumulation.** 73 per cent of all 301 certificates were issued in 2025, on a regulatory-deadline curve prior to the 1 August 2025 entry into force of RED Article 3(3)(d/e/f) cybersecurity requirements. Four Chinese manufacturers in a single Zhejiang corridor account for 59.5 per cent of devices. The 78/22 IDIADA–LCOE laboratory split was administratively created by a single 2022 DGT *Directriz*. Four named individuals sign every certificate in the corpus. The analytic finding is the accumulation across these dimensions. *(High confidence.)*

**KJ-B. Dual-track EU-law exposure.** Two EU-law tracks are independently in play: substantive (Article 34 TFEU cumulative-design, noted by the Commission in conditional terms) and procedural (Directive (EU) 2015/1535 non-notification, confirmed on the European Parliament record by Séjourné, triggering the binding *CIA Security International* remedy under CJEU C-194/94). The procedural track bypasses Article 36 proportionality litigation on the merits. *(High on procedural; moderate-high on substantive.)*

**KJ-C. The dormant-applicant pattern.** Three UK private limited companies (Limburg Technology Limited, Ledel Solutions Co., LTD, Finder V16 Solution Limited), each controlled by a single non-UK-resident director under the maximal Person with Significant Control configuration and each filing dormant accounts under section 480 of the Companies Act 2006, collectively hold 138 of 301 certificates (45.8 per cent). The chapter's most evidentially significant document is a primary-source Telefónica IoT corporate connectivity service contract executed in Ledel's name during its first declared dormant year, citing UK company number 14734987 and committing the entity to a service term of "not less than 12 years." Three structural hypotheses are weighed; the open record discriminates asymmetrically in favour of the operator-deficit reading and forecloses the strictest form of the nominal-applicant reading for Ledel, but cannot resolve whether inaccurate dormant filings also hold or whether the weaker nominal-applicant reading holds across the three companies; the pattern is recorded as a documentary structure, not as an allegation. *(High on documentary structure; moderate on the discrimination problem; GAP-01 through GAP-03.)*

**KJ-D. The Spanish-domestic cybersecurity findings.** Kepar Electrónica S.L. ships two V16 lines on different hardware tiers. The FlashLED SOS runs on the STMicroelectronics STM8 8-bit microcontroller per the 17 January 2023 DGT 3.0 connection-test certificate, with no successor host-MCU declared in the open record, which is architecturally incapable of the cryptographic primitives EN 18031 requires. This constitutes an irremediable ceiling carrying into the Cyber Resilience Act horizon (Regulation (EU) 2024/2847, applicable 11 December 2027). The Help Flash IoT (~250,000-unit Vodafone-distributed field population) runs on an ESP32-class processor capable in principle of meeting EN 18031, but ships firmware that does not comply with the required controls: hard-coded shared WiFi credentials, unauthenticated HTTP firmware delivery, no firmware signature verification, no OTA activation authentication (CVE-2025-65855, Miranda Acebedo, 17 December 2025). This constitutes an implementation failure on capable hardware, technically remediable. *(High on both as documentary findings; moderate-high on field-population implications; GAP-06.)*

Each judgement is graded on the ICD 203 confidence scale and supported by individually graded evidentiary inputs at the chapter level; the per-KJ tabulation is at Appendix A §A.4.1.

## The three most analytically significant intelligence gaps

Eleven gaps are formally registered at Appendix G: nine open at collection close, two partially resolved in-investigation (GAP-04, GAP-05). The three carrying the heaviest analytic weight are surfaced here so that the limits of the open-source surface are visible alongside the four judgements.

**GAP-01 — Invoice and banking evidence on the dormant-applicant pattern.** No documentation of payment flows between laboratories, carrier companies, manufacturers, or applicants of record is on the open record. The streams that would resolve the residual question whether the named UK entities themselves incur the financial flows the applicant-of-record role implies (IDIADA invoices, Telefónica counterparty records, UK banking records across the section 480 dormancy years) are accessible only to UK Companies House compliance review, HMRC, or counterparties.

**GAP-06 — Field-population firmware status of the two Kepar Spanish-domestic device lines.** Of approximately 250,000 first-generation units sold via Vodafone as of March 2025, the current firmware state in the field (specifically whether the WiFi OTA mode underlying CVE-2025-65855 remains reachable on devices in end-user hands, and whether any remediation propagates automatically through the NB-IoT channel or requires user action) is not publicly documented. BandaAncha's confirmation of remediation covers the successor Help Flash IoT+ on Telefónica's network, not the first-generation field population. The gap also covers the FlashLED SOS line: the V01–V05 deployment chronology preceding the V06 firmware build attested in the H-33 connection-test certificate of 17 January 2023, and the post-2023 host-MCU status of any subsequent production run, are not documented on the open record.

**GAP-09 — Judicial test of the Directive (EU) 2015/1535 non-notification defence.** Commission Executive Vice-President Séjourné's written answer of 19 February 2026 (E-004992/2025(ASW)) confirmed on the European Parliament record that neither RD 159/2021 nor RD 1030/2022 was notified under the directive, and cited CJEU C-194/94 (*CIA Security International*) on the binding disapplication remedy. No Spanish *contencioso-administrativo* court has yet ruled on the defence against a V16 fine, and no Article 267 TFEU preliminary reference has been filed.

## How to read it

A reader with limited time should start with the **Executive Summary**: four key judgements, headline findings from the remaining chapters, and the three most analytically significant intelligence gaps. Each chapter then opens with a *Bottom Line Up Front* and a numbered set of key judgements; the body develops the evidence.

The reader is strongly encouraged to weight the 11 intelligence gaps registered at Appendix G, which documents what the open-source domain cannot resolve.

## Methodology

The report is conducted under structured analytic tradecraft. Evidence and analytic discipline are described in full at Appendix A; the headline elements are:

- **Source grading.** Every evidentiary input is graded under the NATO/UK Admiralty 6×6 framework (reliability A–F, credibility 1–6), tabulated per key judgement at §A.4.1.
- **Confidence framing.** Analytic judgements carry qualitative confidence grades calibrated to ICD 203 conventions.
- **Analysis of Competing Hypotheses.** Heuer's ACH framework (1999) is applied at Chapter 4 §4.3 to the dormant-applicant pattern, with three structural hypotheses tested against the documentary record.
- **Alternative-reading paragraphs.** Where a finding rests on interpretation rather than on documentary fact alone, the strongest counter-reading is stated explicitly and addressed before the reading is adopted or set aside.
- **Intelligence-gaps register.** Eleven documented gaps catalogue what open-source material cannot resolve and which evidence stream would resolve each.
- **Non-allegation framing.** No person, company, laboratory, carrier, or public body is characterised as having engaged in wrongdoing. The report records documentary structure; legal or regulatory characterisation is for the competent authority.
- **Right of reply.** Any party named is invited to submit a written correction; substantiated corrections will be incorporated into versioned releases under the same document identifier, with attribution and date.

Collection rests on four methods: indexed search against public registers; retrieval and archiving of primary documents; document forensics on PDF metadata, embedded toolchains, and signature surfaces; and dated direct outreach to named parties.

## Document structure

The report is organised in 8 chapters and 8 appendices.

### Chapters

**Chapter 1 — Legal framework and vulnerability mapping.** Domestic regulatory architecture, EU and international anchoring, the Article 34/36 TFEU exposure, the Directive (EU) 2015/1535 non-notification finding, ITS principles, the *siniestralidad* evidentiary base, and the Annex II telecommunications specification. Establishes the dual-track EU-law exposure.

**Chapter 2 — The certification regime: actors and structure.** Reads the 301-certificate × 45-field dataset for temporal dynamics, manufacturing geography, applicant topology, brand fragmentation, carrier landscape, the administrative origin of the two-laboratory structure, and the four-name signatory surface. Develops the structural-narrowness finding.

**Chapter 3 — Document forensics.** Reads three sub-corpora (six IDIADA test reports, four ancillary artefacts, and seventeen EU Declarations of Conformity) for PDF metadata, embedded toolchains, signature configurations, and standards-list discipline. Surfaces the Spanish-domestic cybersecurity findings (FlashLED SOS STM8 ceiling / Help Flash IoT ESP32-class implementation failure), the Yuyao Jiming trading-channel fan-out, the Foshan Nanhai cluster, and the contractual uniformity of the Telefónica plumbing.

**Chapter 4 — The dormant-applicant pattern.** Three UK private limited companies, the corporate-services substrate that supports them, and the corporate connectivity service contract executed in one of their names during its first declared dormant year. Heuer's ACH applied to three structural readings of the pattern.

**Chapter 5 — Two file-level irregularities.** Two cases where the documentary record is internally inconsistent at file level: IDIADA references circulating in current commerce on devices incompatible with the connected framework, and a single DGT-whitelist entry where the file the channel serves is structurally unlike any other certificate on the list.

**Chapter 6 — The data surface.** The public DGT 3.0 National Access Point and its DATEX II v3.6 SituationPublication feed (the regulation-anchored anonymous channel), and the parallel commercial app layer (five companion apps gating function behind pre-authentication DNI/vehicle/insurance collection, plus two third-party apps that consume the public feed without identity collection). Maps the dual data pipeline.

**Chapter 7 — Public ecosystem and the EU question.** Cybersecurity in public discourse, public-discourse supply-chain cases, government funding and procurement, enforcement and revocations, the EU legal position as received in Spanish public discourse, and adjacent operational concerns.

**Chapter 8 — Forward-looking assessment.** Six stress-test scenarios anchored to specific structural findings, with watching points for each. Not predictive; each scenario depends on a specific structural finding continuing to obtain.

### Appendices

**Appendix A — Methodology.** Scope, collection methods, dataset construction, source grading, per-key-judgement source-grade and confidence tabulation, framing discipline, and legal publication basis.

**Appendix B — IDIADA and LCOE institutional profiles.** Entity baselines, the 2024 Generalitat reconcession, the November 2024 Applus delisting, F2I2 governance and accounts, LCOE designation lifecycle and internal architecture.

**Appendix C — Per-document forensic dossiers.** The test-report, ancillary, and DoC sub-corpora at full forensic depth, the STM8 architectural cross-walk, OEM cross-references, and the Telefónica plumbing chronology.

**Appendix D — Dormant-applicant filings.** Per-entity Companies House chronologies and the corporate-services substrate at full per-address detail.

**Appendix E — App data surface.** Per-app profiles for the seven-app corpus.

**Appendix F — Bibliography.** Legal instruments, standards, parliamentary records, primary corporate filings, datasets, and press.

**Appendix G — Intelligence gaps register.** Eleven documented gaps with the evidence stream that would resolve each.

**Appendix H — Exhibits inventory.** Per-exhibit description and chapter cross-reference for the 54 exhibits underpinning the report.

## Repository contents

- **`README.md`** — this file.
- **`README_Dataset.md`** — provenance, scope, schema, and known limitations of the dataset.
- **`README_Investigation_v1.0.pdf`** — printable copy of this README.
- **`README_Dataset_v1.0.pdf`** — printable copy of the dataset README.
- **`Executive_Brief_v1.0.pdf`** — distils the investigation's core findings, key judgements, evidentiary base, and priority intelligence gaps.
- **`V16_Investigation_v1.0.pdf`** — the full report.
- **`V16_Dataset_v1.0.csv`** — the 301-certificate × 45-field census of the DGT V16 connected-beacon whitelist as it stood at the dataset cut-off of 10 March 2026. The quantitative substrate of this report.
- **`CHANGELOG.md`** — record of incorporated corrections and version history.
- **`LICENSE`**, **`LICENSE-DATASET`**, **`LICENSE-REPORT`** — scoped Creative Commons licensing.

## Right of reply

Any party named in this report whose factual representation they consider inaccurate is invited to submit a written correction or response to the contact address in the front matter. Substantiated corrections will be incorporated into the next versioned release under the same document identifier (V16-INV-2026-001). On request, a response of reasonable length from a directly named party will be appended verbatim to the relevant chapter, with a clear marker indicating the response is the named party's own and is published unedited. The original finding and the response will both remain on the record. This offer is open-ended for the life of the document. Substantiated correction requests will be acknowledged within 14 calendar days of receipt and given a substantive response within 30; any correction incorporated into a subsequent release will be attributed to the requesting party and dated in the *Version history*.

The legal framework under which this report is published (Spanish, EU and UK freedom-of-expression and data-protection guarantees) is set out at Appendix A §A.9.

## About the author

Belinda Álvarez is an independent researcher holding a PhD in Social Anthropology from the University of Cambridge. Her research background is in the ethnographic and documentary analysis of institutions, political actors, and informal networks. This investigation applies those methods to public registers, corporate filings, and regulatory instruments. Findings drawn from open-source intelligence are structured using NATO/UK Admiralty source grading, ICD 203 analytic-confidence framing, and structured analytic techniques. She has no commercial relationship to, and has received no funding from, any party named in this report.

## Version history

**v1.0-public** — initial publication; collection close 31 March 2026.

## License

This repository uses scoped Creative Commons licensing.

- `V16_Dataset_v1.0.csv` is licensed under CC BY 4.0. See [`LICENSE-DATASET`](LICENSE-DATASET).
- The report (`V16_Investigation_v1.0.pdf`), the Executive Brief, and the README documents are licensed under CC BY 4.0. See [`LICENSE-REPORT`](LICENSE-REPORT).
- The top-level [`LICENSE`](LICENSE) file explains the scope of the repository licensing.

The licenses apply only to material authored, compiled, structured, annotated, or analysed by Belinda Álvarez. They do not relicense any underlying third-party source material reproduced, cited, or referred to within the work products. Each such item remains subject to its own copyright and licensing regime.

---

OSINT // TLP:CLEAR · V16-INV-2026-001 · v1.0-public · 31 March 2026
