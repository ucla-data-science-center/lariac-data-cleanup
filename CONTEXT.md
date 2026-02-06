# LARIAC Data Collections Cleanup - Context

## Background
The LARIAC data collections grew into an "accidental architecture" during the COVID-19 pandemic. Access paths are currently fragmented across UCLA Dataverse, Google Drive (including personal drives), StoryMaps, and LibGuides. This project aims to collapse this into an intentional, minimal, and survivable architecture.

## Strategy: Dataverse-as-the-Sole Entry Point
The core strategy is to treat UCLA Dataverse as the **access controller and authoritative index**, rather than the primary storage system for large assets.

### The Model
*   **Dataverse datasets**: Act as contracts, gates, and metadata containers.
*   **Google Drive (Single Shared Drive)**: Serves as the authoritative storage backend.
*   **Legacy Assets**: To be migrated to the shared drive or decommissioned.

### Why Dataverse?
*   **Persistent & Auditable**: Provides a stable entry point with clear access logs.
*   **Authentication**: Leverages institutional and guest authentication.
*   **Licensing**: Manages data use agreements and click-through conditions effectively.

## Proposed Architecture

### 1. Unified Landing Point
The **LARIAC Dataverse** should be the only public-facing landing point.

### 2. Structure by Release
Organize via sub-dataverses for clarity (e.g., LARIAC 4, 5, 6, 7). This allows for version-specific metadata and easy deprecation.

### 3. Datasets as Access Gates
Datasets represent coherent access units (e.g., "LARIAC 7 Orthogonal Imagery") but contain **External Data Access links** to Google Drive instead of the large files themselves.

## Storage Principles
*   **Zero tolerance for personal Drive links** (e.g., `My Drive`).
*   **Single Authorized Shared Drive**: All Dataverse links must point to a specific, managed Shared Drive (e.g., `geospatial/LARIAC/`).
*   **Cleanup**: Anything not referenced in Dataverse is considered legacy/candidate for deletion.

## Role of the StoryMap
The StoryMap transitions from an access tool to an **orientation and discovery** tool. It should link to Dataverse dataset pages rather than directly to Google Drive.

## Expected Benefits
*   **Single Audit Surface**: One place to verify links, licenses, and authentication.
*   **Consistency**: Unified access control.
*   **Sustainability**: Clear path for future staff and easier handoff.
