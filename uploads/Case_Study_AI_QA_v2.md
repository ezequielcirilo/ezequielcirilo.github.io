# Case Study: AI-Assisted Quality Assurance (v2)

**For:** Portfolio site, case study page. Upload this file to Claude Design as the build brief.
**Platform:** Rendered copy anonymises the platform as "an internal research operations platform." Do not print the internal product name anywhere on the page.
**Verb note:** Contribution is framed as product judgement (the insight and the rescope decision) plus review workflow design. Engineering implemented the AI changes. No verb claims AI engineering.
**Length:** Rendered narrative is roughly 440 words, sized for a recruiter who will scan, not study.

---

## PART 1: THE COPY THAT RENDERS ON THE PAGE

### Page title
Reading the team to teach the machine

### Subtitle / dek
How the team's own behaviour, not model tuning, turned an expensive, over-scoped AI into a fast, affordable QA copilot that keeps the human in charge of every decision.

### Context
On our internal research operations platform, Quality Assurance is the heaviest workflow. For every study, Quality Analysts confirm whether each audited feature is genuinely present on a brand's website, evidenced by a screenshot, across up to 3,000 individual criteria decisions per study. It is careful work at high volume, and it was the single biggest time cost on the platform.

### The problem
The first version of AI-assisted QA was expensive and slow. Every uploaded image was assessed against every criterion in the study. An assessment with 200 criteria and 200 images generated over 20,000 comparisons, the overwhelming majority of them meaningless, at roughly $30 per assessment. The AI was doing enormous work to answer questions no analyst would ever ask.

### The insight
Rather than reach for model tuning, I looked at how the analysts were already working. Studying the manual tags QAers had created, I saw a clear pattern: they almost always evidenced a criterion using images uploaded within that criterion's own category. The humans had already drawn the natural boundary. I directed the development team to rescope the AI to match it: assess each image only against the criteria in its own category, not the entire study. Iterations collapsed from over 20,000 to a fraction. Cost fell from around $30 per assessment to roughly $2 to $3. Speed improved sharply.

### Keeping the human in charge
The point was never to remove the analyst. It was to remove the labour around their judgement. Analysts no longer hunt through every image for evidence a feature exists. The AI surfaces and tags the candidate evidence; the analyst does the part only a human should, confirming or overriding. Every override carries a reason, and that reason feeds back into the model, so human decisions continually sharpen the system while staying firmly in control.

### Knowing when to stop
The agent is bounded not only in what it checks but in when it defers. If it cannot confirm a feature with confidence after its retries, it does not fabricate an answer. It fails gracefully and escalates that item to a human. The system is designed around its own limits.

### Outcome
87% of AI suggestions are now approved without correction. A QA pass that once took six to eight hours now takes two and a half to three, a 69% reduction, at a fraction of the original cost.

### Takeaway
The biggest gains came not from a better model, but from a sharper question: what is the AI actually for, and where does the human belong? That is the pattern I design for in every AI product I build.

---

## PART 2: BUILD DIRECTIONS FOR CLAUDE DESIGN

You have access to the internal platform web app. Use it to capture real interface imagery so a recruiter can see this is a shipped product, not a mockup. Read Part 3 before capturing anything: there are strict format and confidentiality rules.

Layout intent: keep the reading column narrow and the copy primary. Visuals support the narrative, they do not lead it. Match the existing case study visual system already on the site: thin strokes, generous whitespace, a single rust accent, one highlighted element per visual.

### Where each visual sits

**[VISUAL 1: HERO, top of page, above the title]**
A single real screenshot of the QA review workspace: an analyst view showing an uploaded screenshot with an AI-suggested bounding box on it and the confirm / override controls visible. This is the money shot. It must read instantly as "a person reviewing an AI suggestion." Capture per Part 3 rules. If a clean real capture is not achievable, fall back to the existing abstracted AI-QA illustration already used on the case study card, do not invent a new style.

**[VISUAL 2: DIAGRAM, placed between "The insight" and "Keeping the human in charge"]**
Build the human-in-the-loop loop diagram specced in Part 4. This is the conceptual centre of the piece.

**[VISUAL 3: SCREENSHOT, beside or below "The insight"]**
A capture that shows the category structure of the image review, the thing that made the scope insight possible: images grouped by feature category, with criteria belonging to that same category. The goal is to let a reader see why "assess each image only against its own category" is a natural boundary, not an arbitrary one. A cropped, focused grab of the category-organised view is better than a full-page screenshot shrunk down.

**[VISUAL 4: FEATURE CLOSE-UP, beside "Keeping the human in charge"]**
A tight capture of the override interaction: the moment an analyst rejects a suggestion and records a reason. If this exact state is hard to capture cleanly, a close crop of the confirm / override controls is an acceptable substitute. This visual carries the feedback-loop point, so the "reason" input is the element worth foregrounding.

**[STAT ROW: directly under "Outcome"]**
Pull the numbers into a scannable row, not buried in prose. Four items:
- 87% approved without correction
- 69% faster QA (6 to 8 hrs, down to 2.5 to 3 hrs)
- ~$30 to ~$2 to $3 per assessment
- 20,000+ checks, cut to a category-scoped fraction
Use the single rust accent for the numbers. Keep units small and secondary so the figures dominate.

---

## PART 3: SCREENSHOT FORMAT AND CONFIDENTIALITY RULES (read before capturing)

**Format and responsiveness**
- Capture all screenshots at one consistent desktop viewport width (target 1440px wide) so every image shares the same scale and aspect ratio. Mismatched widths will look amateurish when stacked.
- Do not capture at a narrow or mobile breakpoint where the layout collapses to a single column, unless a mobile view is specifically the point. The main shots should show the settled desktop layout.
- Wait for the page to fully settle before capturing: data loaded, no loading spinners, no half-open menus or modals, unless a specific interaction state is being shown deliberately.
- For feature close-ups (Visuals 3 and 4), capture the specific component cleanly cropped at native resolution. Do not screenshot the whole page and shrink it; that produces unreadable detail.
- Export at 2x / retina density if available, so the images stay crisp on high-resolution laptops, which is what most recruiters use.
- Keep a consistent crop ratio across the set. Pick one landscape ratio for full-view shots and one tighter ratio for close-ups, and hold to them.

**Confidentiality, non-negotiable**
- The public site anonymises the platform and does not name clients. Before any screenshot is used, blur or redact: real client and brand names, any participant PII (names, emails, account numbers), and the internal product name / logo if it appears in the chrome.
- If a screen cannot be captured without exposing client-identifying data even after redaction, do not use it. Fall back to the abstracted illustration instead.
- When in doubt, redact more. A slightly emptier screenshot is fine; an exposed client name is not.

---

## PART 4: DIAGRAM SPEC (Visual 2, the human-in-the-loop loop)

Build a clean horizontal flow that makes the loop explicit and puts the human at the centre. Match the site's visual language: thin strokes, single rust accent, generous spacing, rounded nodes, no heavy fills. It must stay legible when it stacks to one column at 375px.

**Nodes and flow, left to right:**
1. "Auditor uploads evidence" (screenshot images, grouped by category)
2. "AI assesses, scoped to category" (the rescope: each image checked only against criteria in its own category)
3. "AI suggests and tags candidate evidence"
4. A decision point: "Confident?"
   - If yes, flow to node 5.
   - If no, after retries, branch to a distinct node: "Escalate to human" (this is the safeguard; style it as a deliberate hand-off, not an error).
5. "Analyst confirms or overrides" (highlight this node in the rust accent; it is the human decision, the heart of the diagram)
6. From "override," a labelled return arrow "reason captured" loops back to node 2 / the model, showing the feedback loop that sharpens future suggestions.

**Emphasis:**
- The human decision node (5) is the one highlighted element, in accent colour.
- The feedback loop arrow (6) should be visually clear as a loop, ideally the second accented element, so the "human decisions train the system" idea is unmissable.
- Everything else stays neutral and quiet so those two elements carry the meaning.

**Caption under the diagram:**
"The AI carries the load. The human keeps the decision. Every override teaches the model, and the agent hands back the moment it is unsure."

---

## PART 5: NOTES FOR EZEQUIEL

- The 69% cycle-time figure is used here to stay consistent with your CV and LinkedIn. The cost story is told in dollars, not percentages, on purpose, so nothing collides with that 69% and no one is left doing arithmetic on your numbers.
- The 50% baseline is gone entirely, per your call. The "before" is anchored on cost and iteration volume, the figures you can defend directly, plus a qualitative "expensive and slow."
- If the real interface captures come back weak or hard to anonymise, we lose nothing by leaning on the abstracted illustrations; the copy carries the piece either way.
- Once this page is approved, the case study card's "Read case study" link points here (/case-studies/ai-qa), and this becomes the one live case study while Audit Agents and Research Data Integrity stay "coming soon."
