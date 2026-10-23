# Vivédex Data Licensing and Provenance Policy

**Status:** Initial project policy for the prototype. Review this policy before accepting public contributions or redistributing data at scale.

Vivédex aims to make biodiversity knowledge easier to discover, verify, and reuse. To support that goal, the project must strictly respect the rights and terms attached to all datasets, photographs, recordings, research, and community contributions. 

This file defines the intended approach to data licensing for the Vivédex project. It does not replace the licenses or terms supplied by original data providers, nor does it grant Vivédex rights it does not inherently own.

## 1. The Software License is Not the Data License

The source code in this repository is licensed under the **Apache License 2.0**, as stated in the `LICENSE` file. 

This software license covers the project code, but it does **not** automatically apply to:
*   Third-party taxonomic or biodiversity datasets.
*   Photographs, illustrations, audio, or video media.
*   Papers, field guides, species descriptions, or other publications.
*   Model weights, APIs, or other external software dependencies.
*   Data submitted by Vivédex users.
*   Names, logos, and trademarks owned by other parties.

Each item or dataset must retain its own applicable license, attribution requirements, and source information.

## 2. Rules for External Biodiversity Data

Before importing, caching, transforming, displaying, exporting, or using an external dataset, Vivédex must record and verify its terms. 

For each dataset or record, retain the following information:
*   **Source name** and provider.
*   **Source URL**, record URL, or stable identifier.
*   **Dataset or release version** and retrieval date.
*   **License name and URL** exactly as supplied by the provider.
*   **Required attribution** and any specific citation instructions.
*   **Changes made** by Vivédex, such as normalization, mapping, translation, or deduplication.
*   **Restrictions or notes**, including non-commercial terms or limits on redistribution.

Never assume a record is free to reuse simply because it is accessible via a public website or API. Never replace a source data license with the Vivédex software license.

### External Source Integrations
*   **GBIF:** GBIF-mediated occurrence records typically use licenses such as CC0, CC BY, or CC BY-NC. Verify the license and attribution for the specific records used. An occurrence record's license does not necessarily cover associated media; follow the relevant media license independently.
*   **Catalogue of Life:** Content is generally offered under CC BY 4.0 unless otherwise indicated. Check the license and release metadata for specific downloads, as underlying sources may possess different terms.

## 3. Practical License Handling

Always use the provider's exact license metadata. Handle licenses according to these minimum standards:

*   **CC0:** Reuse is generally permitted without a license-based attribution requirement. Preserve provenance and cite the source as a standard scientific practice.
*   **CC BY:** Provide appropriate attribution, link to the license, and explicitly identify any changes made. Retain source details with the record.
*   **CC BY-SA:** Follow standard attribution requirements and adhere to the ShareAlike conditions before distributing adapted material. Do not assume it can be relicensed under Apache 2.0.
*   **CC BY-NC (or other non-commercial licenses):** Isolate this data from any commercial reuse pipelines. Do not redistribute or utilize it in a manner that conflicts with its non-commercial condition.
*   **CC BY-ND (or other no-derivatives terms):** Do not distribute adapted versions unless explicitly permitted by the license or rightsholder. Check if the intended transformation is allowed.
*   **Unknown, missing, or unclear license:** Do not bulk-import or redistribute the material. Link to the original source or find a clearly licensed alternative.
*   **Custom terms or access restrictions:** Review the provider's terms prior to use; API access alone does not grant permission to republish data.

## 4. Photographs, Audio, and Media

Media used to support an organism's identification may hold a separate copyright and license from the associated taxonomic record. 

For each media item, record:
*   Creator or rights holder.
*   Original source URL and stable identifier.
*   Media-specific license and license URL.
*   Attribution text.
*   Whether changes were made.
*   Any known restrictions.

Do not copy images merely because they illustrate a species. Do not remove watermarks, credits, or license notices. If a media license cannot be established, link to the original page rather than copying or redistributing the file. For the prototype, strictly use self-created media, media with a verified compatible license, or explicitly permitted media.

## 5. Community Observations and User Submissions

Contributors retain ownership of all original material they submit unless they explicitly agree otherwise. Submitting material does not automatically transfer ownership to Vivédex. 

The platform must clearly state what permissions are requested and obtain affirmative consent before displaying or redistributing user contributions.

**Proposed approach for public contributions:**
*   Allow contributors to toggle observations between private and public.
*   Separate the license for structured observation data from the license for submitted media.
*   Recommend **CC BY 4.0** for public records and media when the contributor holds the necessary rights and opts in.
*   Preserve attribution and link back to the original observation during reuse.
*   Do not promise relicensing capabilities if the contributor does not own the rights.
*   Provide a mechanism to report rights concerns and request removal, subject to applicable law.

Until Vivédex establishes a working consent flow, do not present user contributions as openly licensed or redistribute them as an open dataset.

## 6. AI-Generated Identifications and Descriptions

AI-generated identifications are **candidate results**, not confirmed scientific facts. Vivédex must retain:
*   The suggested taxon and its taxonomic identifier.
*   The specific model or service used (and version).
*   Supporting source records and links.
*   Date of the generated result.
*   Uncertainty or confidence metrics exposed by the system.
*   Subsequent user or expert corrections.

Do not copy generated text wholesale from protected sources unless permitted by the relevant terms. Maintain citations near the claims they support. Do not imply that an AI suggestion is expert-verified or that a source endorses Vivédex. Review the specific terms of all models, weights, APIs, and datasets independently.

## 7. Transformations, Taxonomic Changes, and Provenance

Operations such as normalizing scientific names, mapping synonyms, or building linked knowledge graphs must never erase the source trail. 

Retain the original value alongside the normalized value, and record:
*   Source and original identifier.
*   Taxonomic reference or release used.
*   Mapping or transformation applied.
*   Date of the transformation.
*   Unresolved conflicts or uncertainty.

Do not silently overwrite historical identifications during taxonomic revisions when preserving that history is practical. Maintain a clear distinction between expert reviews and machine-generated suggestions.

## 8. Attribution Format

Display required attribution near the relevant record or provide an accessible attribution view. Follow the source's exact citation instructions when available. 

A standard attribution entry format:
> **Source:** [provider or creator] — [dataset or item title/identifier]
> **Record:** [original URL]
> **License:** [license name and URL]
> **Changes:** [none, or a brief description of changes]
> **Retrieved:** [date]

## 9. Dataset Register

Maintain a register (CSV or JSON) for every external source used in a release. 

Required fields:
`source_id, provider, dataset_title, dataset_version, source_url, record_url, license_name, license_url, attribution, changes, retrieved_at, redistribution_allowed, notes`

Store license information at both the dataset and item level if terms differ.

## 10. Reporting a Licensing Concern

Rights infringements or missing attributions should be reported via GitHub issues using the relevant source URLs and record identifiers. Do not upload private information or disclose sensitive location data in a public issue. Private concerns should be routed directly to the repository maintainers. Maintainers will restrict or remove disputed material while the rights issue is assessed.

## 11. Scope and Disclaimer

This document outlines the project's intended data-handling practices; it is not legal advice. It does not replace the specific licenses, terms of service, or permissions that apply to any source or contribution. When licensing or redistribution rights are unclear, the default policy is: **do not redistribute until clarified**.