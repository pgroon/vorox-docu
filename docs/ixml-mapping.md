# iXML and embedded metadata

In addition to filenames and folders, asset metadata can be embedded directly into WAV files using iXML and the [ASWG iXML Extension](https://github.com/Sony-ASWG/iXML-Extension). This allows dialogue text, identifiers, and categorization to survive renaming, copying, and format conversion.

The CSV schema is designed to map cleanly onto iXML asset metadata.

At a minimum, the following fields should be written:
 - asset_name → ASSET_NAME
 - text → DESCRIPTION
 - cat, role, trigger, substate, delivery → KEYWORDS (comma-separated)

This minimal set already covers the majority of real-world use cases and is supported by most metadata-aware tools.
Additional ASWG extension fields (creative intent, loudness, variation grouping) are intentionally optional. They can be added later without changing the CSV structure, as long as the CSV remains the canonical source.
Metadata is written after audio editing is complete. The audio data itself is never modified during metadata injection.
