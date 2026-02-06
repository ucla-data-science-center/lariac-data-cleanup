# Desired End State: LARIAC Data Architecture

This document defines the "Definition of Done" for the LARIAC cleanup project.

## 1. The Single Source of Truth
*   **Public Entry Point:** [UCLA Dataverse (LARIAC Collection)](https://dataverse.ucla.edu/dataverse/lariac).
*   **Storage Backend:** Google Shared Drive: `geospatial` (Shared Drive ID: `0AOD9sgqZt3sCUk9PVA`).

## 2. Dataverse Configuration (The "Gate")
*   Every LARIAC release (4, 5, 6, 7) has a corresponding Dataset in Dataverse.
*   **No large files** are uploaded to Dataverse.
*   Each Dataset contains an **External Data Access** link (using the "Link to External Data" feature or a clear URL in the metadata).
*   All links point **exclusively** to the `geospatial` Shared Drive.

## 3. Google Drive Configuration (The "Vault")
*   **Zero** public access links point to `Tim's My Drive`.
*   **Zero** public access links point to the legacy `lariac` Shared Drive.
*   The `geospatial` drive is organized by release and product type (e.g., `LARIAC7/Imagery/Orthos`).
*   Permissions are managed at the Shared Drive level, not on individual folders.

## 4. Discovery Tools (The "Map")
*   The **LARIAC StoryMap** and **LibGuides** link only to Dataverse DOIs/landing pages.
*   Direct Google Drive links are removed from all public-facing documentation.

## 5. Decommissioning
*   Legacy storage (`Tim's My Drive` LARIAC folders and the old `lariac` Shared Drive) is emptied or deleted after verification that all active links have been migrated to `geospatial`.

---
**Summary for Jamie:** We are moving from a "direct-to-drive" model to a "Dataverse-mediated" model. Your goal is to ensure Dataverse metadata is the authoritative map that points users to the right spot in the `geospatial` drive.
