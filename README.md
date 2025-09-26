# Project 2 — PDDL Planning (GitHub Template)

This repository scaffolds your **Project #2** for Planning with PDDL and **pddl4j**.  
It includes a clean directory structure, ready-to-run scripts, and report templates.

## Contents
```
blocksworld/
  domains/blocksworld.pddl
  problems/pb1.pddl
  problems/pb2.pddl
  problems/pb3.pddl
dockerrobot/
  domain.pddl
  pb1.pddl
puzzle-4x4/
  domain.pddl
  pb1.pddl
scripts/
  run_blocksworld.sh
  run_blocksworld.bat
results/
  planners_comparison.csv
report/
  REPORT_TEMPLATE.md
lib/
  (put pddl4j-4.0.0.jar here — ignored by git)
.gitignore
LICENSE
README.md
```

## Setup

1. Install a recent Java (JDK 11+ recommended).
2. Download **pddl4j** and place the JAR into `lib/` as `pddl4j-4.0.0.jar`.
3. Verify `java` is on your PATH: `java -version`.

> Example run command (Linux/macOS):
```bash
java -cp lib/pddl4j-4.0.0.jar fr.uga.pddl4j.planners.statespace.FF   blocksworld/domains/blocksworld.pddl   blocksworld/problems/pb1.pddl
```

> Example run command (Windows - PowerShell/CMD):
```bat
java -cp lib\pddl4j-4.0.0.jar fr.uga.pddl4j.planners.statespace.FF ^
  blocksworld\domains\blocksworld.pddl ^
  blocksworld\problems\pb1.pddl
```

You can also use the helper scripts in `scripts/`.

## What you need to do

- **Task 1 — BlocksWorld:** Solve 3 problems using different planners (e.g., FF, A* variants available in pddl4j), compare solution length/time, and interpret results. Update `results/planners_comparison.csv`.
- **Task 2 — 4×4 Puzzle:** Provide `puzzle-4x4/domain.pddl` and a problem file (`pb1.pddl`). A template is included — complete/optimize it.
- **Task 3 — Robot Docker:** Provide `dockerrobot/domain.pddl` and `pb1.pddl`. A minimal working template is included — adapt to your variant.
- **Bonus — Wumpus:** (optional) Add a new folder `wumpus/` with domain+problem files and include your run commands & traces in the report.

## Scripts

- `scripts/run_blocksworld.sh` runs FF on pb1–pb3 (Linux/macOS).
- `scripts/run_blocksworld.bat` does the same on Windows.
- Feel free to add more scripts for other planners (`fr.uga.pddl4j.planners.*`).

## Report

Use `report/REPORT_TEMPLATE.md`. Include:
- code snippets you changed/added,
- **execution traces** (copy the planner output),
- **comparison table** of planners (time, steps, actions),
- teammate names and contribution breakdown,
- ToC and clean structure.

## Notes

- Keep the `lib/` folder **out of git** (`.gitignore` already handles that).
- You can open issues/PRs on your private GitHub to collaborate with teammates.
- If you change the folder layout, be sure to update the scripts.

Good luck & happy planning!
