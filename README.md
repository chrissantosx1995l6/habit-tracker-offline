# habit-tracker-offline

I wanted a simple habit tracker that runs entirely in my terminal, works offline, and gamifies my daily tasks with XP, levels, and streak tracking. This script keeps everything in a local SQLite database inside your home directory.

## Installation

No external packages are required. Just clone the repo and drop the script into your path.

```bash
# Put the script somewhere in your PATH
cp habit_tracker.py /usr/local/bin/habit
chmod +x /usr/local/bin/habit
```

On Windows, you can run it directly with python:

```powershell
python habit_tracker.py --help
```

## Usage

Define a new habit with XP rewards and an optional daily target:

```bash
python habit_tracker.py add "read-books" 15 --target 1
python habit_tracker.py add "leetcode" 25
```

Log progress for a habit:

```bash
python habit_tracker.py track "read-books" 1
```

Show your current level, total XP, streaks, and a weekly history grid:

```bash
python habit_tracker.py status
```

To view all raw logged records:

```bash
python habit_tracker.py log
```

## Database

The tool stores data in `~/.habits.db`. If you want to back up or sync your habits across machines, just copy this file.

<!-- checked: 2026-09-20 -->
