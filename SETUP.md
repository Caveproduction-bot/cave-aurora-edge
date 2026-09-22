# Setting up Cave Aurora Edge

Setup takes about two minutes. You need Windows, iCUE 5.47 or later, and a CORSAIR
XENEON EDGE.

## 1. Add the widget to your XENEON EDGE

1. Get **Cave Aurora Edge** from Elgato Marketplace. iCUE installs it for you.
2. In iCUE, open your **XENEON EDGE** and go to the **Widgets** page.
3. Add **Cave Aurora Edge** to a screen and give it the whole screen (the largest size).

The clock, the countdown timer, tasks, work sessions, colours and the CPU and GPU
readings all work straight away, with nothing else installed.

## 2. Install the companion app

The free **Cave Aurora Edge companion app** is what lets the dashboard reach Windows. It
powers the sound controls, media details, RAM and network readings, notifications, Show
desktop, the display-mode button, Task Manager, Lock / Shut down / Restart, and your own
shortcuts.

1. Download **CaveAuroraEdgeBridge-Setup.exe** from the Related Download link on the
   store page, or from
   <https://github.com/Caveproduction-bot/cave-aurora-edge/releases/latest>.
2. Run it. Windows SmartScreen may warn you because the app is not code-signed: choose
   **More info → Run anyway**.
3. It installs for your user only, starts straight away and starts with Windows from
   then on. There is no window — it runs quietly in the background.

The dashboard notices within a second or two: the greyed-out controls come to life and
the readings fill in.

**Version 1.0.5 or later** is needed for shortcuts to a website. Anything the companion
app cannot do yet is said on screen rather than left blank.

To remove it: **Settings → Apps → Cave Aurora Edge Bridge**, or run the installer with
`--uninstall`.

## 3. Choose your look in iCUE

Cave Aurora Edge is coloured from iCUE, in the same place as every other widget. Select
**Cave Aurora Edge** under **Widgets**, then **Cave Aurora Edge Personalization**:

- **Background** — five to choose from. **Midnight Aurora** (the default) is deep navy
  into aubergine; **Ember Aurora** is the same idea in warm red; **Total Eclipse** is
  much darker, so almost all the light on screen is the glow; **Violet Nebula** and
  **Graphite Slate** are quieter.
- **Accent Color** — any colour you like. It sets the glow behind Focus & Tasks, the
  buttons, the sliders and the graphs. Six ready-made ones: blue `#5BA6D9`, violet
  `#8B78D5`, emerald `#51A783`, amber `#D18A3D`, crimson `#C85A67`, graphite `#A7B2C0`.
- **Text Color** — the dashboard's text. The original is `#F1F5FA`.
- **Background Transparency** — fades the background and panels so the iCUE page shows
  through, while text, numbers and buttons stay at full strength. It starts at 100%.

The dashboard changes as you pick. Whatever you choose is checked for readability and
nudged if a combination would be hard to read, so it never ends up unreadable. The
dashboard's own **Options** names the colours you started with, so you can always get
back to them.

iCUE's **Pages Personalization** (Theme per Page, Widget Text Color, Widget Accent Color,
Widget Background, Widget Transparency) does not change this dashboard, on purpose:
those settings dim a widget on a new page and hide its own choices.

## 4. Where the readings come from

These are found for you and need no setup. **Options → System readings** always names
the source behind each figure. If you would rather choose, select **Cave Aurora Edge**
under **Widgets** in iCUE and use **System Readings**:

- **CPU Source**, **GPU Source**, **RAM Source** each start on **Automatic**. Change one
  to **Manual** and pick from the sensors on your PC in the row below it. The sensor row
  is only read when its Source says **Manual**.
- Only the reading you change is affected; the rest stay automatic. If a sensor you
  picked is no longer there, that reading goes back to Automatic.
- **Network Source**: **Automatic** measures whichever connection is carrying traffic.
  Choose **Ethernet** or **Wi-Fi** to measure that one. The box is labelled ETHERNET or
  WI-FI so you can see which is being measured.

iCUE has no sensor for system RAM on most PCs, and none at all for network speed, so
those two come from the companion app. A reading with no source shows **N/A** with a
note saying where to fix it — it is never left blank.

## 5. Display mode and swiping between screens

The display-mode button in the clock card, and swiping left or right to change iCUE
screen, both press the keyboard shortcuts you set in iCUE.

1. In iCUE, open your **XENEON EDGE** and go to **Screen Setup**.
2. Set **Switch Display Mode**, **Previous Display Screen** and **Next Display Screen**.

Until they are set, the dashboard says so rather than doing nothing.

## 6. Your own shortcuts

Tap **+** on the SHORTCUTS panel. Up to eight, four on screen at a time with arrows for
the rest.

- **FIND A PROGRAM…** opens a normal Windows file box on your desktop. Pick a program
  (`.exe`), a Start Menu shortcut (`.lnk`) or a saved web link (`.url`) and it is added
  straight away.
- **FIND A FOLDER…** is the same for a folder — Windows file boxes list files *or*
  folders, never both, which is why there are two buttons.
- Or **paste** a full path, or a web address like `https://youtube.com`, and press SAVE.

Each tile shows the program's own icon and its name, and launches it with one tap. Tap a
shortcut in the pop-up's row to point it somewhere else or remove it, or tap **REARRANGE**
and then two tiles to change their places.

Scripts (`.bat`, `.cmd`, `.ps1`, `.vbs`) and network paths are refused on purpose: the
companion app runs these with no arguments, and a file full of commands is not a program.

## 7. Arrange the panels

Tap **LAYOUT** in the clock card, then drag a panel onto another to swap the two. Music
and the clock are the tall pair, SHORTCUTS and PC CONTROLS the short pair; a panel keeps
its own size wherever it goes, so it can move up or down its own column, or across to the
panel that is the same size. **RESET** puts everything back, **DONE** leaves.

## 8. Lock, shut down and restart

**LOCK** is one tap. **SHUT DOWN** and **RESTART** have to be pressed and held until the
ring fills, so a stray touch on a screen at desk height cannot end your session. Let go
early and nothing happens.

## Troubleshooting

**Controls are greyed out and readings show N/A.** The companion app is not running.
Start **Cave Aurora Edge Bridge** from the Start menu, or reinstall it.

**The installer said it could not start the app.** Its own log says why:
`%LOCALAPPDATA%\CaveAuroraEdge\bridge-start.log`. The most common cause is another copy
still holding the port — wait a few seconds and run the installer again.

**A shortcut says "Not found".** The program has moved or been uninstalled. Tap **+**,
tap that shortcut in the row, and point it somewhere else or remove it.

**A web address will not save.** It has to start with `http://` or `https://` and name a
site. Other kinds of address are refused on purpose.

**The display-mode button or swiping says the shortcuts are not set.** See step 5.

**Nothing at all appears in iCUE after installing the widget.** Remove the widget from
the screen, import it again and add it back. iCUE keeps per-widget settings otherwise.

## Privacy

Nothing leaves your PC. No account, no telemetry, no analytics. The full policy is in
[PRIVACY.md](PRIVACY.md).

## Support

<https://github.com/Caveproduction-bot/cave-aurora-edge/issues>
