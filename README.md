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
