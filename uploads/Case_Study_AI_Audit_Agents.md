# Case Study: AI Audit Agents (v1) — FLAGSHIP

**For:** Portfolio site, case study page. Upload this file to Claude Design as the build brief.
**Card this belongs to:** "AI Audit Agents" (the flagship card; currently "Coming soon").
**Platform:** Rendered copy anonymises the platform as "an internal research operations platform." Do not print the internal product or module name. Do not name any client or brand.
**Model vendors:** Naming Anthropic and OpenAI is intentional and consistent with the site's existing tech-stack line. Keep it.
**Verb note:** Framed as "led the integration of." Contribution is product leadership and product judgement. The consensus mechanism was the engineering team's design and is credited to them. The decision to leave no-consensus criteria unanswered, the screenshot budget, and the capture-from-URL flow are Ezequiel's calls. The starting-URL input was a discovery finding from the ops team. No verb claims that model or agent engineering was done personally.
**Boundary (do not blur):** Audit answers the criteria and captures evidence images. There is NO tagging and NO bounding boxes at this stage. Tagging and bounding boxes belong to the QA case study and must not appear here.
**Length:** Rendered narrative is roughly 460 words, sized for a recruiter who will scan, not study.
**Imagery:** No live interface capture this round. Interface visuals are described placeholders; the one real asset Ezequiel already holds (the AI Co-pilot capture panel) may be dropped in once redacted. See Part 2 and Part 3.

---

## PART 1: THE COPY THAT RENDERS ON THE PAGE

### Page title
Knowing what not to answer

### Subtitle / dek
An autonomous agent that audits a brand's website against a criteria library, using two frontier models that must agree, at confidence, before an answer counts. Where they can't, the work passes to a human. Near-human accuracy in production, at a fraction of the cost.

### Context
Auditing is where the platform's data begins. For every brand, an auditor works through a library of 150 to 200 criteria per channel, deciding whether each feature is present on the site and capturing the screenshot evidence that later proves it. It is the heaviest input task on the platform, hours of skilled work per assessment, and more when the experience sits behind a login. Automating it was the biggest prize available, and the easiest to get wrong.

### The build
The agent takes a single input: the starting URL. That choice matters, because multi-line brands run separate landing pages per product, and the entry point decides whether the agent assesses the right one. From there it is autonomous: it crawls the site, maps it, decides which pages are worth capturing, and answers the criteria from what it finds. Two frontier models sit behind those answers, one from Anthropic and one from OpenAI. One navigates, captures, and answers; the other answers from the screenshots alone.

### The decision that mattered
When the two models disagreed, the engineering team's first instinct was to publish the answer from whichever model was more confident. We tried it. Accuracy fell, and the team stopped trusting the output. I argued for the opposite: when the models do not reach confident agreement, answer nothing and leave the criterion for the human co-auditor. Consensus had to mean genuine agreement at genuine confidence, not the louder model winning. We traded reach for trust, and the trust is what made the tool usable.

There was a second reason the split worked. One model sees the live site; the other sees only the screenshots, the same evidence a human reviews later at QA. When that model cannot confirm a feature from the images, the evidence itself is thin, and that is precisely when a person should look.

### Two product levers
The first agent run captured over a thousand screenshots: tooltips, dropdowns, chat widgets, everything. I introduced a screenshot budget, a cap that forces the agent to prioritise the captures it is most confident carry a feature, trading coverage against storage cost. I also designed a capture-from-URL flow: rather than manually screenshotting and uploading evidence, the auditor pastes a URL and the system captures it, and records where that feature lives so the next run finds it faster. The human makes the agent better every time they use it.

### Outcome
In production, the agent's answers were confirmed correct at QA 93% of the time, against a human auditor baseline of 96%: near-human accuracy, at a 63% reduction in audit cost and time. The company kept the savings.

### Takeaway
The flagship result did not come from a smarter model. It came from deciding what the system should refuse to answer, and building the human in to catch exactly those cases. Reach is easy. Trust is the product.

---

## PART 2: BUILD DIRECTIONS FOR CLAUDE DESIGN

No live interface capture in this pass. Do not attempt to visit any URL. Interface visuals below are placeholders: render each as a clean framed box in the site's visual system (thin strokes, generous whitespace, single rust accent), with the supplied description as its caption. Ezequiel will drop in a redacted real screenshot or an abstracted illustration later.

Layout intent: reading column narrow, copy primary, visuals in support. One highlighted element per visual, rust accent used sparingly. This is the flagship page, so it can carry slightly more visual weight than the other two, but not at the cost of the copy.

### Where each visual sits

**[PLACEHOLDER 1: HERO, above the title]**
Depicts: the AI Co-pilot capture panel. It maps a brand's site from a starting URL, screenshots the pages it finds, and files them into category folders across the audit. The panel shows the starting-URL field and a screenshot budget selector (for example 50 / 80 / 100 pages). Ezequiel holds a real screenshot of this and can drop it in once redacted. The point this image makes: the whole agent is driven by one input and a deliberate capture budget.
Caption: "One input, the starting URL, and a capture budget that forces the agent to prioritise. The rest it does itself."

**[PLACEHOLDER 2: DIAGRAM, between "The build" and "The decision that mattered"]**
Build the two-model consensus flow specced in Part 4. This is the conceptual centre of the flagship and should be a built diagram, not a placeholder box.

**[PLACEHOLDER 3: capture-from-URL, beside "Two product levers"]**
Depicts: the evidence capture-from-URL control. Instead of manually screenshotting and uploading, the auditor pastes a page URL and the system takes a full-page screenshot and files it against the criterion. This is a crop of the same real UI Ezequiel holds, so it can be a real asset once redacted.
Caption: "Paste a URL, and the system captures the evidence and remembers where the feature lives for next time."

**[STAT ROW: directly under "Outcome"]**
Pull the numbers into a scannable row, rust accent on the figures. Four items:
- 93% of agent answers confirmed correct at QA
- 96% human auditor baseline (the agent runs at near-human accuracy)
- 63% reduction in audit cost and time
- 1 input to the agent: the starting URL
Keep units small and secondary so the figures dominate. The 93% and 96% should sit next to each other so the near-human comparison reads instantly.

---

## PART 3: PLACEHOLDER AND CONFIDENTIALITY RULES

**Placeholders (this round)**
- Render each interface placeholder as a framed box in the site's style, with the description as caption, sized to the aspect ratio the final image will use, so the layout can be approved before the real image exists.
- Placeholders 1 and 3 are crops of one real screenshot Ezequiel already holds; he may drop those in as real assets.
- Keep placeholders on one consistent landscape ratio for full-view images and one tighter ratio for the stat strip.

**When real screenshots replace the placeholders (by Ezequiel)**
- The public site anonymises the platform and names no clients. Before any screenshot is used, redact: client and brand names, any URLs that reveal a brand, and the internal product or module name in the chrome. The co-pilot screenshot in particular carries a brand URL and a client folder name that must be removed.
- Model vendor names (Anthropic, OpenAI) may stay, they are already on the site.
- When in doubt, redact more. An emptier screenshot is fine; an exposed client is not.

---

## PART 4: DIAGRAM SPEC (Placeholder 2, the two-model consensus flow)

Build a clean flow that shows two models cross-checking, agreement flowing through, and disagreement handed to a person. Match the site's visual language: thin strokes, single rust accent, rounded nodes, no heavy fills. Legible when it stacks to one column at 375px.

**Nodes and flow:**
1. "Auditor assigns the agent" with two small input labels: "Starting URL" and "Named human co-auditor."
2. "Agent crawls, maps, and captures" with a small sub-label: "within a screenshot budget, prioritising confident captures."
3. A parallel pair of model nodes, side by side:
   - "Model A (Anthropic): navigates, captures, answers, sees the live site."
   - "Model B (OpenAI): answers from the screenshots only, sees what QA will see."
   (Vendor-to-role mapping is illustrative; if unsure, label them Model A and Model B and keep the "live site" vs "screenshots only" distinction, which is the important part.)
4. A decision point: "Agree, at confidence?"
   - Yes: flows to "Answer enters the audit." Render this path quiet.
   - No, or agreement only at low confidence: flows to "Left unanswered for the human." Render this path in the rust accent.
5. "Human co-auditor answers the uncertain criteria and adds evidence." This is the single highlighted node, in the rust accent, the heart of the diagram.
6. "On to QA" with a small note that the evidence images carry forward.

**Emphasis:**
- The human node (5) is the one highlighted element.
- The "left unanswered for the human" path (4 to 5) is the second accent. The "answer enters the audit" path stays quiet. The contrast is the message: the system's discipline is in what it declines to answer.
- The "live site vs screenshots only" contrast on the two model nodes should be visually clear, since that is the clever cross-check.

**Caption under the diagram:**
"Two models must agree, at confidence, before an answer counts. One sees the live site, one sees only the evidence QA will get. Everything uncertain goes to a person."

---

## PART 5: NOTES FOR EZEQUIEL

- This is the flagship, and it is the strongest of the three because the pivotal decision is counterintuitive and backed by a real failure: the team first pushed the higher-confidence model's answer, accuracy dropped, trust eroded, and you argued the platform back to leaving uncertain criteria blank. That arc is the whole case study. I led the page with it.
- Contribution is split exactly as we agreed: the consensus mechanism is credited to the engineering team; the "answer nothing without confident agreement" decision, the screenshot budget, and capture-from-URL are yours; the starting-URL input is framed as a discovery finding from the ops team. Nothing claims you engineered the models.
- The 6-to-8-hours figure does not appear here. I described the manual audit as "hours of skilled work per assessment, more behind a login," which is true under any reading and keeps this page from echoing the QA piece.
- IMPORTANT, and it concerns the QA case study, not this one: you described 6 to 8 hours as the budget "across the two tasks (Audit and QA)." The QA case study currently states that a QA pass alone took 6 to 8 hours. If 6 to 8 was the combined budget for audit plus QA together, the QA piece overstates it and we should correct it to keep the two consistent. If audit and QA were each separately 6 to 8 hours, both are fine as written. Tell me which, and I will reconcile them.
- Title: I led with "Knowing what not to answer," which captures the counterintuitive judgement. If you want something plainer for a fast skim, "Trust over reach" or "Two models, one human" both work. Easy swap.
- When this page is built, the flagship card's "Coming soon" can flip to a live link (/case-studies/ai-audit-agents), and you will have all three case studies live.
- As with the others, there is strong material I left out for length: the full crawl-and-map behaviour, the screenshot-budget tuning, and how capture-from-URL compounds the agent's reach over successive runs. That is your interview-backup depth if you ever want a longer version.
