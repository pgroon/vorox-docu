# CSV Specification

All planning, production, and delivery for a project is done in a single CSV file. This CSV acts as the authoritative source for recording, editing, and packaging.

The schema is:

    cat,role,trigger,substate,delivery,asset_name,text,usage_notes

The meaning of each column is fixed.

```cat```

Logical content domain. Currently always VOICE, but retained to keep the schema extensible.

```role```

The speaking role or function. This is not a character name. It should remain reusable across projects.

```trigger```

The event or state that causes the asset to play. Triggers are chosen to map cleanly to game logic rather than narrative flow.

```substate```

Optional refinement of the trigger. Leave empty if no meaningful distinction exists.

```delivery```

Performance style. This should only affect tone, not meaning.

```asset_name```

A stable, extension-free identifier. This is the canonical identity of the asset and is used for filenames, metadata, and cross-references. Once published, asset names should never change.

```text```

The spoken dialogue. This is the authoritative version of the line and is the correct place for localization, censorship, or wording changes.

```usage_notes```

Freeform notes. This column is ignored by scripts and exists only to convey intent to collaborators or to the future self.

The CSV is used both for planning (before recording) and as an index for automation (after recording). Scripts should fail loudly if required fields are missing or duplicated.
