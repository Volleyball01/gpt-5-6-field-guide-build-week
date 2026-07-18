# GPT-5.6 Field Guide

An independent, capability-first field guide for choosing GPT-5.6 models and reasoning levels from task needs, resource preferences, and transparent benchmark evidence.

> **Status: Build Week submission candidate.** The product is complete and deployed. The final YouTube video and Codex `/feedback` Session ID are still pending. Every recommendation and capability synthesis is project interpretation, not official OpenAI advice.

## Live demo

- [Open the GPT-5.6 Field Guide](https://gpt-5-6-field-guide-build-week.vercel.app/)
- [Open the six-slide demo deck](https://gpt-5-6-field-guide-build-week.vercel.app/slides.html)
- [View the public repository](https://github.com/Volleyball01/gpt-5-6-field-guide-build-week)

Both pages are framework-free, self-contained, and usable offline after download.

## Project features

- Task-first Quick Decision flow covering everyday work and agent workflows.
- Shared recommendation settings for resource tendency, money versus waiting, and active metric.
- Dynamic model and reasoning recommendations with quantified cheaper and stronger alternatives.
- Artificial Analysis Intelligence Index v4.1 as a clearly sourced general-capability overview.
- Capability-first Benchmark Atlas with individual benchmark evidence beneath project-derived family syntheses.
- Interactive SVG charts for estimated cost, latency, output tokens, and a labeled project-specific composite resource cost.
- Keyboard-selectable points, recommended balance points, Pareto-efficient states, and visibly dominated points.
- Separate score-only evidence, visible missing-data states, configuration detail, provenance, formulas, limitations, and sources.
- Paper and ink-blue study themes, responsive layouts, reduced-motion support, and no external runtime assets.

## Run locally

No installation or build step is required.

1. Clone or download this repository.
2. Open `index.html` directly in a modern browser for the product.
3. Open `slides.html` directly for the presentation deck.

For an HTTP origin that matches deployment behavior, run:

```bash
python -m http.server 8000
```

Then visit:

- `http://localhost:8000/`
- `http://localhost:8000/slides.html`

## Test the experience

For the field guide:

1. Select a task in Quick Decision.
2. Change Conserve Resources, Balanced, or Quality First.
3. Move the money-versus-waiting slider and switch resource metrics.
4. Confirm the recommendation, alternatives, chart star, and explanation update together.
5. Open the Capability Atlas, change capability and benchmark, and select chart points with a pointer or keyboard.
6. Switch themes and repeat at a narrow viewport.

For the slide deck, use `ArrowLeft`, `ArrowRight`, `PageUp`, `PageDown`, `Home`, `End`, or `Space`. Press `T` to switch theme and `F` to request fullscreen.

## Data and evidence

The guide uses three disclosed pre-existing dataset snapshots: 39 benchmark definitions across the source files and 278 evidence points, including 196 points with complete estimated cost, latency, and output-token fields. Missing values remain missing. Raw scores from unlike benchmarks are never averaged.

The source snapshots stay unmodified under `data/source/`. Provenance, normalization, source conflicts, and missing-data policy are documented in [SOURCES.md](SOURCES.md). Build Week boundaries are documented in [BUILD_WEEK.md](BUILD_WEEK.md).

## How Codex and GPT-5.6 accelerated implementation

The product was planned, built, audited, and refined in a primary Codex build thread powered by GPT-5.6. Codex accelerated the work by:

- inspecting three schemas and validating every record count and missing-value pattern;
- translating a capability-first product brief into an original single-file architecture;
- implementing linked recommendation state, Pareto analysis, project-specific utility logic, and interactive SVG charts;
- tracing source conflicts without overwriting or averaging them;
- iterating on editorial hierarchy, responsive behavior, theme behavior, and keyboard access;
- running repeatable static, browser, offline, console, privacy, and deployment checks.

GPT-5.6 and Codex were used meaningfully during creation; the finished static site does not call an AI model or external API at runtime.

## Human product, design, and evidence decisions

The human creator made the central judgments that define the project:

- organize the guide around capabilities and real work, not benchmark brands;
- make task choice local to Quick Decision while keeping resource preferences globally linked;
- separate a broad general-capability overview from specialist evidence;
- treat recommendations and syntheses as project interpretation rather than official advice;
- normalize only within each benchmark and never invent, interpolate, average, or zero-fill missing source data;
- preserve source conflicts and distinguish score-only evidence from resource-complete evidence;
- choose a warm editorial field-guide identity instead of a generic dashboard or application shell;
- keep the delivery framework-free, self-contained, responsive, accessible, and offline-capable.

## Build Week boundary

The three JSON datasets and private design references existed before Build Week. They are disclosed as pre-existing materials and are not claimed as original event work. The information architecture, task mappings, recommendation formula, capability synthesis, interaction model, visual system, implementation, testing, documentation, and presentation deck were created during Build Week with Codex and GPT-5.6.

Private references were used read-only for general design and interaction direction. They are not included in the repository, and their code was not copied wholesale.

## Submission placeholders

- Final public YouTube demo: `<add-public-youtube-url>`
- Primary Codex `/feedback` Session ID: `<add-feedback-session-id>`

Do not fill these placeholders until the final recording is public and `/feedback` has been run in the primary build thread.

## License and notices

Original project code and content are licensed under the MIT License. Pre-existing datasets and third-party names remain subject to the boundaries in [NOTICE.md](NOTICE.md).
