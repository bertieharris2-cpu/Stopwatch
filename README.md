# Stop the Clock

A classroom version of the "stop the stopwatch on exactly 10.00 seconds" game.
Big green LED-style digits (minutes : seconds . hundredths, like a gym timer), one button: press to start, press to stop, press again to reset.

It is a single file, `index.html`. No installation, no internet needed once it is on the laptop
(it will use a fallback font if offline).

## Running it

- **Easiest:** download `index.html` and double-click it. It opens in Chrome or Edge.
- **From a web address:** in this GitHub repo go to *Settings → Pages*, choose "Deploy from a branch",
  pick the branch and `/ (root)`, and save. You get a link like
  `https://<your-username>.github.io/Stopwatch/` that works on any school computer.

Click **Full screen** before playing on the projector or interactive whiteboard.

## How it plays

| Press | What happens |
|-------|--------------|
| 1st   | Clock starts |
| 2nd   | Clock stops, shows how close you were (e.g. `00:10.03`, "0.03 s late") |
| 3rd   | Clock resets to `00:00.00`, ready for the next pupil |

- **Target time:** 1, 3, 5, 10, 20, 30, 60 seconds, **Random**, or type your own (0.5 to 99 s).
- **Hide the clock:** makes it much harder. The digits turn to `--:--.--` after 1 s, 3 s, halfway, or
  straight away, so pupils have to count in their heads. The real time is revealed when they stop.
- **Player:** type a name (press Enter when done) and it goes on the scoreboard.
- **Scores:** top 10 closest for the current target, plus the last 10 goes. Scores are saved
  in that browser on that computer only.
- Presses that come in less than ~0.15 s after the last one are ignored, so a bouncy switch or a
  double-tap can't stop the clock instantly or skip the result.
- Results are shown to the hundredth of a second, timed from the moment the browser receives the key press.

## The button

The page treats **almost any key** as "the button" (Space, Enter, letters, numbers, arrow keys,
Page Up/Down...). It also works with **USB game controllers / arcade buttons**, and with a mouse
click or touch on the clock. So the button does not need any set-up: whatever key it sends will work.

Things that work, and what to search for on Amazon:

1. **USB big button / "one key keyboard"** – search *"USB big red button keyboard"*,
   *"single key USB keyboard"* or *"1 key USB macro keyboard"*. A big dome push button on a lead that
   plugs into USB and acts like a keyboard key. Best match for the YouTube look.
2. **Arcade button kit** – search *"arcade buttons USB encoder kit"* or *"zero delay USB encoder"*.
   Cheap big chunky buttons (often light up) that show up as a game controller. You need to
   mount the button in a box or tub, which could be a nice DT project.
3. **USB foot pedal / foot switch** – search *"USB foot switch pedal"*. Pupils stamp on it. Tough.
4. **Presentation clicker** – search *"wireless presenter clicker"*. Wireless, and you might already
   have one. Smaller button, but it works straight away.

Avoid anything described as needing its own app on a phone (e.g. some Bluetooth "smart buttons").
You want something that plugs into the computer and types a key, or appears as a game controller.

Keys that are deliberately ignored: Tab, Esc (closes the scores panel), F1–F12, and anything held with
Ctrl/Alt/Cmd. Key presses are also ignored while you are typing in the name or target box,
so press Enter after typing.

---

# Stop the Clock Lab (version 2)

`lab.html` is a second version for collecting data from a whole class. The original `index.html` is unchanged.

**Pupils.** Paste a class list into *Pupils*, one name per line (initials or pupil numbers work too).
The current pupil's name is shown above the clock. Use ◀ ▶ or click a name to change turn.
*Shuffle the order* mixes up the turn order. The list shows how many goes each pupil has had in this session.

**Set-up.** Everything chosen here is saved with every go:

- **Target time**
- **Start the clock:** when the pupil presses, or after a 3, 2, 1 (or 5 second) countdown. With a countdown
  the clock beeps each second and starts itself exactly on GO, so the pupil only presses once, to stop it.
  Pressing before GO shows "Too soon!" and nothing is recorded.
- **Clock while running:** shown, or hidden after 1 s, 3 s, halfway, or from the start
- **After each go, show the pupil:** *Time and how close*, *Time only*, or *Nothing*. With *Nothing*
  the clock stays as `--:--.--` and the screen just says "Go 3 recorded".
- **Move to the next pupil:** when you choose, or automatically after 1, 2, 3, 5 or 10 goes
- **Session or group**, e.g. "5B science"
- **Condition**, e.g. "eyes closed" or "counting aloud", for comparing conditions in a fair test
- **Practice goes:** while this is ticked, goes are not recorded

The strip under the clock always shows what is being recorded.

**After each go** you can click *Mark as anomaly* (for example if the button was pressed by accident)
or *Delete this go*.

**Data** shows every go, newest first, with a filter for session and pupil.

- Tick **Anomaly** to leave a go out of the summary without deleting it. Click **Delete** twice to remove it.
- **Summary** shows one row per pupil, target and condition: number of goes, mean, median, lowest,
  highest, range, mean distance from the target and closest go. Anomalies are left out.
- **Download for Excel (CSV)** downloads whichever table is showing, with the current filters.
  The "Every go" file has one row per go, with these columns: Date, Time, Session, Pupil, Go, Target,
  Result, Difference (+ late, − early), Distance from target, Early or late, Condition, Start,
  Clock while running, Pupil was shown, Anomaly, ID.
- **Copy table** copies it so you can paste straight into Excel.
- **Restore from a CSV file** loads an "Every go" download back in, for example on another computer.
  Goes that are already there are skipped.

Data is kept in that browser on that computer only. Nothing is sent over the internet.
Download a CSV at the end of each lesson as a backup, because clearing the browser's history can delete it.
