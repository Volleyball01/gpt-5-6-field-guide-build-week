# Sources and Data Policy

## Primary public source

- OpenAI, [“GPT-5.6: Frontier intelligence that scales with your ambition”](https://openai.com/index/gpt-5-6/), published July 9, 2026.

This official announcement is the primary public source for the model-family descriptions and benchmark evidence represented by the pre-existing datasets. A citation records provenance; it does not imply that OpenAI or any benchmark owner endorses this project.

## Pre-existing benchmark datasets

Both source files use schema version `0.3.0` and preserve a `null` `generatedAt` value:

| File | Benchmark definitions | Data points | Intended evidence shape |
| --- | ---: | ---: | --- |
| `data/source/benchmarks-v3.json` | 19 | 202 | Scores with resource fields where published |
| `data/source/benchmarks-v3-score-only.json` | 19 | 58 | Scores without published cost, latency, or output-token values |

The datasets were assembled before Build Week. Every point currently carries the provenance label `openai-official`, and its `sourceFiles` object preserves the source-artifact labels recorded during the earlier extraction process. Those labels document provenance; they are not guaranteed to be usable repository paths in this baseline.

## Missing-value policy

Missing data remains missing.

- Do not invent, interpolate, or extrapolate unpublished values.
- Do not convert an unavailable value to zero.
- Preserve omitted fields and explicit `missing` entries.
- Preserve the recorded reason, including `not-published`.
- Preserve source disagreements rather than silently averaging or replacing values.
- Keep official values visibly separate from any future project-specific calculation or interpretation.

In the complete dataset, 24 points explicitly omit cost, latency, and output-token objects and record those three fields as `not-published`. In the score-only dataset, all 58 points use the same explicit three-field missing pattern.

## Interpretation boundary

Benchmark results are evidence about particular evaluations, not proof that one model or configuration is universally best. Future task mappings or recommendations must be labeled as project-specific interpretation and must remain traceable to the underlying records.
