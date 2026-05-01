---
description: Force-save all current state to files
---
Trigger a full state save to all persistent files:

1. Update `world-state/current-state.md` with current scene/location/party status
2. Update active `campaigns/<name>/campaign.md`
3. Update `campaigns/<name>/quest-log.md` with quest progress
4. Update all `characters/pcs/*.md` files with current HP, inventory, notes
5. Update `npcs/index.md` with NPC status changes
6. Update `world-state/timeline.md` with new events
7. Update `world-state/inventory.md` if loot was gained
8. Update `campaigns/<name>/decisions.md` with key decisions
9. If in combat, flush combat state to `sessions/<id>.md`

Confirm each file updated successfully.

$ARGUMENTS
