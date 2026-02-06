# Overview

This repository documents a CSV-driven workflow for planning, producing, and delivering reusable voice assets (primarily for games). The system is designed to support structured dialogue and other sound libraries that prioritize usability for the artist, are documented well, and scale cleanly over time without relying on filenames as the primary carrier of meaning.

The guiding principle is using a single CSV-file that acts as a single source of truth. Filenames, folder structure, and embedded metadata are all derived from it. Audio files are never renamed or tagged manually once they enter the pipeline.

The workflow is deliberately conservative. It favors explicit structure and is intended to survive real-world use: localization, format conversion, repackaging, and collaboration with other people who did not design the system.

This documentation covers:
 - a cleanly structured category system for spoken voice
 - a canonical CSV schema
 - mapping to [UCS](https://universalcategorysystem.com/) concepts
 - mapping the same (meta-)data cleanly to iXML and the ASWG iXML extension
 - fitting these pieces together in a practical production pipeline

This repository serves as my own personal documentation. It depicts the system I use and is not meant as a tutorial or sound design guide. If you find useful ideas or concepts here you are welcome to iterate and expand on them.
