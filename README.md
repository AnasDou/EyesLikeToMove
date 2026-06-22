# Task
# Eyesliketomove — Inconsistency-Detection Stimuli

A set of controlled HTML stimuli for studying cognitive load during **code comprehension**
with multimodal sensing (webcam gaze estimation, mouse coordination, and reaction-time probes).

Each stimulus shows two representations of the same algorithm side by side and asks the
participant to find a single **inconsistency** between them. Every stimulus is a self-contained
HTML file rendered at a fixed **1920 × 1080-safe canvas of 1920 × 980** with **no scrolling**.

## Study design

- **Within-subject**, two factors:
  - **Stimulus type**: `statement + code` and `statement + flowchart`
  - **Difficulty**: `easy` (single-loop algorithms) and `hard` (sorting / recursion)
- **12 main tasks** = 6 easy + 6 hard. Within each difficulty, 3 tasks are `statement + code`
  and 3 are `statement + flowchart`. All 12 use **different algorithms**.
- **2 warm-up tasks** (one per stimulus type) to familiarise participants with the paradigm.
- **1 baseline task** — a fully **consistent** stimulus (no inconsistency) used to record a
  clean reading / resting measurement.

## Design principles

- **Cross-referential inconsistencies.** Every error is a mismatch that can only be found by
  *comparing the two panels* (a loop bound, an operator direction, a recursion side, an
  off-by-one, an initial value). Both panels look individually plausible, so the inconsistency
  cannot be spotted from prior knowledge of the algorithm alone.
- **Balanced placement.** Of the 12 inconsistencies, 6 live in the statement and 6 in the
  reference (code/flowchart), so no single representation is systematically the "correct" one.
- **Comparable complexity within each difficulty**, controlled on both code size and text
  metrics (word count, sentence count).
- **Equal occupied surface.** The statement block and the code/flowchart block are tuned to
  occupy comparable on-screen area (surface ratio ≈ 0.96–1.00 for all real tasks), so the two
  AOIs are size-matched and don't bias gaze metrics.
- **Wide line pitch for webcam tracking.** Lines are widely spaced (code ≈ 63 px
  center-to-center; statement 57–96 px) so a lower-accuracy webcam estimate can be attributed
  to the correct line with reasonable confidence.
- **Layout:** statement always on the **left**, code/flowchart on the **right**. French
  stimulus content, large fonts, no scrolling, fixed 1920 × 980.

## Contents

| File | Purpose |
|------|---------|
| `index.html` | Researcher navigation page (one card per task, with the answer). |
| `e*_easy_*.html` | 6 easy tasks (E1–E6). |
| `h*_hard_*.html` | 6 hard tasks (H1–H6). |
| `w*_warmup_*.html` | 2 warm-up tasks (W1–W2). |
| `b1_baseline_*.html` | 1 baseline task (consistent, no inconsistency). |
| `ANSWER_KEY.md` | Full answer key + measured comparability/alignment metrics. |
| `_records.json`, `_metrics.json` | Machine-readable task list and per-task measurements. |

File names follow `{{id}}_{{difficulty}}_{{stimulustype}}_{{algorithm}}.html`.

## Task list

| ID | Difficulty | Algorithm | Stimulus | Inconsistency side |
|----|-----------|-----------|----------|--------------------|
| E1 | easy | Sum of an array | statement + flowchart | statement |
| E2 | easy | Factorial (iterative) | statement + flowchart | flowchart |
| E3 | easy | Power (iterative) | statement + flowchart | statement |
| E4 | easy | Linear search | statement + code | code |
| E5 | easy | Maximum of an array | statement + code | statement |
| E6 | easy | Count occurrences | statement + code | code |
| H1 | hard | Bubble sort | statement + code | code |
| H2 | hard | Insertion sort | statement + code | statement |
| H3 | hard | Selection sort | statement + code | code |
| H4 | hard | Binary search | statement + flowchart | statement |
| H5 | hard | Merge sort | statement + flowchart | flowchart |
| H6 | hard | Quicksort | statement + flowchart | statement |
| W1 | warm-up | Swap two variables | statement + code | code |
| W2 | warm-up | Print 1 to n | statement + flowchart | flowchart |
| B1 | baseline | Minimum of an array | statement + code | — (consistent) |

See `ANSWER_KEY.md` for the exact inconsistency in each task.

## Usage

Open any task file in a browser at a **1920 × 980** viewport (or present it full-screen on a
1080p display). No build step, server, or dependencies are required — each file is standalone
HTML/CSS with inline SVG flowcharts.

> **Note for deployment:** the code panels currently include a `# BUG …` comment and a pink
> highlight marking the error. These are convenient for piloting and for the answer key, but
> they reveal the answer and should be removed before showing the stimuli to participants.

## How the stimuli were generated

The HTML, SVG flowcharts, and per-task layout tuning were produced programmatically. Flowchart
geometry is drawn with explicit, verified arrowheads; the statement font size and line height
are auto-tuned per task (via a headless-browser measurement pass) to (a) match the code/flowchart
surface area, (b) keep line pitch above the webcam-tracking threshold, and (c) guarantee no
overflow at 1920 × 980.

## Citation / contact

Part of the **eyesliketomove** project (multimodal cognitive-load sensing for e-learning, using webcam-based eye tracking).
Add your authors, affiliation, license, and a citation/DOI here before publishing.

<!-- Suggested:
## License
## How to cite
-->
