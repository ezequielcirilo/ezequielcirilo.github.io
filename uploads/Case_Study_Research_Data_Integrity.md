# Case Study: Research Data Integrity (v2)

**For:** Portfolio site, case study page. Upload this file to Claude Design as the build brief.
**Card this belongs to:** "Research Data Integrity" (renamed from Participant QA / Monitoring).
**Platform:** Rendered copy anonymises the platform as "an internal research operations platform." Do not print the internal product or module name anywhere on the page. Do not name any client, brand, or panel provider.
**Verb note:** This was a 0-to-1 product and design lead. Contribution is framed as product judgement, problem definition, and design leadership. Engineering built the parser and detection. No verb claims that AI or data engineering was done personally.
**AI-claim scope (defensibility):** The detection is mostly behavioural (speed, straightlining, task engagement, brand compliance, tester accounts). An LLM is used specifically to analyse the open-ended free-text answers, surfacing duplication and shared language patterns across participants. The copy is written to claim exactly that and no more. Do not let any wording imply the whole detection engine is AI.
**Length:** Rendered narrative is roughly 455 words, sized for a recruiter who will scan, not study.
**Imagery:** No live interface capture this round. Every interface visual is a described placeholder (see Part 2 and Part 3). Claude Design should render each as a clean framed placeholder with the description as its caption, ready for a real screenshot or an abstracted illustration to drop in later.

---

## PART 1: THE COPY THAT RENDERS ON THE PAGE

### Page title
When the participants aren't people

### Subtitle / dek
Research samples are increasingly polluted by bots and AI-generated responses. This module turns automation back on the problem: behavioural detection, an LLM reading the free-text answers where fakes hide, a human on every exclusion, and the evidence trail a panel demands before it will remove anyone.

### Context
The people who take unmoderated studies are no longer reliably people. Research samples are increasingly contaminated by bots, fraud farms, and participants who use AI to write their answers, alongside the familiar speeders, straightliners, and internal test accounts. Left in the dataset, these responses do not just add noise. They move the benchmark KPIs the business sells to clients as a comparative measure. And the newest offenders are the hardest to spot, because a participant pasting AI-written text into every open-ended question looks perfectly fine on the surface.

### The problem
Screening them out was a daily manual ritual: export the panel file, build pivot tables, run open-ended answers through ChatGPT to catch duplication, cross-reference lookup tables by hand. And catching a bad participant was only half the work: the panel would not remove a respondent without proof, so every exclusion had to be documented by hand into a package the panel would accept. Across up to ten concurrent studies it cost hours of senior time a day, thresholds lived in people's heads, and once someone was excluded the evidence was gone.

### The bet
The obvious brief was "automate the spreadsheet." I rejected it. The judgement in the process is real: a person reading a clickstream can tell a participant who abandoned a task from one whose session timed out. Automating that away trades one quality problem for another and never earns the team's trust. The bet I made instead: machines do the detection, humans do the judgement, and the system remembers both.

### The design
Most of the signals are behavioural: speed, straightlining, task engagement, brand compliance. The hardest to catch, and where AI-generated answers reveal themselves, is the free text, so that is where an LLM does the reading, surfacing duplicated and machine-written open-ends across participants, a comparison no human could run by hand at scale. Review is exception-based: the reviewer sees only participants who tripped a check, and every flag renders its proof, never a black-box score. Every automated decision is overridable, every override recorded with its reason and the strictness in force, and finalised days are read-only, producing the exact evidence package the panel requires.

### Outcome
A daily review that once took multiple hours per study now takes under fifteen minutes. Spreadsheet work went to zero, every exclusion traces to specific evidence in the format the panel accepts, and participant quality moved from an informal practice in people's heads to a governed, auditable capability of the platform.

### Takeaway
The ask was to speed up a spreadsheet. The real problem was an AI-era collapse in sample quality with no defensible way to police it. Naming that correctly, turning AI on the one signal humans could not scale, and keeping a person on every call, is what made it trustworthy.

---

## PART 2: BUILD DIRECTIONS FOR CLAUDE DESIGN

There is no live interface capture in this pass. Do not attempt to visit any URL. Every interface visual below is a placeholder: render it as a clean framed box, matching the site's visual system (thin strokes, generous whitespace, single rust accent), with the supplied description shown as the caption. Ezequiel will later drop in either a redacted real screenshot or an abstracted illustration in that same style.

Layout intent: keep the reading column narrow and the copy primary. Visuals support the narrative, they never lead it. One highlighted element per visual, the single rust accent used sparingly.

### Where each visual sits

**[PLACEHOLDER 1: HERO, above the title]**
Depicts: the study triage list. All monitored studies in one table, sorted queue-first so the studies needing attention float to the top. Three summary counts sit across the top (active studies, queue ready, awaiting review), and each row carries a status pill (Awaiting first upload, Queue ready, Up to date). The point this image makes: a reviewer knows where the day's work is before reading a single row.
Caption: "Portfolio state in three numbers, and a queue-first sort that puts the day's work at the top."

**[PLACEHOLDER 2: DIAGRAM, between "The bet" and "The design"]**
Build the detection-to-record flow specced in Part 4. This is the conceptual centre of the piece and should be a built diagram, not a placeholder box.

**[PLACEHOLDER 3: the detection checks table, beside "The design"]**
Depicts: the list of detection checks and their default action (Speeder, Outlier, Straightlining, Open-ended length, Open-ended duplication same-question and across-questions, Task not attempted, Tester, Segment compliance). Ezequiel has a clean, client-safe version of this table already, so this one can be a real asset rather than an illustration. Foreground the two open-ended duplication rows as the AI-powered checks (a small "LLM" tag or accent), since they carry the "fighting AI with AI" point.
Caption: "Ten checks. Most read behaviour. The open-ended ones read the text, where AI-written answers give themselves away."

**[PLACEHOLDER 4: the evidence panel, beside "The design" or just below Placeholder 3]**
Depicts: a single flagged participant's detail panel, showing the inline evidence that makes a defensible call possible and forms the package the panel requires. Multiple proof blocks stacked: a horizontal bar of this participant's completion time against the study median with the threshold marked; an answer-sequence strip with the straightlined run highlighted; the participant's verbatim open-ended answers; a compact per-task engagement table. This is "evidence, not verdicts" made visible.
Caption: "Every flag renders the proof that produced it, the same proof the panel needs to act on the exclusion."

**[STAT ROW: directly under "Outcome"]**
Pull the numbers into a scannable row, not buried in prose. Four items, rust accent on the figures:
- Under 15 min daily review, down from multiple hours
- 0 spreadsheet steps in the daily workflow
- 100% of exclusions evidenced in the panel's own format
- 10 detection signals, with LLM analysis on the free-text answers
Keep units small and secondary so the figures dominate.

---

## PART 3: PLACEHOLDER AND CONFIDENTIALITY RULES

**Placeholders (this round)**
- Render each interface placeholder as a framed, empty box in the site's visual style, with the description as its caption, sized to the aspect ratio the final image will use. This lets the page layout be reviewed and approved before any real image exists.
- Placeholder 3 (the checks table) is the exception: Ezequiel has a client-safe version and may drop it in as a real asset.
- Keep all placeholders on one consistent landscape ratio for full-view images and one tighter ratio for the stat and summary strips, so the page reads as designed once images land.

**When real screenshots replace the placeholders (later, by Ezequiel)**
- The public site anonymises the platform and names no clients. Before any screenshot is used, blur or redact: client and brand names, any participant PII (names, emails, account numbers), and the internal product or module name if it appears in the chrome.
- If a screen cannot be shown without exposing client-identifying data even after redaction, use an abstracted illustration in the site style instead.
- When in doubt, redact more. A slightly emptier screenshot is fine; an exposed client name is not.

---

## PART 4: DIAGRAM SPEC (Placeholder 2, the detection-to-record flow)

Build a clean flow that shows detection narrowing the many to the few, the human deciding, and the record making it defensible. Match the site's visual language: thin strokes, single rust accent, rounded nodes, no heavy fills. It must stay legible when it stacks to one column at 375px.

**Nodes and flow, left to right:**
1. "Daily panel file uploaded" (labelled as the single source of truth)
2. "Automated detection" with two grouped sub-labels: "Behavioural checks: speed, straightlining, engagement, compliance" and, set slightly apart with a small accent tag, "LLM: reads the open-ended answers for duplication and machine-written text." The AI tag here is what carries the "AI vs AI" story, keep it visible but secondary to the human node.
3. A visual split into two paths:
   - The large majority: "Passed. Counted, not shown." Render this path quiet and de-emphasised, thin and grey, to convey exception-based review.
   - The minority: "Flagged for review." Render this path in the rust accent so the eye follows it.
4. "Human reviews the evidence" (this is the single highlighted node, in the rust accent). Attach a small cluster of evidence glyphs beside it: a time-vs-median bar, an answer-sequence strip, a quote mark for open-ends.
5. "Decision recorded" flowing to two outputs: "Exclusion list (reason, flags, reviewer, timestamp)" and "Panel email draft."
6. A persistent horizontal band running beneath the whole flow: "Immutable audit trail: every override, its reason, and the strictness in force." This band should visually underpin every node, signalling that the record sits under the entire process, and it is the package the panel needs to act.

**Emphasis:**
- The human review node (4) is the one highlighted element, in accent colour.
- The audit-trail band (6) is the second accent, quieter than the human node but clearly present under everything.
- The "passed, not shown" path stays deliberately faint. That contrast is the message: the system hides what is fine and surfaces only what needs a person.

**Caption under the diagram:**
"Detection narrows thousands of responses to the few that need a human. The human decides. The record makes every exclusion defensible to the panel."

---

## PART 5: NOTES FOR EZEQUIEL

- New angle folded in: the industry framing (bots and AI-generated participants degrading sample quality) now opens the piece, and the "AI vs AI" point is scoped honestly to the open-ended text analysis so it holds up under interview questioning. The whole engine is not claimed as AI, only the free-text reading, which is the true and strongest version.
- Panel-evidence requirement is now a load-bearing part of both the problem and the design: the panel will not remove a respondent without a documented package, so "evidence, not verdicts" is framed as a commercial necessity, not just good practice. It also sharpens the outcome (exclusions land in the panel's own format).
- Verbs still framed as your 0-to-1 product and design lead. Engineering built the parser and detection. Nothing claims you personally built the LLM or the pipeline.
- Anonymisation held throughout: no platform name, no client or brand names, no panel provider named. When you drop real screenshots in, redact accordingly. The checks table you sent is already client-safe and can be used as-is.
- Title: I led with "When the participants aren't people," which hooks the AI-era threat honestly. If you want to lean harder into the punchline, "Fighting AI with AI" is bolder, but it slightly overclaims scope (only the open-ends use AI), so I would keep that energy in the dek and body rather than the title. Your call.
- Optional strengthener: I can pull one or two current, credible references on the synthetic-respondent / bot-sample problem so the industry framing rests on more than assertion. Say the word and I will add a short, cited line.
- Still trimmed for the recruiter page: the zero-configuration parser, the full check list, the v1-to-v2 API design, and the five deferred capabilities. That is your interview-backup material if you ever want a longer version.
