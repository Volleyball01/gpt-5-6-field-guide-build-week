# Sources and Data Policy

## Primary public source

- OpenAI, [“GPT-5.6: Frontier intelligence that scales with your ambition”](https://openai.com/index/gpt-5-6/), published July 9, 2026.

This official announcement is the primary public source for the model-family descriptions and benchmark evidence represented by the pre-existing datasets. A citation records provenance; it does not imply that OpenAI or any benchmark owner endorses this project.

## Pre-existing benchmark datasets

All three source files preserve a `null` `generatedAt` value. The files remain separate because the Artificial Analysis snapshot uses an earlier schema and a distinct evidence role:

| File | Benchmark definitions | Data points | Intended evidence shape |
| --- | ---: | ---: | --- |
| `data/source/benchmarks-v3.json` | 19 | 202 | Scores with resource fields where published |
| `data/source/benchmarks-v3-score-only.json` | 19 | 58 | Scores without published cost, latency, or output-token values |
| `data/source/benchmarks-aa.json` | 1 | 18 | Artificial Analysis Intelligence Index v4.1 scores with cost, latency, and output-token fields |

The `benchmarks-v3` files use schema `0.3.0`; `benchmarks-aa.json` uses schema `0.2.0`. The datasets were assembled before Build Week. Every point currently carries the provenance label `openai-official`, and its `sourceFiles` object preserves the source-artifact labels recorded during the earlier extraction process. Those labels document the dataset's recorded provenance; they are not guaranteed to be usable repository paths and do not imply endorsement or independent verification.

## Artificial Analysis Intelligence Index v4.1

- Artificial Analysis, [Intelligence Benchmarking Methodology](https://artificialanalysis.ai/methodology/intelligence-benchmarking), defines the versioned Intelligence Index and its component evaluations.
- Artificial Analysis, [“Artificial Analysis Intelligence Index v4.1: a shift toward agentic workloads”](https://artificialanalysis.ai/articles/artificial-analysis-intelligence-index-v4-1/), documents the v4.1 update.
- The OpenAI GPT-5.6 release page publishes GPT-5.6 results and describes the index as a broad measure spanning agentic work, coding, scientific reasoning, and general capabilities.

Artificial Analysis defines and maintains the benchmark. This repository's `benchmarks-aa.json` is a pre-Build-Week snapshot, not a live feed and not an official Artificial Analysis dataset release. The field guide presents it as a broad general-capability overview and clearly separates the benchmark's published index score from project-specific recommendation and synthesis layers.

## Missing-value policy

Missing data remains missing.

- Do not invent, interpolate, or extrapolate unpublished values.
- Do not convert an unavailable value to zero.
- Preserve omitted fields and explicit `missing` entries.
- Preserve the recorded reason, including `not-published`.
- Preserve source disagreements rather than silently averaging or replacing values.
- Keep official values visibly separate from any future project-specific calculation or interpretation.

In `benchmarks-v3.json`, 24 points explicitly omit cost, latency, and output-token objects and record those three fields as `not-published`. In `benchmarks-v3-score-only.json`, all 58 points use the same explicit three-field missing pattern. All 18 points in `benchmarks-aa.json` include score, estimated cost, latency, and output-token objects; this completeness does not make the snapshot live or independently verified.

## Interpretation boundary

Benchmark results are evidence about particular evaluations, not proof that one model or configuration is universally best. Future task mappings or recommendations must be labeled as project-specific interpretation and must remain traceable to the underlying records.
