# Workout Program

A personal functional fitness lifecycle planner — structured training cycles with strength, metcon, endurance, skill/core, and integrated nutrition, designed to be generated and managed with GitHub Copilot.

---

## What This Is

A Git-tracked record of training cycles built around a 5-day-per-week functional fitness program:

- **Mon / Wed / Fri** — Functional fitness (strength + metcon + skill/core)
- **Tue** — Indoor rowing (goal: 10 km under 50 min)
- **Thu** — Running (goal: 10 km under 50 min)

Each cycle has a defined focus, week-by-week load progression, and phase-adjusted nutrition targets. Weekly files are generated with GitHub Copilot using the instructions in [.github/copilot-instructions.md](.github/copilot-instructions.md).

---

## Repository Structure

```
workout-program/
├── README.md
├── equipment.md                  # Available equipment and gym space constraints
├── cycle-plan-template.md        # Blank template for starting a new cycle
│
└── 01-DefiningLimits/            # Example cycle folder (<no>-<name>)
    ├── cycle-plan.md             # Cycle overview, goals, progression, nutrition
    ├── weekly-template.md        # Week file structure used when generating weeks
    └── 2026-03-16_Week-1.md      # Generated weekly workout file
```

### Cycle Folder Naming

```
<two-digit-number>-<CycleName>
```

Examples: `01-DefiningLimits`, `02-StrengthBase`, `03-OpenPrep`

### Weekly File Naming

```
<CycleFolder>/YYYY-MM-DD_Week-N.md
```

Where `YYYY-MM-DD` is the Monday start date of that week.

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
- Produce a complete weekly file at `YYYY-MM-DD_Week-N.md`.

### Updating After a Session

After training, open the weekly file and update the score/notes blocks. Add feedback at the top of the next week's file (or ask Copilot to incorporate it).

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
