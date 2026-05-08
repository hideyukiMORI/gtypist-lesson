# gtypist-lesson

Touch typing practice scripts for [GNU Typist](https://www.gnu.org/software/gtypist/).

This repository contains two terminal lesson scripts:

- `xion.typ`: the original weak-finger etude collection.
- `keyquest.typ`: a GNU Typist adaptation of the first 28 implemented KeyQuest lessons.

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

`keyquest.typ` ports the first four implemented KeyQuest arcs into gtypist:

- Days 1-7, Novice Hall: home position, finger ownership, home-row accuracy, and the Gatekeeper Trial.
- Days 8-14, Meadow Road: top-row reach and the Waystone Trial.
- Days 15-21, River Gate: bottom-row movement, bridge keys, comma, period, and the Ferryman Trial.
- Days 22-28, Lantern Keep: number-row control, simple codes, map labels, and the Beacon Trial.

The original KeyQuest game presents these lessons through RPG progression, story scenes, scoring, and rewards. GNU Typist is a simpler terminal trainer, so this port keeps the typing substance and reshapes the experience into menus, concise training notes, and drill lines.

## Recommended Practice

Use one day per session. Repeat a day when accuracy feels unstable, especially during the first week. The early lessons are intentionally short and repetitive because KeyQuest prioritizes home position, finger responsibility, and calm accuracy before speed.

For a deeper curriculum map and maintenance notes, see [`docs/keyquest-curriculum.md`](docs/keyquest-curriculum.md).

## Author

The original `xion.typ` script was written by Hideyuki Mori of Ayane International Inc.

The `keyquest.typ` script adapts KeyQuest lesson content for GNU Typist.
