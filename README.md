# Cheems' Candy Factory · Sorting Game

A standalone educational HTML5 sorting game featuring Cheems the candy factory worker, teaching fundamental sorting algorithms: **Insertion Sort**, **Merge Sort**, and **Quick Sort**.

## How to Run
- Double-click [`index.html`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/index.html) to open directly in any modern browser (Edge, Chrome, Firefox, Safari).
- **100% self-contained**: Runs offline from `file://` with zero external assets, no server, Node.js, or Python needed.

## Features & Controls
- **Stage Select**: Choose your shift from the full-screen stage select menu (Insertion Line, Merge Mixer, Quick Splitter) or launch Tutorial. Cards show algorithm difficulty, best moves, and prominent DSA pills (`Insertion Sort`, `Merge Sort`, `Quick Sort`). Mid-game stage selection is accessible via the **Stages** button.
- **Stage Title Badge with DSA Name**: Prominent two-line stage chip in the sticky header showing the stage icon, stage name in Baloo 800 (22px), and an accented pill with the underlying algorithm name (`Insertion Sort`, `Merge Sort`, `Quick Sort`). Text contrast exceeds 10:1. Fits with zero horizontal overflow and header height well below 110px.
- **Factory HP Bar**: Prominent 5-segment health bar with heart icon. Wrong placements deduct 20 HP with visual shake and floating damage indicators.
- **Insertion Line**: Slide or click to place incoming candies into their correct sorted position on the tray. Sized responsively to fit on one row without scrolling.
- **Merge Mixer**: Compare the front items of Tray A and Tray B, dispensing the smaller candy into the mixer using click or keys `[A]` / `[B]`.
- **Quick Splitter**: The machine crowns a golden star candy (pivot). Route subsequent candies to the Smaller bin `[1]` or Bigger bin `[2]`. All components (star panel, pile, funnels, and both bins) fit on screen without vertical page scroll at 1513x728, 1440x800, and 1280x720.
- **Star Candy Contrast & Readability**: Candy numbers are rendered in cocoa font with crisp text shadows and guaranteed high contrast (≥ 4.5:1). The star pivot features a dark gold star shape, corner star badge, and gold outline.
- **Dynamic Random Candy Numbers**: Every round re-rolls fresh 2-digit numbers (`10–99`) with a pairwise gap of at least 3 (`minGap >= 3`) so neighbouring values are never confusing:
  - **Insertion Line**: 8 distinct candies with inversion count strictly between 8 and 20 (guaranteeing the pile is never pre-sorted and never completely backwards).
  - **Merge Mixer**: 8 distinct candies split evenly into Tray A (4) and Tray B (4), each pre-sorted ascending, with at least 3 source switches required to merge.
  - **Quick Splitter**: 7 distinct candies. The golden star is crowned when the timer fires from values at sorted rank 2, 3, or 4 (median-ish), guaranteeing at least 2 candies fall into both the smaller and bigger bins.
  - **Quick Star Timer Protection**: Clears pending star timers on reset, stage switch, and rapid restarts (tested with 20 restarts in 900ms) to prevent phantom star crowning.
  - **Deterministic Seeds**: Supports `?seed=N` in URL query parameters using the `mulberry32` PRNG for reproducible test runs and demonstrations.
- **Tutorial Mode with Step-by-Step Undo & Dynamic Presets**: Watch algorithms sort candies with fixed light-to-dark green shades, ring highlights, and plain-English captions. Controls are arranged strictly in DOM and Tab order: `▶ Play`, `↩ Undo`, `⏭ Step`, and `🔄 Reset`. Undo supports keyboard shortcuts `[Z]` and `[Backspace]`, allows rewinding out of the finished state, and restores counters, bars, and radio logs. Presets (Mixed-up, Almost sorted, Backwards, Twins with ≥ 2 repeated pairs) dynamically re-roll on reset, preset change, size change, and stage switch using Fisher-Yates shuffling.
- **Mouse-Only Gameplay**: Gameplay moves are strictly mouse-operated (clicking gumdrop slots / dragging candy for Insertion, clicking Push buttons / dragging for Merge, clicking Smaller/Bigger or dragging to funnels for Quick). Gameplay keys (Arrows, Enter, A, B, 1, 2) are removed to eliminate input ambiguity while utility keys (`[R]` restart, `[M]` mute, `[Z]` / `[Backspace]` undo, `[Space]` tutorial play/pause, `[Escape]` modals) remain responsive.
- **Factory Jam & Reconstruction**: Emptying Factory HP triggers an animated physics collapse. Click **FIX THE MACHINE** or press `[R]` to sweep up the sprinkles and restart clean.
- **"Built By" Credit Card**: Prominent project credit ticket located at the bottom-right of the factory floor inside the side column:
  - Header: Lemon pill with cupcake icon `🧁 BUILT BY`.
  - Name: **Pichayut Jeawpongpipat** in Baloo 800 on a single line.
  - Student ID: `68102010209` in Baloo tabular numerals.
  - Institution: **Srinakharinwirot University** in semi-bold Nunito.
  - Layout & Height: Page height is guaranteed not to increase (Factory Radio flexes and absorbs the card's space). Responds smoothly at 1250px into a full-width bottom strip and tumbles cleanly during jam collapse.
- **Shift Report**: Comprehensive end-of-stage evaluation with star rating, grade badge, efficiency stats, and direct navigation buttons.
- **Audio & Visuals**: Synthesized in real time using the Web Audio API with embedded pixel-art character sprites. Interactive sound effects (pops, clinks, whooshes, chimes) respond dynamically to gameplay. No ambient background drone.

## Deliverables & Verification
Screenshots are saved in the [`screenshots/`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001\DSA%20GAME\DSA%20GAME\EXPORT\screenshots) directory:
- **1280x720 Gameplay Screenshots (0 Vertical & Horizontal Scroll)**:
  - [`stage_select_1280x720.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/stage_select_1280x720.png)
  - [`insertion_1280x720.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/insertion_1280x720.png)
  - [`merge_1280x720.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/merge_1280x720.png)
  - [`quick_1280x720.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/quick_1280x720.png)
  - [`tutorial_1280x720.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/tutorial_1280x720.png)
- **"Built By" Credit Card Deliverables**:
  - [`credit_card_insertion_1440x900.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/credit_card_insertion_1440x900.png)
  - [`credit_card_quick_1440x900.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/credit_card_quick_1440x900.png)
  - [`credit_card_insertion_1280x720.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/credit_card_insertion_1280x720.png)
  - [`credit_card_quick_1280x720.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/credit_card_quick_1280x720.png)
  - [`credit_card_1100px.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/credit_card_1100px.png)
  - [`credit_card_close_up.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/credit_card_close_up.png)
- **Header & Navigation**:
  - [`header_insertion_1440px.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/header_insertion_1440px.png)
  - [`header_merge_1440px.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/header_merge_1440px.png)
  - [`header_quick_1440px.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/header_quick_1440px.png)
  - [`tutorial_controls_bar.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/tutorial_controls_bar.png)
  - [`stage_select_with_dsa_pills.png`](file:///C:/Users/iceje/Downloads/DSA%20GAME-20261009T072816Z-1-001/DSA%20GAME/DSA%20GAME/EXPORT/screenshots/stage_select_with_dsa_pills.png)
- **Test Suite Verification**:
  - `_build/run_driver_test.js`: **811 / 811 automated tests passing** with zero failures.
  - `_build/test_math.js`: **200 / 200 random seeds verified** with Grade S, 3 Stars, 100 HP under perfect play across Insertion, Merge, and Quick.
  - `_build/test_rapid_jam.js`: **15 / 15 rapid jam scenarios passing** with zero failures across all algorithms and recovery modes.
  - `_build/verify_credit_card.js`: Verified `scrollHeight <= baseline` across 1440x900, 1280x720, and 1513x728 for all 4 modes; card placement within 0.5px right delta; single-line name; collapse & reconstruct inline transform clearance; zero console errors.
