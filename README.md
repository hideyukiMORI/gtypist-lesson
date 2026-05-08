# gtypist-lesson

Touch typing practice scripts for [GNU Typist](https://www.gnu.org/software/gtypist/).

This repository contains two terminal lesson scripts:

- `xion.typ`: the original weak-finger etude collection.
- `keyquest.typ`: a 90-day GNU Typist typing journey adapted from KeyQuest.

## Requirements

Install GNU Typist before running these scripts.

### Debian / Ubuntu

```sh
sudo apt install gtypist
```

### macOS

```sh
brew install gtypist
```

## Quick Start

Run the KeyQuest journey directly from this repository:

```sh
gtypist keyquest.typ
```

Run the original weak-finger etudes:

```sh
gtypist xion.typ
```

## Optional Install Path

GNU Typist can load lesson files from directories listed in `GTYPIST_PATH`. Add this repository path to your shell profile if you want to run the lessons from anywhere:

```sh
export GTYPIST_PATH=/path/to/gtypist-lesson
```

Then run:

```sh
gtypist keyquest.typ
```

## KeyQuest Curriculum

`keyquest.typ` provides a full 90-day gtypist version of the KeyQuest journey:

- Days 1-28 preserve the implemented KeyQuest lesson prompts and reshape them for gtypist drills.
- Days 29-90 are gtypist-native extensions based on KeyQuest's official quest map themes.
- The journey covers 12 weekly arcs plus a 6-day finale, from home position through full-keyboard mastery.

The original KeyQuest game presents lessons through RPG progression, story scenes, scoring, and rewards. GNU Typist is a simpler terminal trainer, so this port keeps the typing substance and reshapes the experience into menus, concise training notes, and drill lines.

## Recommended Practice

Use one day per session. Repeat a day when accuracy feels unstable. The first month is intentionally repetitive because KeyQuest prioritizes home position, finger responsibility, and calm accuracy before speed. Later arcs add Shift, symbols, code-like patterns, longer phrases, recovery, and final integrated review.

For a deeper curriculum map and maintenance notes, see [`docs/keyquest-curriculum.md`](docs/keyquest-curriculum.md).

## Author

The original `xion.typ` script was written by Hideyuki Mori of Ayane International Inc.

The `keyquest.typ` script adapts and extends KeyQuest lesson content for GNU Typist.
