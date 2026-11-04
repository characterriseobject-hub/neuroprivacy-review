# Workspace preservation status

Snapshot UTC: 2026-11-04T20:51:16.273064+00:00

This repository contains a selected private review collection. The larger local workspace has not been uploaded. See [review contents](REVIEW_CONTENTS.md) for the six unchanged source documents and visuals, their purposes and the limits of this release.

## Local preservation

| Scope | Result |
|---|---|
| Starting path classification (17:18 UTC) | 229,276 file and symlink paths covered by file/folder rules |
| Confirmed agent intermediates archived | 1,072 files; 353,481,317 bytes |
| Relocation verification | All 1,072 archived files independently rehashed and reconciled with the move records |
| Additional candidate renders retained | 130; source/version mapping remains unresolved |

Substantive user-created or co-created materials, source documents, useful provenance and active tooling retain their local locations. Retired auxiliaries are preserved under one local `AGENT_ARCHIVE` parent, organized by their original relative paths. No mirror or flattened copy was created.

## Inventories and dates

- [Before archival](WORKSPACE_FILE_TYPES.csv): the original local census, grouped by filename extension and entry kind.
- [After archival](WORKSPACE_FILE_TYPES_AFTER_ARCHIVE.csv): the same starting population, partitioned into archived, retained and unresolved entries. Verification columns are separate flags, not additional files. New paths created after the original census are excluded.
- [Published source manifest](REVIEW_FILE_MANIFEST.json): hashes, sizes and observed filesystem dates for the six included source artifacts.

The later pre-move census (18:00–18:01 UTC) contains 253,594 entries: 226,870 regular files, 24,316 directories and 2,408 symlinks. Extension labels are not detected file formats. Detailed paths, original/current date observations and the relocation audit remain local. Git commit dates do not preserve original filesystem dates. No source timestamp resets were performed.

## Review still open

Starting metadata classification is complete; wider file-content review, source dependencies, audience-specific selection and cloud retrieval remain incomplete. Uncertain material was retained. Of the archived files, 369 also matched earlier recorded hashes; 703 were checked for unchanged current bytes without historical byte authentication. These are file-preservation checks, not independent corroboration of reported experiences or proposed mechanisms.
