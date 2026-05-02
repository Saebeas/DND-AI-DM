---
description: View or update an existing player character sheet
---

For **creating** a new character, use `/addnewpc` instead — it launches the full interactive 8-phase character creation workflow.

## Viewing a Character
1. Use file tools to locate the character's `.md` file in `characters/pcs/`.
2. Read and present the full character sheet to the co-DM.

## Updating a Character
1. Load the existing PC file from `characters/pcs/<name>.md`.
2. Apply requested changes:
   - HP changes (damage, healing, temp HP)
   - Conditions (add/remove)
   - Equipment changes (add/remove items, gold)
   - Spell slot usage
   - XP awards
   - Ability score changes (ASI, feats, magic items)
   - Any other stat updates
3. Recalculate derived stats if needed (AC, modifiers, save DCs, skill totals).
4. Confirm all changes with the co-DM before saving.
5. Add an entry to the **DM Tracking** section with date and description of change.

## Updating XP
- When XP is awarded, update the **Current XP** field and the **DM Tracking** entry.
- If the new XP meets a level-up threshold, prompt the co-DM to run `/levelup [Character Name]`.

$ARGUMENTS
