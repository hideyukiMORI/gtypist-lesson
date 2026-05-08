# KeyQuest Curriculum for GNU Typist

This manual explains how `keyquest.typ` adapts the first 28 implemented KeyQuest lessons to GNU Typist.

KeyQuest is designed as a terminal typing adventure. Its source lessons are JSON files with metadata, target keys, skill tracks, finger hints, and English prompts. GNU Typist uses a compact `.typ` script language, so this port turns the same curriculum into menus, banners, text notes, key introductions, and drill lines.

## How to Run

```sh
gtypist keyquest.typ
```

Choose an arc from the main menu, then choose a day. The lesson returns to its arc menu when complete.

## Adaptation Rules

- Each KeyQuest JSON lesson became one GNU Typist lesson block.
- KeyQuest prompt text remains English.
- Very short prompts are repeated on a drill line so gtypist practice is not too brief.
- `targetKeys` metadata becomes the gtypist `I:` key group for each drill.
- RPG systems such as XP, HP, MP, inventory, story gates, and achievements are not simulated in gtypist.
- Story flavor is kept as concise training framing so the screen stays calm while typing.

## Practice Philosophy

The first KeyQuest month is accuracy-first. Type slowly enough that each finger returns to home position after every reach. Do not chase speed during the early lessons. Repeat a day when the hand shape feels unstable.

## Arc Overview

### Novice Hall (Days 1-7)

The first week is intentionally stubborn: small patterns, mirrored pairs, home-row ownership, and accuracy before speed.

- Day 01: Novice Hall: Home Position - Learn the calm home stance and anchor both index fingers on f and j. Focus: home position, left index, right index, home row accuracy.
- Day 02: Novice Hall: Left And Right Balance - Balance left and right hands without rushing the home row. Focus: left hand balance, right hand balance, home row rhythm.
- Day 03: Novice Hall: Finger Responsibility - Reinforce which finger owns each home-row key. Focus: finger responsibility, home row ownership, calm correction.
- Day 04: Novice Hall: Rhythm Hall - Build a steady cadence with familiar home-row combinations. Focus: home row rhythm, spacing, steady cadence.
- Day 05: Novice Hall: First Words - Connect home-row drills to tiny readable English word groups. Focus: short words, home row posture, word accuracy.
- Day 06: Novice Hall: Repair The Stance - Repair weak-finger habits with slow, accurate review. Focus: weak finger repair, slow perfect typing, home row recovery.
- Day 07: Novice Hall: Gatekeeper Trial - Prove the first-week home-row basics in a gatekeeper trial. Focus: home row trial, accuracy check, calm recovery.

### Meadow Road (Days 8-14)

The second week expands into nearby top-row keys while repeatedly returning the hands to home position.

- Day 08: Meadow Road: First Steps Beyond Home - Step beyond home row with r, u, e, and i while returning home. Focus: vertical movement, nearby top row keys, return to home.
- Day 09: Meadow Road: Ring Finger Reach - Practice ring-finger top-row reach with w and o. Focus: ring finger reach, w and o, return to home.
- Day 10: Meadow Road: Index Reach - Practice index-finger reach with t and y in short patterns. Focus: index reach, t and y, controlled stretch.
- Day 11: Meadow Road: Outer Watch - Add the outer pinky top-row keys q and p carefully. Focus: outer reach, q and p, return to home.
- Day 12: Meadow Road: Top Row Trail - Travel across the top row in short lateral patterns. Focus: top row travel, lateral control, steady return.
- Day 13: Meadow Road: First Flow - Type short English word flow using home row and top row. Focus: short word flow, top row words, calm rhythm.
- Day 14: Meadow Road: Waystone Trial - Check top-row control in a deliberate Waystone Trial. Focus: weekly checkpoint, top row control, accuracy under pressure.

### River Gate (Days 15-21)

The third week adds bottom-row movement, bridge letters, and the first punctuation checkpoint.

- Day 15: River Gate: Lower Step - Introduce lower-step movement with c and m. Focus: bottom row introduction, c and m, return to home.
- Day 16: River Gate: Valley Reach - Practice valley reach with v and n while keeping hands quiet. Focus: bottom row reach, v and n, index control.
- Day 17: River Gate: Bridge Keys - Bridge rows around b, g, and h without drifting from home. Focus: index bridge, b and g h, center control.
- Day 18: River Gate: Comma And Period - Add comma and period practice with the right hand. Focus: comma, period, right-hand punctuation.
- Day 19: River Gate: Bottom Row Words - Use bottom-row words inside short readable phrases. Focus: bottom row words, mixed rows, accuracy.
- Day 20: River Gate: Current Review - Review mixed rows and punctuation with calm recovery. Focus: mixed-row review, punctuation review, steady cadence.
- Day 21: River Gate: Ferryman Trial - Cross the Ferryman Trial for bottom-row and punctuation control. Focus: weekly checkpoint, bottom row control, punctuation under pressure.

### Lantern Keep (Days 22-28)

The fourth week introduces digits in small groups before mixing them into readable English prompts.

- Day 22: Lantern Keep: Left Number Row - Introduce the left number row with 1, 2, 3, and 4. Focus: left number row, upper reach, accuracy.
- Day 23: Lantern Keep: Right Number Row - Introduce the right number row with 7, 8, 9, and 0. Focus: right number row, upper reach, rhythm.
- Day 24: Lantern Keep: Center Span - Practice the center number span with 4, 5, 6, and 7. Focus: center number row, index reach, steady return.
- Day 25: Lantern Keep: Counts And Codes - Type short counts and codes without losing home-position shape. Focus: number words, short codes, accuracy under context.
- Day 26: Lantern Keep: Map Marks - Practice map labels and room numbers as practical digit prompts. Focus: map labels, mixed rows, number accuracy.
- Day 27: Lantern Keep: Mixed Signals - Mix number-row instructions while keeping rhythm stable. Focus: mixed number row, short instructions, steady cadence.
- Day 28: Lantern Keep: Beacon Trial - Clear the Beacon Trial for number-row control. Focus: weekly checkpoint, number row control, mixed instruction accuracy.

## File Map

- `keyquest.typ`: GNU Typist script for the KeyQuest 28-day journey.
- `xion.typ`: original weak-finger etude script, kept unchanged.
- `README.md`: installation and quick usage guide.
- `docs/keyquest-curriculum.md`: this curriculum manual.

## Maintaining Future Lessons

When new KeyQuest lessons are added, keep the gtypist version small and explicit:

1. Add the day to the appropriate arc menu or create a new arc menu.
2. Add one `*:DAY_NN` label for the lesson.
3. Use `B:` for the day title and `T:` lines for the practice goal.
4. Use `I:` to introduce target keys before each drill.
5. Use `D:` and continuation lines starting with ` :` for the actual typing text.
6. End the lesson with `G:` back to the arc menu.

Keep drill lines readable in a normal terminal. If a KeyQuest prompt is extremely short, repeat it several times. If it is long, split it into multiple gtypist continuation lines.
