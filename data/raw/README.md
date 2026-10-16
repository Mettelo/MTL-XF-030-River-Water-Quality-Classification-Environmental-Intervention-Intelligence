# MTL-XF-030 — Raw source snapshots

**State:** no raw data uploaded by this build.

Use the agreed Environment Agency England classifications.csv and measures.csv endpoints. They are mutable exports: freeze both at one recorded retrieval timestamp before team analysis. Filter to England river water bodies using actual type codes; include other water-body types only as separately labelled context. Compare classification years/cycles only when methodologically compatible. No raw Water Quality Explorer observations are required.

The exact agreed inputs are listed in [the source register](../SOURCE_REGISTER.md). This folder is reserved for original publisher bytes only after controlled acquisition and permission under verified reuse terms. Never place cleaned extracts, manually corrected files or dashboard exports here.

For every approved snapshot, retain source ID, original/resolved URL, retrieval UTC, publisher version, original filename, byte size and SHA-256 in metadata. Preserve archived member names and sheet structure. Use versioned paths rather than overwriting a snapshot. Validate expected file type and schema before ingestion; retain failures in an acquisition log.

The Data Governance Analyst controls freeze approval; the Data Engineer verifies checksums on each run. If redistribution is restricted, preserve the manifest and authorised retrieval instructions in the approved location rather than uploading prohibited bytes. Do not add data merely to make the repository look populated.
