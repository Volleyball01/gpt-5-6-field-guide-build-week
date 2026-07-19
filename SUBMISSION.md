# GPT-5.6 Field Guide — Submission Kit

## Recommended track

**Work and Productivity**

The field guide helps knowledge workers, developers, researchers, and operators choose a GPT-5.6 configuration for real work while making cost, waiting time, evidence quality, and uncertainty inspectable. Its primary outcome is better work decisions, so Work and Productivity is a closer fit than a benchmark viewer categorized only as a developer tool.

## One-sentence tagline

Choose GPT-5.6 by the work you need to finish—not by the loudest benchmark number.

## Required links and placeholders

- Live project: https://gpt-5-6-field-guide-build-week.vercel.app/
- Source repository: https://github.com/Volleyball01/gpt-5-6-field-guide-build-week
- Public YouTube demo: https://www.youtube.com/watch?v=-OdQyk8LBSU
- Primary Codex `/feedback` Session ID: `019f740c-94a0-7f11-ae0f-f0b20c1223e9`

## Devpost Project Story

### Inspiration

GPT-5.6 arrives with a rich set of model tiers, reasoning levels, execution modes, benchmark scores, estimated costs, latency measurements, and token counts. That evidence is valuable, but it is published in the language of evaluations. People make decisions in the language of work: “I need to debug this repository,” “I need to find an obscure fact,” or “I need to complete an important professional task.”

The project began with a simple product question: what if benchmark evidence behaved like a field guide instead of a leaderboard?

### What it does

GPT-5.6 Field Guide turns published benchmark evidence into a task-first decision experience. A user chooses the kind of work, selects a recommendation tendency, and expresses whether money or waiting matters more. The guide then proposes one model and reasoning configuration, explains why, and shows quantified cheaper and stronger alternatives.

Below that fast path, the Capability Atlas reorganizes evidence around meanings such as building and operating software, finding hard-to-reach facts, completing professional work, and automating with tools. Each benchmark introduction states the capability it represents, the real tasks it resembles, what it does not measure, how to read its score, and which benchmark supplies the evidence.

Interactive SVG charts expose estimated cost, latency, output tokens, and a clearly labeled project-specific composite resource cost. Recommended points, Pareto-efficient points, dominated points, provenance, missing fields, source conflicts, formulas, and limitations remain visible. Artificial Analysis Intelligence Index v4.1 provides a separate general-capability overview, while score-only records remain in their own evidence section so unavailable resource values are never guessed.

Every recommendation and synthesis is labeled as project interpretation, not official OpenAI advice.

### How we built it

The product was created in a primary Codex build thread powered by GPT-5.6. Codex first audited three pre-existing JSON snapshots, their schema versions, record counts, missing-value patterns, provenance fields, and source conflicts. The human creator then set the core product thesis: capabilities before benchmark brands, task choice only where it is meaningful, transparent uncertainty, and an editorial field-guide identity rather than a dashboard shell.

Codex and GPT-5.6 translated that direction into an original, framework-free implementation: one self-contained `index.html` with inline CSS, JavaScript, SVG, and embedded derivative data. The build added shared preference state, recommendation utilities, within-benchmark normalization, capability synthesis, Pareto analysis, keyboard-selectable chart points, responsive layouts, two themes, and offline behavior. Playwright-driven browser checks exercised desktop, mobile, keyboard, controls, themes, every rendered benchmark, console output, and local network activity.

The final site does not call an AI model or external API at runtime. GPT-5.6 and Codex were the build-time reasoning and implementation environment.

### Challenges we ran into

The hardest problem was epistemic, not visual: dense benchmark evidence can look more certain than it is. Some records have complete resource curves; others publish only scores. Some table values conflict with chart-derived values. Multi-agent and single-agent configurations are not interchangeable. Raw scores from unlike benchmarks cannot be averaged honestly.

The solution was to make those boundaries part of the interface. Missing stays missing. Score-only evidence cannot drive cost or speed claims. Conflicts are preserved and described. Synthesis normalizes only within each benchmark, reports coverage, and labels confidence as an evidence-breadth signal rather than a statistical interval.

A second challenge was connecting a fast recommendation experience with a deep evidence atlas without creating a generic four-workspace application. The final page uses one global resource-preference state, but task choice remains local to Quick Decision. Detailed charts can show suggested evidence or independent exploration without pretending every everyday task has a specialist benchmark.

### Accomplishments that we are proud of

- A substantial editorial product delivered as one portable HTML file with no framework or runtime dependency.
- 39 benchmark definitions across the source files and 278 source points represented across general, resource-complete, and score-only evidence roles.
- 196 points with complete cost, latency, and output-token data used without inventing values for the remaining records.
- Capability-first explanations that foreground real task meaning and measurement limits.
- Linked recommendations, alternatives, metrics, chart states, and plain-language explanations.
- Strong responsive, keyboard, theme, reduced-motion, offline, privacy, and console validation.
- A clear public record separating pre-existing data from original Build Week work.

### What we learned

The most useful benchmark interface is not the one with the most numbers. It is the one that helps a person understand what a number can support, what it cannot support, and what to test next.

We also learned that a single-file constraint can improve product discipline. Without a framework or component library, every interaction and visual motif had to justify itself. Codex made that constraint practical by accelerating schema inspection, implementation, regression testing, and iterative design while the human creator retained responsibility for product judgment and evidence policy.

### What is next

The public narrated demo and primary Codex `/feedback` evidence are complete. The immediate next step is the Devpost submission, which has not yet been claimed as submitted. After Build Week, the project could add user-supplied evaluation results, exportable comparison notes, and versioned benchmark snapshots. Any expansion should preserve the current rules: no hidden averaging, no guessed resources, no universal winner, and a visible boundary between source evidence and project interpretation.

## Built with tags

- Codex
- GPT-5.6
- HTML5
- CSS3
- JavaScript
- SVG
- JSON
- Playwright
- Vercel
- Accessibility
- Data visualization
- Offline-first

## Image-gallery shot list

1. **Editorial opening, paper theme** — Capture the hero, opening thesis, and “Choose the work. Then choose the model.” headline at 1440 × 900.
2. **Quick Decision in action** — Show a selected agent workflow, Balanced tendency, money-versus-waiting slider, and the recommendation with cheaper and stronger alternatives.
3. **General capability overview** — Capture Artificial Analysis Intelligence Index v4.1 with the shared settings, recommendation star, legend, and provenance note visible.
4. **Capability Atlas, study theme** — Show “Build and operate software,” its capability explanation, supporting benchmark, interactive SVG chart, and selected configuration panel.
5. **Evidence transparency** — Capture the score-only section or source-conflict state with missing cost, latency, and output-token ribbons visible.
6. **Method and formulas** — Show the project-interpretation label, normalization rule, composite formula, Pareto definition, limitations, and source notes.

Do not include browser chrome containing private bookmarks, local paths, account names, or unrelated tabs.

## 2:40 English narration script

### 0:00–0:20 — The problem

“GPT-5.6 gives us multiple models, reasoning levels, and benchmark signals. But benchmarks answer questions like score, cost, and latency, while people ask a different question: what should I use for the work in front of me? I built GPT-5.6 Field Guide to translate between those two languages.”

### 0:20–0:42 — The solution

“This is an independent, capability-first field guide, not official OpenAI advice. It is one self-contained HTML file with no framework and no runtime assets. It organizes 278 preserved evidence points around real capabilities, while keeping missing data, provenance, and measurement limits visible.”

### 0:42–1:12 — Quick Decision

“I start with the task, for example building and operating software. Then I choose whether to conserve resources, balance the trade-off, or prioritize quality. This slider expresses whether money or waiting matters more, and I can switch between estimated cost, latency, output tokens, and a project-specific composite. The recommendation updates immediately, with one cheaper alternative and one stronger alternative. These are quantified project interpretations, not universal winners.”

### 1:12–1:42 — General overview and Atlas

“Artificial Analysis Intelligence Index v4.1 provides a broad general-capability overview. For specialist evidence, the Capability Atlas leads with meaning: what the capability represents, which real tasks it resembles, what it does not measure, how to interpret the score, and which benchmark supplies the evidence. I can select every chart point by mouse or keyboard, inspect the exact configuration, and distinguish the recommended point, Pareto-efficient options, and dominated points.”

### 1:42–2:05 — Evidence integrity

“The guide never invents unavailable values. Resource-complete evidence and score-only evidence remain separate. Source conflicts are preserved instead of silently averaged. Capability syntheses normalize only inside each benchmark, then report benchmark coverage and evidence confidence. Raw scores from unlike evaluations are never averaged.”

### 2:05–2:28 — Codex and GPT-5.6

“I built the project in one primary Codex thread powered by GPT-5.6. Codex accelerated schema auditing, interaction architecture, original HTML, CSS, JavaScript and SVG implementation, Pareto and recommendation logic, accessibility work, and browser regression testing. I made the key human decisions: capabilities before benchmark brands, strict evidence boundaries, local task meaning, and the editorial paper-and-ink design direction.”

### 2:28–2:40 — Close

“The result is a fast three-minute decision path with a deep audit trail underneath. Choose the work, tune the compromise, inspect the evidence, and decide what to test next. This is GPT-5.6 Field Guide.”

## Matching recording shot list

| Time | Screen action | Narration focus |
| --- | --- | --- |
| 0:00–0:20 | Start on slide 1, then open the product hero. Slow scroll to the opening thesis. | Benchmark language versus task language. |
| 0:20–0:42 | Show slide 2, then the top-level section rhythm in the product. | Independent, self-contained, capability-first solution and evidence scope. |
| 0:42–1:12 | Select “Build and operate software.” Toggle all three tendencies, move the slider, switch cost to latency, and pause on alternatives. | Quick Decision and project-interpretation boundary. |
| 1:12–1:42 | Scroll through the general overview into the Capability Atlas. Change one benchmark and select a chart point with the keyboard. | Broad overview, capability meaning, chart states, and configuration detail. |
| 1:42–2:05 | Show a visible provenance block, a source-conflict note, the score-only evidence ribbon, and the synthesis coverage labels. | Missing-data, conflict, and normalization policy. |
| 2:05–2:28 | Show slide 5, a brief clean repository tree, then return to the product’s theme toggle and keyboard focus state. | Specific Codex and GPT-5.6 contributions versus human decisions. |
| 2:28–2:40 | Show slide 6, click “Open the live field guide,” and end on the hero in the study theme. | Closing message and call to test. |

Recording notes:

- Record at 1920 × 1080 or 1440 × 810 with browser zoom at 100%.
- Keep the pointer still while speaking; move only when demonstrating an interaction.
- Use the prepared six-slide deck as chapter cards, not as a substitute for the working-product demo.
- The final narrated export is public and remains under the three-minute limit.
- The primary Codex `/feedback` Session ID is recorded in the required links section above.
