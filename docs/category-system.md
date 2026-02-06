# Voice Category System

Spoken dialogue occupies an awkward position in existing sound-effect taxonomies. The Universal Category System (UCS) does not define dialogue or voice acting as a first-class category, and attempting to force dialogue into HUMAN or FOLEY categories usually produces more confusion than clarity.

This system therefore uses an explicit top-level category called VOICE. This is a conscious deviation from UCS, not an attempt to extend or redefine it. The goal is semantic clarity and internal consistency rather than formal compliance.

This category system is trigger-oriented rather than descriptive. Assets are classified by when and why they are played, as this maps better to how games and interactive systems actually use dialogue.

At a high level, each asset is described along five axes:

```Category```
Currently always VOICE. This exists mainly to keep the system open to future non-voice assets without breaking structure.

```Role```
The speaking entity or functional role. Examples include MECHANIC, MERCHANT, GENERIC_NPC, ANNOUNCER, or SYSTEM. Roles are intentionally broad. Fine character detail belongs in delivery and text, not in taxonomy.

```Trigger```
The game or system event that causes the line to play. This is the most important axis. Examples include GREET, WORK_COMPLETE, ERROR, IDLE, or CONFIRM.

 ```Substate```
An optional refinement of the trigger, used when the same trigger has multiple meaningful variants. Examples include SUCCESS, FAILURE, BUSY, WARNING, SHORT, or LONG. Substates should be mechanically useful, not purely descriptive.

 ```Delivery```
 A performance variant that does not change semantic meaning. Typical values are NEUTRAL, GRUFF, or DRY. Delivery exists to support variation and reuse, not characterization.

The intent is that a developer can wire these fields directly into a dialogue or state-machine system without having to reinterpret prose descriptions or filenames.
