# D&D 5.5th Edition (2024) Character Creation Workflow

## CRITICAL RULES
1. **ONE QUESTION AT A TIME.** Ask one question (or a small logically grouped set), then STOP and WAIT for the co-DM's response before proceeding. NEVER ask multiple unrelated questions in a single turn.
2. **KEEP IT SIMPLE.** When reporting results (species traits, class info, etc.), show ONLY the information relevant to the ONE field being filled in. Do NOT dump full class tables, spell lists, or exhaustive trait descriptions. Give the player the minimum they need to write one field on their sheet, then stop. The player does not need to see the entire Druid spell list when picking a class — they just need to know "Druid, Level 1, write it here."
3. **SHEET LOCATION FIRST.** Every single response MUST start with exactly WHERE on the physical character sheet to write the value. Format: **"Write [VALUE] in [LOCATION]."** Then a 1-sentence explanation of what it means. Then stop.
4. **AUTO-CALCULATE & PAUSE.** When a stat can be derived, calculate it automatically. Show ONLY the value and its sheet location. Say: *"Please write this on your physical character sheet. Let me know when you are ready to proceed."*
5. **USE WEB SEARCH FIRST.** Always use the `duckduckgo_search` tool to look up D&D 5.5e (2024) rules — search results are more reliable and less prone to hallucination than training data. When you do search, make ONE targeted query and extract ONLY the single value you need. NEVER fetch an entire class description, species block, spell list, or equipment table. **BREVITY IS KEY** — the purpose of searching is ONLY to provide short, accurate descriptions that the player can copy onto their physical character sheet (e.g., spell name, casting time, range, damage, one-line effect). The digital character file will serve as the in-game reference for full details during play.
6. **SAVE TO FILE.** At the end, write the character to `characters/pcs/<name-slug>.md` using the comprehensive template.

## RESPONSE FORMAT RULES
- Each turn should be **3-5 lines max** (excluding the "write this down" prompt).
- Never show more than ONE table per turn.
- Never list more than ONE set of options per turn.
- If the player asks "what does X mean?", explain it in ONE sentence.
- When reporting species traits or class features after a selection, show them as a **short bullet list** (name + one-line description each), NOT full block text.
- Do NOT show spell lists, weapon tables, or equipment lists until that specific phase asks for them.
- **FIELD-SCOPED OUTPUT ONLY.** Each step MUST only output information relevant to the specific field(s) being written in that step. Do NOT include stats, features, proficiencies, or details that belong in other fields — those will be covered in their own phase. For example, when filling the Class field, do NOT dump hit dice, saving throws, spellcasting info, class features, or equipment lists. Just the class name and a brief one-liner about what it is.
- ALWAYS end each turn with: *"Please write this on your physical character sheet. Let me know when you are ready to proceed."* (or equivalent pause prompt)

---

## Phase 1: Core Identity
The **Campaign** field is pre-filled from the `/addnewpc` initiation — do NOT ask for it again.

Ask each of the remaining fields **one at a time**, waiting for response between each:

### 1a. Species
Ask the co-DM to choose a Species. Use `duckduckgo_search` to look up the 2024 species traits — keep results brief (one-line per trait). **ONE SEARCH ONLY** — if you need multiple species lookups, do them one at a time across separate messages. After they choose, report ONLY:
- **Write "Species: [NAME]" below Character Name, left side of header.**
- One-line summary: Speed, Size.
- Bullet list of traits (name + one-line description each).
- End with pause prompt.

Do NOT list all species options with full stats. Just name the options (one-line each) and wait.
Do NOT include ability score bonuses, class features, equipment lists, or anything not directly tied to the Species field.

### 1b. Class & Level
Ask for Class and starting Level. After they choose, report ONLY:
- **Write "Class: [NAME]" below Character Name, right side.**
- **Write "[LEVEL]" in the large center circle.**
- **Write "0 XP" in the small semi-circle below the level circle (if Level 1).**
- **Write "+2" in the top left corner above the Strength block (Proficiency Bonus).**
- One-line flavor: what the class IS (e.g., "a nature-based divine spellcaster").
- End with pause prompt.

Do NOT dump the full class feature table, spell list, equipment list, hit dice, saving throws, or stat breakdowns. Just the fields being filled in now. Hit Dice, Saving Throws, and other derived stats are handled in their own phases.

### 1c. Subclass
If the chosen class gets a subclass at or before the starting level, ask for it. After they choose, report ONLY:
- **Write "Subclass: [NAME]" below Class, right side.**
- One-line description of the subclass.
- End with pause prompt.

If subclass is at a higher level (e.g., Druid at 3), say: "Not yet — you choose a subclass at Level [X]. We'll handle that later."

### 1d. Background
Ask for Background. After they choose, report ONLY:
- **Write "Background: [NAME]" below Character Name, left side.**
- Bullet list: skill proficiencies, tool proficiency, feat gained.
- End with pause prompt.

Do NOT list all backgrounds with full details. Just name the options and wait.
Do NOT include backstory, personality, or ability score bonuses — those are separate fields.

### 1e. Alignment
Ask for Alignment. Report ONLY:
- **Write "[ALIGNMENT]" at the very bottom of the Backstory & Personality box on Page 2.**
- One-sentence description of what it means.
- End with pause prompt.

---

## Phase 2: Ability Scores
### Step 1: Method
Ask which method: **Standard Array** (15, 14, 13, 12, 10, 8), **Point Buy** (27 points), or **Rolling** (4d6 drop lowest). One-sentence explanation of each. Wait for response.

### Step 2: Assignment
One ability at a time. Ask where to put each score. After ALL six are assigned, auto-calculate modifiers using `floor((Score - 10) / 2)` and present a single table:

| Ability | Score | Modifier | Sheet Location |
|---------|-------|----------|---------------|
| STR | XX | +X | Small box, left column. Modifier in large circle. |
| DEX | XX | +X | Same pattern, left column. |
| CON | XX | +X | Same pattern, left column. |
| INT | XX | +X | Small box, second column. Modifier in large circle. |
| WIS | XX | +X | Same pattern, second column. |
| CHA | XX | +X | Same pattern, second column. |

*"Please write these down on your physical character sheet. Let me know when you are ready to proceed."*

---

## Phase 3: Derived Combat Stats
Auto-calculate and display each stat ONE AT A TIME, starting with HP. For each stat, show:
1. The value.
2. Exactly where to write it.
3. One-sentence explanation.

Order: Max HP → Current HP → Hit Dice → Initiative → Speed → Size → Passive Perception → Death Saves (explain) → Heroic Inspiration (explain).

Do NOT dump all derived stats in one giant block. One stat per message, with sheet location.

For Max HP: Class Hit Die value + CON modifier (at Level 1). Add +1 for Dwarven Toughness if Dwarf.
For Initiative: DEX modifier.
For Speed & Size: From Species selection.
For Passive Perception: 10 + WIS modifier + (Proficiency Bonus if proficient in Perception).

Sheet Locations:
- **Current HP:** Large box in upper middle of HP section.
- **Max HP:** Bottom right of Current HP box.
- **Temp HP:** Small box to the right of Current HP.
- **Hit Dice Spent:** Top half of Hit Dice box.
- **Hit Dice Max:** Bottom half.
- **Initiative:** Box directly below header, left of Speed.
- **Speed:** Box to the right of Initiative.
- **Size:** Box to the right of Speed.
- **Passive Perception:** Box on the far right of derived stats row.
- **Death Saves:** Successes = top row of 3 diamonds. Failures = bottom row of 3 diamonds.
- **Heroic Inspiration:** Shield icon below Constitution block.

After displaying each stat, pause: *"Please write this on your physical character sheet. Let me know when you are ready for the next one."*

---

## Phase 4: Proficiencies & Skills

### 4a. Saving Throws
**Auto-calculate** the 2 class saving throw proficiencies. For proficient saves: modifier + Proficiency Bonus. For non-proficient: just the modifier.

| Save | Proficient | Total |
|------|-----------|-------|
| STR   | Yes/No    | +X    |
| DEX   | Yes/No    | +X    |
| CON   | Yes/No    | +X    |
| INT   | Yes/No    | +X    |
| WIS   | Yes/No    | +X    |
| CHA   | Yes/No    | +X    |

Sheet Location: Each saving throw is a bubble within its ability block.

### 4b. Skill Proficiencies
List the available skill choices based on Class and Background. Ask the co-DM to choose (class gives X choices, background may add more).

**Auto-calculate all 18 skills:**

| Skill | Ability | Proficient | Total |
|-------|---------|-----------|-------|
| Acrobatics | DEX | | +X |
| Animal Handling | WIS | | +X |
| Arcana | INT | | +X |
| Athletics | STR | | +X |
| Deception | CHA | | +X |
| History | INT | | +X |
| Insight | WIS | | +X |
| Intimidation | CHA | | +X |
| Investigation | INT | | +X |
| Medicine | WIS | | +X |
| Nature | INT | | +X |
| Perception | WIS | | +X |
| Performance | CHA | | +X |
| Persuasion | CHA | | +X |
| Religion | INT | | +X |
| Sleight of Hand | DEX | | +X |
| Stealth | DEX | | +X |
| Survival | WIS | | +X |

Proficient skill total = Ability Modifier + Proficiency Bonus.
Sheet Location: Each skill is a bubble within its associated ability block.

### 4c. Equipment Training
List armor and weapon proficiencies from class. Sheet Location: **Equipment Training & Proficiencies** in the bottom left corner.

### 4d. Tools & Languages
Ask for tool proficiencies from Background/Species. Ask for known Languages from Species/Background. Sheet Location: **Languages** box below Backstory & Personality on Page 2. Tools go in Equipment Training section.

*"Please write these down on your physical character sheet. Let me know when you are ready to proceed."*

---

## Phase 5: Equipment & Armor Class (AC)

### 5a. Equipment Method
Ask: **Starting equipment** (class/background defaults) or **rolling for gold** (buy your own)?

### 5b. Armor & Shield
Ask what armor (if any) and whether they use a shield. Use `duckduckgo_search` to look up the armor's base AC — extract only that one value.

**Auto-calculate AC:**
- Light Armor: Base AC + DEX modifier
- Medium Armor: Base AC + DEX modifier (max +2)
- Heavy Armor: Base AC (no DEX)
- Shield: +2

Sheet Location: **AC** is the large shield shape to the right of the Level circle. **Shield** is the small diamond at the bottom point.

### 5c. Weapons
Ask what weapons the character carries. Use `duckduckgo_search` to look up each weapon's stats — extract only damage die, properties, and weight.

**Auto-calculate for each weapon:**
- **Attack Bonus:** Relevant ability modifier (STR for melee, DEX for ranged, either for Finesse) + Proficiency Bonus
- **Damage:** Weapon dice + ability modifier
- **Properties:** Light, Finesse, Versatile, Range, etc.

Present as a weapon table:

| Weapon | Attack Bonus | Damage | Properties |
|--------|-------------|--------|------------|
| [Name] | +X          | XdX+X [type] | [props] |

Sheet Location: **Weapons & Damage Cantrips** is the large table below the derived stats row.

### 5d. Currency
Track starting gold and any coins from equipment/background. Sheet Location: **Coins** bottom right corner (CP, SP, EP, GP, PP).

*"Please write these down on your physical character sheet. Let me know when you are ready to proceed."*

---

## Phase 6: Magic & Spells (Only if Spellcaster)
Skip this entire phase if the class is not a spellcaster (Barbarian, Fighter, Monk, Rogue at Level 1 — unless subclass grants casting like Eldritch Knight or Arcane Trickster at later levels).

### 6a. Spellcasting Basics
Identify the Spellcasting Ability (INT, WIS, or CHA based on class).

**Auto-calculate:**
- **Spell Save DC:** 8 + Proficiency Bonus + Spellcasting Ability Modifier
- **Spell Attack Bonus:** Proficiency Bonus + Spellcasting Ability Modifier
- **Spell Slots:** Based on class and level (full caster, half caster, or third caster progression).

Sheet Locations on Page 2:
- **Spellcasting Ability:** Top left box.
- **Spellcasting Modifier:** Below Spellcasting Ability.
- **Spell Save DC:** Below Spellcasting Modifier.
- **Spell Attack Bonus:** Below Spell Save DC.
- **Spell Slots:** Top center block (Levels 1-9).

### 6b. Cantrips
Ask the co-DM to choose cantrips (number based on class/level). Use `duckduckgo_search` to look up each cantrip — report only: Casting Time, Range, Duration, Components, and a one-line effect summary for the physical sheet. **Search for each cantrip ONE AT A TIME across separate messages — never search for multiple cantrips in the same response.**

### 6c. Prepared/Known Spells
Ask the co-DM to choose spells. Use `duckduckgo_search` to look up each spell — report only: Level, Casting Time, Range, Duration, Concentration (Y/N), Ritual (Y/N), Components (V/S/M and material cost if any), and a one-line effect summary for the physical sheet. **Search for each spell ONE AT A TIME across separate messages — never search for multiple spells in the same response.**

Present each spell clearly formatted. Sheet Location: **Cantrips & Prepared Spells** table on Page 2, left and middle.

*"Please write these down on your physical character sheet. Let me know when you are ready to proceed."*

---

## Phase 7: Features, Traits, & Flavor

### 7a. Class & Subclass Features
List all features gained from Class and Subclass at the current level. Explain each briefly. Sheet Location: **Class Features** large central text box.

### 7b. Species Traits
List all Species Traits with descriptions. Sheet Location: **Species Traits** bottom middle text box.

### 7c. Feats
Ask if the character has any Feats (from Background, Species, or Variant rules). If so, list and explain each. Sheet Location: **Feats** bottom right text box.

### 7d. Appearance
Ask for physical appearance description. Sheet Location: **Appearance** top right box on Page 2.

### 7e. Backstory, Personality & Alignment
Ask for:
- Backstory
- Personality traits / ideals / bonds / flaws
- Alignment (if not already set)
Sheet Location: **Backstory & Personality** large box on Page 2.

### 7f. Magic Item Attunement
Leave blank unless the co-DM specifies starting magic items. Sheet Location: **Magic Item Attunement** three diamond bullet points at the bottom of the Equipment box on Page 2.

---

## Phase 8: File Generation
Once all phases are complete, generate the character file using the comprehensive template in `templates/character-template.md`. Save it to `campaigns/<campaign-name>/pcs/<character-name-slug>.md` where:
- `<campaign-name>` is the campaign directory chosen at the start of `/addnewpc`
- `<character-name-slug>` is the lowercase, hyphenated name (e.g., `lyra-quickfingers.md`)

Set the **Campaign** field in Core Identity to the campaign name.

**Do NOT save to `characters/pcs/`** — that is a legacy/shared location. The authoritative PC file lives inside the campaign folder.

If a file already exists for that name in the campaign's `pcs/` folder, warn the co-DM and ask before overwriting.

After writing the file:
1. Update `campaigns/<campaign-name>/campaign.md` — add a row to the **Party Roster** table with the character's Name, Race, Class, Level, Player, and Status (Active).
2. Confirm to the co-DM that the character has been saved and provide the file path.
