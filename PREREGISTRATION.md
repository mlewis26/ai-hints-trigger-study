# Preregistration: Does a Physical Tap Trigger Change How I Use AI for Learning?

**Author:** Madison Lewis
**Date registered:** October 22, 2026 (before any A1 data were collected)
**Design:** Single-case ABAB (withdrawal) design, n = 1

## Research question

Does using a physical tap trigger (the Tri) that switches my AI tools into hints-only mode change how I use AI, and how much I remember from what I learned with it?

## Hypotheses

1. **Hints mode:** During Tri phases (B1, B2), I will only use hints mode: every AI session will be in hints mode.
2. **Outcome:** A higher percentage of sessions will end with me reaching the answer myself (Outcome = Me) during Tri phases.
3. **Recall:** I will be able to explain what I learned the previous day ("Could explain it?" = Yes) more often during Tri phases.
4. **AI minutes:** No directional prediction. Daily AI minutes will be reported, but I don't have a strong reason to expect them to go up or down.

## Phases

| Phase | Dates | Tri? |
|---|---|---|
| Pilot | Oct 20–22 | No (practice only, not analyzed) |
| A1 | Oct 23 – Nov 4 | No |
| B1 | Nov 5 – Nov 18 | Yes |
| A2 | Nov 19 – Dec 2 | No |
| B2 | Dec 3 – Dec 16 | Yes |

Phase dates are fixed in advance and will not be moved based on the data. One exception, set now: if a phase has 4 or more days missing or disrupted (for example, illness or travel), that phase will be extended by one week, and the change will be listed under Deviations.

## Intervention (the Tri)

The Tri is a small triangle-shaped object that I tap with my phone to switch Claude on my Mac and iPhone into hints-only mode. The general idea of a physical tap object that changes how a phone works comes from existing consumer focus devices; this study adapts it to set AI tools to hints-only for learning. It will be built by November 4, before B1 starts. The exact build will be documented in this repository before B1 begins. During A phases, the Tri is put away and I use AI normally.

## Scope

- **AI tool:** Claude, in one ongoing conversation.
- **Devices:** Mac (main) and iPhone.
- I will use AI normally and not change my habits because I'm tracking them.

## Measures

**Sessions tab** (one row per topic, not per sitting):
- Date, start time, device, app, purpose (Coding, School, Admin, Personal, Other)
- **Hints mode (Yes/No):** "Yes" if I asked for hints only, or used the Tri or a learning mode, *before* the AI started helping with that topic. If I switch to asking for full answers partway through, the row stays "Yes," and the switch shows up in the Outcome column.
- **Outcome:** Me = hints led me to the answer; AI = it gave me the answer; Mixed = some of each.

**Daily tab** (one row per day, each evening):
- **AI minutes:** total minutes in AI apps and sites from Screen Time (Mac + iPhone, "Share across devices" on).
- **Recall:** write one thing I learned with AI the day before, then try to explain it without looking.
- **Could explain it?** Yes, Partly, or No.

## Analysis plan

**Which data:** All session rows from A1, B1, A2, and B2 are included in the main analysis, whatever the purpose. Pilot data are excluded.

**Primary measures:** % of sessions in hints mode and % of sessions with Outcome = Me, calculated for each day and for each phase.

**Secondary measures:** % of days with recall = Yes, and average AI minutes per day, by phase.

**Method:**
1. Plot each measure by day, with phase change lines (standard single-case graphs).
2. Visual analysis of level, trend, and variability within and across phases.
3. Report phase means and the percentage of non-overlapping data (PND) between each adjacent pair of phases.

**What counts as support for H1:** 100% of sessions in B1 and B2 are in hints mode. Any session that is not will be reported, with the reason if I know it.

**What counts as support for H2–H3:** The measure goes up from A1 to B1, down from B1 to A2, and up again from A2 to B2. That gives three demonstrations of the effect. If only some of the changes appear, I'll report the result as mixed.

**Exploratory (not confirmatory):** The same measures broken down by purpose, especially Coding and School alone, since hints-only fits learning tasks best.

## Missing data

Days with no AI use are logged with 0 minutes, and no session rows are added. Missed logging days are left blank and reported, not filled in afterward from memory.

## Limitations

- One participant, and I'm both the researcher and the participant, so I'm not blind to the phase.
- All measures are self-reported, and tracking itself may change my behavior.
- An ABAB design assumes the effect can reverse when the Tri is removed. If I learn lasting habits in B1, A2 may not return to baseline.
- Results won't generalize to other people. This is a pilot for a possible larger study.

## Deviations

Any change to this plan after October 22, 2026 will be listed here with the date and the reason.

##| Date | Change | Reason |
#| Oct 27, 2026 | Session rows for Oct 23-26 were entered from the conversation's exported timestamps instead of each evening. Recall for Oct 23-26 is missing | Daily logging was missed those days. Daily logging resumes Oct 27 |
#| Oct 27, 2026 | Recall changed from a self-rated Yes/Partly/No to a 3 question quiz (0-3) on yesterday's first Coding/School topic, plus a weekly 1 week delayed quiz (Sundays). Added need for cognition (Oct 27, then end of each phase) and a 3 problem no AI Python test (end of each phase.) | More objective learning and retention measures. NFC baseline is mid A1, not before A1.|
