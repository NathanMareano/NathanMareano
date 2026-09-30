# Vantic

**Sports research application · Personal project · Working prototype in development**

[Back to profile](../README.md) · [Full walkthrough](https://nathanielmareano.com/projects/vantic/)

![Vantic player research view with recorded season statistics, game results, and matchup context](../assets/vantic-performance.jpg)

*Actual development screen captured September 27, 2026, using a saved research snapshot. The statistics shown are historical records, not live game data.*

## Why I built it

I wanted sports research to be freely accessible and easier to follow. Looking into a player or matchup often means moving between statistics, schedules, injury reports, and separate explanations. Vantic brings that context together and lets someone follow a number back to its source and calculation.

## My contribution

I'm developing the product direction, interface, and data workflows. The current web prototype focuses on NFL research, with a parallel SwiftUI app project in development.

**Stack:** React, FastAPI, Python, SQLite; SwiftUI for the native app.

## How it works

1. Python workflows collect public team, player, schedule, and contextual data.
2. Required inputs are validated before a new research snapshot is published.
3. FastAPI serves the research to the React interface with sample periods, formulas, and source metadata.
4. Saved research retains its original evidence for later comparison.

## Decisions that matter

- **Keep a usable snapshot.** A failed required feed preserves the previous core snapshot; optional feeds update separately.
- **Show gaps honestly.** A missing statistics row does not become zero, and an unavailable injury report does not imply a healthy player.
- **Make the reasoning visible.** Calculations include their source, sample, and limitations so a polished chart does not hide uncertainty.

## Current status

The web prototype runs locally and supports player and team research, game logs, measured factors, source metadata, and saved research. The applications remain in development. Next work includes broader validated coverage and evaluation across seasons and changing player roles.

The source code is private. This page shares the product and engineering approach.
