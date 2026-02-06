# Production pipeline

The workflow is split into distinct phases. Each phase has a clear output.

**Authoring**: Creation of the CSV - Categories, triggers, dialogue text and variations are finalized before recording begins. Asset names are assigned at this stage and treated as immutable identifiers.

**Recording & editing**: Audio is captured, cleaned, and exported as WAV files. Temporary filenames are acceptable here. Editorial decisions belong entirely to this phase.

**Processing & packaging**: WAV files are matched to CSV rows, renamed to their canonical asset names, embedded with iXML metadata, and sorted into a folder structure derived from category fields. This is now fully automated.

In the delivery phase, the resulting folder tree is validated, optionally spot-checked with a metadata tool such as BWF MetaEdit, and the uploaded to relevant marketplaces.

The key constraint is that manual intervention stops once the script runs. Changes and fixes happen in the CSV/script, not in the files.
