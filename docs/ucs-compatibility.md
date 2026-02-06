# Relationship to the Universal Category System

This system is inspired by UCS conventions but is not formally UCS-compliant.

UCS was designed for sound effects and physical sound sources. It provides no official category for spoken dialogue, narration, or character voice acting. Treating dialogue as HUMAN or FOLEY assets usually obscures intent and makes libraries harder to use.

For that reason, this system does not attempt to assign UCS CatIDs to voice assets. Instead, it is an original implementation of the UCS design philosophy:

 - structured naming
 - predictable ordering of descriptors
 - avoidance of prose in filenames
 - separation of identity from description

For users who care about UCS-style organization, the CSV fields map reasonably well to UCS at a conceptual level. "Category" and "role" correspond loosely to source descriptors, while "trigger" and "substate" correspond to action or usage descriptors. "Variation" maps cleanly.

This loose compatibility is intentional. It avoids mislabeling dialogue as something it is not, while still producing assets that sit comfortably alongside UCS-organized libraries.

Documentation and README files of audio assets should state this explicitly. 
