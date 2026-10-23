# 100 in 100: script rules

The series: Denis (21) has 100 days to open the world's first humanoid robot store, in a mall in Miami, by **December 1, 2026**, while growing his personal page. Each day's video is built from what he logs in the 100 in 100 Log form.

## Hard rules (never break)

- **Only real events.** Every line comes from the log entry. Never invent an event, a person, a quote, a number or a feeling. If the log is thin, write a shorter video, never a padded one. Put anything you had to assume in a `[bracket]` for Denis to fill.
- **No exact money figures.** No prices, rent, revenue, penalties or amounts raised. Say "a penalty every month" or "multiple six figures", never a number with a dollar sign.
- **Never name the company** (no brand name on screen, in speech or caption). It is "the store" or "a humanoid robot store".
- **Talk to people his age** (early 20s builders). Never address parents, never talk about kids as the audience. Kid classes can appear as an event, briefly.
- **No em dashes or en dashes** anywhere. Use periods, commas or parentheses.
- **Don't name suppliers or partner brands** (robot or printer makers, contractors, the mall's owner). Say "a robot company in China", "the contractor".

## Format

- **Length:** 30 to 45 seconds spoken (roughly 75 to 115 words of body).
- **Text hook (on screen):** always the day number plus a stake. Never a bare "Day 14". Pattern from Mino Lee's DAY 1 / DAY 32 reels (600K+), where a goal sat next to the number; plain day counts fell to 28K to 45K.
  - Good: `DAY 31: the robots still aren't here (45 days left)`, `DAY 40: we almost lost the store today`
  - Bad: `Day 31 of 100`
- **Spoken hook (first line):** short, open, creates a curiosity gap. Denis's favorite words are "disgustingly" and "disturbingly"; use one when it fits naturally, never forced. Avoid "but it gets increasingly more niche".
- **Story arc (his 5-step format):**
  1. Hook: the goal or stake for today
  2. The obstacle (what went wrong, from the log)
  3. What he actually did about it
  4. The turn: the moment it moved (or didn't)
  5. One honest line of lesson or feeling, then the close
- **Close / CTA:** `Follow to see if we open December 1.` (vary lightly: "if we make it", "if the doors open on time"). Optional comment prompt tied to the day.
- **Tone:** direct, a little self-aware, never corporate. Short sentences. Talk like a 21 year old telling a friend what happened.

## What to output for each day

Write a JSON object (one per day) into `scripts.json` with these fields:

```json
{
  "date": "2026-10-23",
  "day": 29,
  "textHook": "DAY 29: the robots still aren't here",
  "hooks": ["spoken hook 1", "spoken hook 2", "spoken hook 3"],
  "body": "Full spoken script, line breaks between beats. [B-ROLL: ...] cues in brackets.",
  "cta": "Follow to see if we open December 1.",
  "caption": "Caption text, one line plus an optional question",
  "shots": ["Shot list built ONLY from what the log says is on camera", "..."],
  "fillins": "Anything Denis must confirm or fill, or empty string",
  "sourceEntries": ["db document ids used"],
  "written": "2026-10-23T02:05:00Z"
}
```

If a day has several log entries, combine them into one script. If an entry already has a script and new entries arrive for the same date, rewrite that day's script with everything.

Inspiration links shown on every card: Mino Lee DAY 1 (`https://www.instagram.com/reel/C1kzUmsRcEl/`), DAY 32 (`https://www.instagram.com/reel/C23BpgAvnSH/`), and Denis's own Dec 1 deadline reel (`https://www.instagram.com/reel/Ddw9G7eyvfP/`).
