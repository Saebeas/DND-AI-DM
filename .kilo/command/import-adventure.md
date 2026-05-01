---
description: Import a D&D adventure module (PDF/MD) into the adventures folder
---
The co-DM wants to import an adventure. Process:

1. Ask for the adventure source (file path, or paste content)
2. Create directory `adventures/<adventure-name>/`
3. Parse the adventure into structured files:
   - `adventure.md` — full structured adventure content
   - `encounters.md` — extracted encounters with stat blocks
   - `npcs.md` — extracted NPCs with stats, personality, motivations
4. Present a summary to the co-DM:
   - Adventure overview (level range, estimated sessions, theme)
   - Key NPCs list
   - Major encounter count and difficulty
   - Suggested pacing notes
5. Ask how the co-DM wants to adapt for their party

$ARGUMENTS
