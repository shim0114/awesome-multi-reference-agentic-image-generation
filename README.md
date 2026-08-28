# Awesome Multi-Reference & Agentic Image Generation

A curated, source-checked reading list for two rapidly converging directions in
image generation:

- **Multi-reference generation** — composing multiple visual references,
  subjects, identities, concepts, or styles in one generation process.
- **Agentic generation** — using LLM/VLM agents to plan, retrieve, route tools,
  generate, inspect, critique, and iteratively improve images.

The collection also tracks their **direct intersection**: systems in which an
agent actively searches for, selects, organizes, or reasons over visual
references during generation. The list is broad but intentionally
high-precision: uncertain venues, unofficial links, and weakly related papers
are not presented as established results.

> Last updated: **2026-08-29** · Contributions and corrections are welcome.

## Reading lists

| Track | Coverage | List |
|---|---|---|
| Multi-reference image generation | 71 in-scope papers, including 6 dedicated benchmarks, plus 4 foundations | [Browse 75 entries](papers/multi-reference.md) |
| Agentic image generation | 63 direct papers plus 16 adjacent or enabling works | [Browse 79 entries](papers/agentic.md) |
| Multi-reference × agentic generation | 27 strict intersections plus 13 carefully labeled bridges | [Browse 40 entries](papers/intersection.md) |

Counts are per list and are not a unique-paper total. The intersection is
curated independently so that evidence for both axes can be shown explicitly;
not every intersection row is duplicated in both parent lists.

## Scope and taxonomy

| Axis | Included | Kept separate or excluded |
|---|---|---|
| Multi-reference | A method or benchmark explicitly handles multiple visual references, subjects, concepts, identities, or reference roles | Single-reference personalization is listed only when foundational; ordinary multi-image datasets alone are not enough |
| Agentic | An LLM/VLM agent or explicit controller plans, acts, uses tools, retrieves, evaluates, remembers, or revises across steps | A fixed generation pipeline, plain reinforcement learning, or one-shot prompt rewriting alone is not automatically agentic |
| Direct intersection | Agentic behavior is used to obtain, select, structure, reason over, or compose visual references; or a benchmark directly studies agentic systems on multi-reference generation | Retrieval-only and feedback-only systems appear as adjacent bridges unless they demonstrate agentic control |

The detailed lists use the following evidence hierarchy:

1. official proceedings or OpenReview;
2. arXiv abstracts and PDFs;
3. author-maintained project pages and code repositories.

Publication status is written conservatively. In particular, an OpenReview
submission is not labeled as accepted unless an official decision is available.

## A practical reading path

1. Start with the **benchmarks and foundations** in each track.
2. Read the **core methods** newest-first to see the current design space.
3. Use the **intersection list** to study retrieval, reference organization,
   agent planning, and closed-loop visual feedback together.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md), then open a paper-suggestion
issue or a pull request. Every entry should use the exact title, a primary paper
source, an accurate venue/status, and one sentence explaining its relevance.

## License

[MIT](LICENSE)
