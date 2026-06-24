# Workout Program

A personal functional fitness lifecycle planner — structured training cycles with strength, metcon, endurance, skill/core, and integrated nutrition, designed to be generated and managed with GitHub Copilot.

---

## What This Is

A Git-tracked record of training cycles built around a 5-day-per-week functional fitness program:

- **Mon / Wed / Fri** — Functional fitness (strength + metcon + skill/core)
- **Tue** — Indoor rowing (goal: 10 km under 50 min)
- **Thu** — Optional recovery LIIT (bike commute or 20 min light row)
- **Sat or Sun** — Running (goal: 10 km under 50 min)

Each cycle has a defined focus, week-by-week load progression, and phase-adjusted nutrition targets. Weekly files are generated with GitHub Copilot using the instructions in [.github/copilot-instructions.md](.github/copilot-instructions.md).

---

## Current Week

- [03-FatBurning - Week 6](03-FatBurning/week-6)
  - [Monday](03-FatBurning/week-6/01-monday.md)
  - [Tuesday](03-FatBurning/week-6/02-tuesday.md)
  - [Wednesday](03-FatBurning/week-6/03-wednesday.md)
  - [Thursday](03-FatBurning/week-6/04-thursday.md)
  - [Friday](03-FatBurning/week-6/05-friday.md)
  - [Saturday](03-FatBurning/week-6/06-saturday.md)
  - [Sunday](03-FatBurning/week-6/07-sunday.md)
  - [Nutrition](03-FatBurning/week-6/nutrition.md)

## Repository Structure

```
workout-program/
├── README.md
├── equipment.md                  # Available equipment and gym space constraints
├── cycle-plan-template.md        # Blank template for starting a new cycle
│
├── 01-DefiningLimits/            # Example legacy cycle folder (<no>-<name>)
    ├── cycle-plan.md             # Cycle overview, goals, progression, nutrition
    ├── weekly-template.md        # Week file structure used when generating weeks
    └── 2026-03-16_Week-1.md      # Legacy weekly workout file format
└── 03-FatBurning/                # Current cycle using split week files
    ├── cycle-plan.md
    ├── weekly-template.md
    └── week-2/
        ├── 01-monday.md
        ├── 02-tuesday.md
        ├── 03-wednesday.md
        ├── 04-thursday.md
        ├── 05-friday.md
        ├── 06-saturday.md
        ├── 07-sunday.md
        └── nutrition.md
```

### Cycle Folder Naming

```
<two-digit-number>-<CycleName>
```

Examples: `01-DefiningLimits`, `02-StrengthCut`, `03-FatBurning`

### Weekly File Naming

```
<CycleFolder>/week-N/<day-number>-<day>.md
```

Weekly nutrition is stored separately in:

```
<CycleFolder>/week-N/nutrition.md
```

Legacy exception: older cycles can keep the single-file format `YYYY-MM-DD_Week-N.md`.

---

## Workflows

### Starting a New Cycle

1. Create a new folder: `<NN>-<CycleName>/`
2. Copy `cycle-plan-template.md` → `<NN>-<CycleName>/cycle-plan.md` and fill in all fields.
3. Copy or adapt `weekly-template.md` from the closest previous cycle into the new folder.

### Generating a New Week

Ask GitHub Copilot:

> "Generate Week N for `<NN>-<CycleName>`."

Copilot will:
- Read `cycle-plan.md` for load targets, goals, and nutrition phase.
- Read `weekly-template.md` for structure.
- Read `equipment.md` for movement selection constraints.
- Produce all day files in `week-N/` plus `week-N/nutrition.md`.

### Updating After a Session

After training, open the relevant day file and update the score/notes block. Add feedback in the next week's files (or ask Copilot to incorporate it).

---

## Athlete Profile

| Attribute | Value |
|---|---|
| Sex / Age | Male, 38 |
| Body weight | 92 kg |
| Training days | 5 / week |
| Primary goal | Performance — fuel output, maximise recovery |

---

## Nutrition Baseline

| Day Type | Calories | Protein | Carbs | Fat |
|---|---|---|---|---|
| Functional Fitness (Mon/Wed/Fri) | ~3400 kcal | ~185 g | ~460 g | ~90 g |
| Endurance — Row/Run (Tue/Thu) | ~3200 kcal | ~185 g | ~410 g | ~90 g |
| Rest / Active Recovery (Sat/Sun) | ~2700 kcal | ~185 g | ~290 g | ~90 g |

Phase-specific adjustments (deload, build, push, test) are defined in each cycle's `cycle-plan.md`.

---

## Equipment

See [equipment.md](equipment.md) for the full list. Key constraints:

- Gym space: **5 m × 4 m** — no long carries or continuous runs.
- No Assault bike, ski erg, GHD, rope climb, sled, or cable machine.
- Running must leave the gym — always paired with a row/jump rope alternative.

---

## Cycles

| # | Name | Dates | Focus |
|---|---|---|---|
| 01 | DefiningLimits | 2026-03-16 → 2026-04-12 | Reactivation → baseline testing (3–5 RM lifts + 10 km benchmarks) |
| 02 | StrengthCut | 2026-04-14 → 2026-05-11 | Strength retention under cut + aerobic progression |
| 03 | FatBurning | 2026-05-11 → 2026-06-19 | Deficit phase with higher metcon output and endurance progression |
| 04 | ConditioningCut | 2026-06-30 → 2026-07-26 | Continued deficit; HSPU + pull-up volume via rotated accessories; VO2 max focus via rowing intervals + running |
