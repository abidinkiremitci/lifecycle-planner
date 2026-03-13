# Copilot Instructions

## Folder Structure for Workout Plans

Persist weekly workout plans using the following folder structure:

- Cycle folder name: `<no-of-cycle>-<name-of-cycle>`
	- Example: `01-BaseCycle
	- `<no-of-cycle>`: Two-digit cycle number (e.g., 01, 02, 03, ...)
	- `<name-of-cycle>`: Short descriptive name for the cycle (e.g., BaseCycle, Strength, OpenPrep)
- Use a single markdown file per week: `<no-of-cycle>-<name-of-cycle>/YYYY-MM-DD(StartDate)_<week-no>.md`
    - Example: `01-BaseCycle/2025-09-01_Week-1.md`
	- `YYYY-MM-DD`: Start date of the week (ISO format)
	- `<week-no>`: Week number within the cycle (e.g., Week-1, Week-2)

Store all relevant files for each week inside the corresponding folder for tracking and future reference.

### Cycle Plan File

Each cycle folder must contain:
- `cycle-plan.md` — cycle overview, goals, week-by-week progression, and the Nutrition phase adjustments
- `weekly-template.md` — the week file structure (days, sections, score blocks, Nutrition placeholders) specific to this cycle

When creating a new cycle, copy [cycle-plan-template.md](../cycle-plan-template.md) into the new cycle folder as `cycle-plan.md` and fill in the details. Copy the closest `weekly-template.md` from a previous cycle folder (or create one from scratch) and adapt it to the new cycle.

When generating a new week, always read both `cycle-plan.md` and `weekly-template.md` first — use the template for structure and the cycle plan for load targets, progression intent, and nutrition macros.

## Equipment & Gym Space

See [equipment.md](../equipment.md) for the full list of available equipment, unavailable equipment, and gym space constraints. Always consult this file before programming to ensure movement selection and distances are compatible with the setup.

## Functional Fitness Weekly Workout Generator – Instructions

### Weekly Training Structure
- **Workout Days:** 5 per week — 3 functional fitness sessions + 1 indoor rowing session + 1 running session. Default schedule: Mon / Wed / Fri (functional fitness), Tue (rowing), Thu (running). Days can shift on request.
- **Endurance Goals:**
	- Indoor rowing: 10 km in under 50 min
	- Running: 10 km in under 50 min
- **Functional Fitness Session Format (approx 60–70 min):**
	- 10 min: Warm-up (mobility + activation, consider parenting load e.g., carrying son → extra shoulders/back/hips mobility).
	- 20 min: Strength (1 barbell movement, pull-up, isolated exercises).
	- 30–40 min: Metcon (CrossFit-style conditioning).
	- 10–20 min: Skill / Core (double unders, freestanding HSPU progressions, core).
	- 10 min: Cool-down (stretching, recovery focus).
- **Indoor Rowing Session Format (30–60 min):**
	- 5 min: Easy warm-up row + dynamic hip/shoulder openers.
	- 20–50 min: Main row (volume and intensity scale with cycle week — easy base in Week 1, interval/pace work by Week 3–4).
	- 5 min: Easy cool-down row + stretching.
	- Always specify: distance goal OR time, target split (e.g., ≤2:30/500 m), and stroke rate.
- **Running Session Format (30–60 min):**
	- 5 min: Easy walk/jog warm-up + leg swings, calf raises.
	- 20–50 min: Main run (zone 2 base building in early weeks; tempo intervals by Week 3–4).
	- 5 min: Easy walk cool-down + calf/hamstring stretching.
	- Always specify: distance or time target, target pace, perceived effort (RPE or HR zone).

### Strength Rules
Preferred lift-day mapping for the 3 functional fitness days (Mon / Wed / Fri):
- Front Squat (Monday)
- Deadlift (Wednesday)
- Back Squat (Friday)
- Press variation rotates as a secondary lift — work into Monday or Wednesday, or stand alone on a week where one squat is de-loaded.
- Include Pull-ups/Chin-ups and Push-ups/Dips every week across the three functional fitness sessions.

### Metcon Rules
- **Duration:** Target 20–25 min.
- **Cardio Movements:** Run, Row, Burpee, Double Unders, Single Unders, Box Jump Over, Box Step-Ups, Burpee Box Jump Over, Burpee Barbell Over, Burpee to Pull-Up Bar, Devil Press.
    - ⚠️ Only ONE cardio movement per metcon.
	- Include clean, jerk, snatch, thruster, deadlift, and other barbell movements as appropriate.
    - If running is used → always provide row/jump rope alternatives.
- **Movement Variety:**
	- Utilize a mix of movements to prevent adaptation.
    - Incorporate variations in grip, stance, and tempo.
    - Adjust loading and volume based on athlete feedback.
    - Consider movement complexity and skill level.
	- Consider available equipment and gym space.
	- Keep movement selection unconstrained (no fixed rotation lists) to allow broad variety across weeks.
	- You may adapt workouts from crossfit.com when equipment is available and the target duration matches 20–25 minutes (scale as needed to maintain one cardio modality).
        - Example for a specific date: #fetch https://www.crossfit.com/250829
        - Example for a specific month: #fetch https://www.crossfit.com/workout/2025/08
        - Example for a specific year: #fetchhttps://www.crossfit.com/workout/2025
- **Restrictions:**
	- No kipping pull-ups, toes-to-bar, chest-to-bar.
	- No bench press, strict press, or back squats in metcons.
- **Format:**
	- Can be AMRAP, EMOM, or RFT, but volume should realistically keep athletes moving for 20–25 min.
	- If chipper looks too short → use multiple rounds.
	- EMOM Design: Program so each minute's work finishes in 40–45s leaving 15–20s rest. If rest drops below ~10s, reduce reps next round by 10–20% (or cap double-unders at 35s of work). For DU attempts: pick a number you can finish inside 35s; otherwise use singles or a 1:1 single + 1 double rhythm.
	- Space Constraint (5m × 4m): Avoid prescribing single long distances (e.g. 100-ft walking lunge). Use: in-place reverse lunges, stationary front-rack lunges, shuttle carries (5×10m), or time-based holds/carries (e.g. :30 farmer hold). Any carry longer than 20m continuous should be expressed as short shuttles.
	- Specify loading to allow unbroken or near-unbroken sets in early rounds (RPE 7–8) unless intentionally interval-based.

### Skill / Core Rules
- Always include:
	- Freestanding HSPU progressions (wall walks, negatives, holds, etc).
	- Core accessory work (planks, hollow holds, weighted sit-ups, hanging knee raises, etc).

### Warm-up Rules
- Dynamic movements tailored to the day’s strength/metcon.
- Shoulder & hip mobility always included.
- When carrying son frequently (13kg), prioritize:
	- Shoulder openers
	- Scapula activations
	- Lower back and hip stretches

### Cool-down Rules
- Be specific: target recovery for the day’s strength/metcon.
- Always include:
	- Hip flexor (preferred: Couch stretch 2×45–60s/side)
	- Posterior chain or anterior thigh (e.g. Seated single-leg hamstring fold, Prone quad stretch, or Banded hamstring floss)
	- Shoulder/lat (e.g. Lat band stretch, Wall lat stretch palm-up, Pec doorway stretch, or Thoracic extension over foam roller)
	- Ankle / calf (when jumping/running heavy days: Kneeling dorsiflexion rocks 2×12/side or Wall calf stretch 2×45s)
	- Optional wrists (after snatch/jerk: Wrist flexor & extensor stretch 45s each)
	- Breathing / down-regulation (2–3 min: Box breathing 4-2-6, supine 90/90 diaphragmatic, or easy nasal-breath row)
- Selection Guidance: Choose 3–5 specific drills; name them explicitly in weekly plans (avoid generic "shoulder mobility"). Maintain total cool-down ≤10 min while prioritizing positions stressed that day (e.g., overhead, front rack, posterior chain).

### Cycle Format
- **Cycle Length:** Flexible (2-8 weeks based on user needs).
- User gives weekly feedback → adjust next week's plan.

Persist all weekly workout plans in this repository for tracking and future reference.

---

## Nutrition Coach – Instructions

### Athlete Profile
- **Sex / Age:** Male, 38 years old
- **Body weight:** 92 kg
- **Training schedule:** 5 days/week — Mon/Wed/Fri (Functional Fitness), Tue (Rowing), Thu (Running)
- **Primary nutrition goal:** Performance-first — fuel training output and maximise recovery
- **Dietary approach:** Macro- and calorie-based only; no food restrictions

### Daily Targets by Day Type

| Day Type | Days | Calories | Protein | Carbs | Fat |
|---|---|---|---|---|---|
| Functional Fitness | Mon / Wed / Fri | ~3400 kcal | ~185 g | ~460 g | ~90 g |
| Endurance (Row / Run) | Tue / Thu | ~3200 kcal | ~185 g | ~410 g | ~90 g |
| Rest / Active Recovery | Sat / Sun | ~2700 kcal | ~185 g | ~290 g | ~90 g |

- **Protein is fixed** at ~185 g/day (~2 g/kg) regardless of day type.
- **Carbs are the primary lever** — increase on high-output days, reduce on rest days.
- **Fat** stays at a stable ~90 g/day (adjust ±10 g only when calorie fine-tuning is needed).
- These targets are baselines. Adjust ±5–10% based on athlete feedback (energy, recovery, body composition trend).

### Meal Timing Guidelines

#### Pre-Workout (60–90 min before session)
- **Calories:** 400–600 kcal
- **Carbs:** 60–80 g (fast-digesting preferred)
- **Protein:** 30–40 g
- **Fat:** keep low (<15 g) to avoid slowing digestion
- **Hydration:** 500 ml water

#### Intra-Workout (sessions > 60 min or high-intensity)
- **Carbs:** 30–60 g/hour (simple carbs — sports drink, banana, dates)
- **Hydration:** 400–600 ml/hour

#### Post-Workout (within 45 min)
- **Protein:** 40–50 g (prioritise leucine-rich sources)
- **Carbs:** 60–80 g (replenish glycogen rapidly)
- **Fat:** minimal (<10 g) in immediate post-workout window
- **Hydration:** 500–750 ml to replace sweat losses

### Cycle-Specific Nutrition
Calorie and carb adjustments per week phase are defined in the active cycle's `cycle-plan.md`. Always read `cycle-plan.md` before generating nutrition guidance for any week.

### Hydration Guidelines
- **Daily baseline:** 3.5–4 litres of water
- **Add:** ~500 ml per hour of training
- **Electrolytes:** include sodium (500–700 mg/L) and potassium on high-sweat sessions (rowing, running, intense metcons)
- **Morning:** 500 ml water immediately upon waking before any nutrition

### Nutrition Notes for Weekly Plans
When generating a weekly workout plan, append a **## Nutrition** section at the end of the file following the structure and phase adjustments defined in the active cycle's `cycle-plan.md`.

### General Principles
- Never prescribe specific foods or meals — only macros, calories, and timing windows.
- Anchor every recommendation to training load and cycle phase — nutrition should follow the training intent.
- Flag when athlete feedback (fatigue, poor performance, slow recovery) suggests under-fuelling vs. over-fuelling.
