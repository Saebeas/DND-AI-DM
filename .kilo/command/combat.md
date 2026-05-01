---
description: Manage active combat - initiative, HP, conditions, turns
---
Start or manage a combat encounter:

If no combat is active:
1. Ask for encounter details (enemies, terrain, party positions)
2. Roll initiative for all combatants
3. Create combat tracker in `sessions/<id>.md`
4. Create detailed combat log in `combat-logs/<encounter-name>.md`

If combat is active:
1. Load current combat state from `sessions/<id>.md`
2. Display initiative order with HP/conditions
3. Announce current turn
4. Wait for co-DM input on actions
5. Resolve actions, roll dice openly, update state
6. Advance to next turn

Always announce: "[Roll: XdY+Z = Total]" for all dice rolls.

$ARGUMENTS
