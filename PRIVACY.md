# Privacy — Cave Aurora Edge

**Short version: nothing leaves your PC. There is no account, no telemetry and no
analytics. Neither the widget nor the companion app sends anything to the internet.**

## What the widget stores

The widget keeps its data in the browser storage iCUE provides for it, under the
`cave-aurora-edge` name, on your own PC:

| Key | Contents |
| --- | --- |
| `tasks` | Your tasks: title, description, due date, duration, priority, and whether and when each was completed |
| `task-memory` | Titles, descriptions, durations and priorities of tasks you have saved before, for suggestions |
| `task-stats` | Your running count of completed tasks and the planned time credited when tasks are ticked off by hand |
| `stopwatch` | Whether the work timer is running, its start time, time worked so far and your goal |
| `break-timer` | Break end time and the number of breaks taken |
| `work-settings` | Break length, reminder settings, automatic logging, and the task the current session is for |
| `work-session-history` | Logged sessions: start and end times, time worked, paused time, breaks, goal and linked task or project |
| `timer-memory` | Names you have given countdown timers before, so they can be picked again instead of retyped |
| `preferences` | 12- or 24-hour clock, Movie Mode brightness, colour theme, how you arranged the panels, any countdown timer still running, and your last chosen sound output and media app |

None of it is ever transmitted. **Options → Reset all data** deletes all of it, and
removing the widget from iCUE removes it too.

## What the widget reads

Track and artist come from iCUE's official Media Data Provider. Everything else comes
from the companion app, below. The widget does not store media information.

## What the companion app does

The Cave Aurora Edge companion app is a Windows program that runs on your own PC. It:

- listens only on `http://127.0.0.1:47142`, your own PC, so nothing on your network or
  the internet can reach it, and refuses requests from websites;
- reads your sound devices' names, volume and mute state, and changes them when you tap;
- reads what Windows media sessions are playing (title, artist, app, artwork and
  position) and sends play, pause, skip and seek commands when you tap;
- reads CPU, GPU, RAM and network usage;
- reads how many Windows notifications you have. It reads the count only, never their
  content;
- reads the XENEON EDGE Screen Setup keyboard shortcuts from iCUE's settings file,
  without changing them, and presses them only when you tap the display-mode button or
  swipe between screens;
- presses Windows + D when you tap Show desktop, opens iCUE when you tap Open iCUE, opens
  Task Manager when you tap that button, and opens the Tom's Cave shop page in your web
  browser when you tap that button;
- locks, shuts down or restarts Windows — and only when you press and hold that button on
  the dashboard;
- keeps the shortcuts you add, and starts them when you tap one. Adding one opens a normal
  Windows file box on your desktop for you to choose in; the app never searches your PC on
  its own, and only ever starts something you added yourself. It reads the program's own
  icon from the file you picked, so the tile can show it.

It keeps no history of what you play, read or run. The files it writes are all in
`%LOCALAPPDATA%\CaveAuroraEdge\` on your own PC, and none of them is ever sent anywhere:

| File | Contents |
| --- | --- |
| `shortcuts.json` | The shortcuts you added: the name, and the path of the program, folder or web address each one points at |
| `origins.log` | A short diagnostics list of the kinds of program that have contacted it (for example `file://` for iCUE), capped at 50 lines |
| `power-audit.log` | A line for each lock, shut down or restart asked for, so an unexpected one can be accounted for. Capped, and it records the action and the time only |
| `bridge-start.log` | The last 20 times the app started or failed to start, for working out why it is not running |

Removing the companion app through **Settings → Apps** deletes the program; you can delete
that folder to remove these files as well. The installer writes a log to your temporary
folder if something goes wrong.

## Third parties

There are none: no SDKs, crash reporting, advertising or analytics.

## Your rights

No personal data is collected or transmitted, so there is nothing for Tom's Cave to
disclose, export or erase on request. Everything the Software knows is already on your
own PC and under your control.

## Contact

<https://github.com/Caveproduction-bot/cave-aurora-edge/issues>
