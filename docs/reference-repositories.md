# Reference Repositories and Curation Patterns

> Reviewed on 2026-08-29 using each project's own GitHub repository, README,
> contribution guide, structured data, and workflows. The links below document
> design and maintenance patterns; inclusion here is not an endorsement of each
> repository's paper-selection decisions.

## Repositories reviewed

| Repository | Pattern worth reusing | Pattern to avoid |
|---|---|---|
| [Awesome Text-to-Image Studies](https://github.com/AlonzoLeeeooo/awesome-text-to-image-studies) | The README is the homepage; papers are organized by research direction, year, and venue, with topic pages and a bibliography | Deep nesting and maintainer-specific news make the main page difficult to scan |
| [Awesome Personalized Image Generation](https://github.com/csyxwei/Awesome-Personalized-Image-Generation) | A task taxonomy, compact paper blocks, and separate benchmark/survey sections make a large field navigable | Full author lists on every record make the page extremely long |
| [Awesome Multimodal Large Language Models](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models) | Fixed metadata columns, newest-first ordering, highlighted entry points, and a complete contents section | Per-paper star badges and extensive promotional content create visual noise |
| [Awesome Diffusion Language Models](https://github.com/VILA-Lab/Awesome-DLMs) | A small badge set, research timeline, Must-Read section, and taxonomy-first organization give newcomers a clear route | Repeated resource badges make dense sections harder to read |
| [Awesome Multimodal Reasoning](https://github.com/The-Martyr/Awesome-Multimodal-Reasoning) | A short table of contents and date-first entries work well for a fast-moving field | Date and title alone do not establish scope or relevance |
| [Awesome LLM Agent Papers](https://github.com/js-lee-AI/awesome-llm-agent-papers) | Starter Kit, taxonomy, collapsible lists, one-line annotations, related lists, and CI-backed metadata checks form a strong end-to-end design | Hand-maintained counts and popularity-based sections need careful automation and interpretation |
| [Awesome Data Agent Papers](https://github.com/SJTU-DMTai/Awesome-Data-Agent-Papers) | Structured YAML, generated Markdown, contribution forms, maintenance documentation, and review-first discovery automation reduce drift | Automated classification and venue filling cannot replace human verification |
| [Awesome Code Agents](https://github.com/EuniAI/awesome-code-agents) | Recent papers stay on the homepage, the historical archive is generated, and automated discovery creates review issues rather than publishing directly | A large hero area and many badges can overwhelm the collection itself |
| [Awesome MLLM Benchmarks](https://github.com/lchen1019/awesome-mllm-benchmarks) | Structured JSON powers both compact README tables and a searchable site | A separate interactive site is unnecessary before benchmark metadata becomes large enough to justify it |
| [AI Papers of the Week](https://github.com/dair-ai/AI-Papers-of-the-Week) | A concise index points to durable yearly archives, and selected entries explain why they matter | Chronological curation cannot replace a research taxonomy |

## Patterns adopted here

1. **A useful first screen.** The README immediately explains the scope and
   exposes a Starter Kit, latest additions, and direct paper links.
2. **Taxonomy before chronology.** Research categories are primary; entries are
   newest-first within each category.
3. **The direct intersection is prominent.** It is the collection's most
   distinctive contribution and has a compact homepage list plus a detailed
   two-axis evidence matrix.
4. **Compact metadata.** Paper title, venue/status, project, code, and data are
   shown consistently. Missing artifacts are omitted from compact entries.
5. **Primary-source-first status.** Proceedings, OpenReview decisions, and
   arXiv are preferred over aggregators or repository claims.
6. **Few visual elements.** A small badge group and one Mermaid research map
   provide orientation without per-paper badge noise.
7. **Structured contribution paths.** Separate issue forms cover additions and
   corrections, while a maintainer guide records scope and verification rules.
8. **Mechanical CI, human judgment.** CI checks Markdown and duplicate arXiv
   identifiers. Paper relevance, intersection status, and venue claims remain
   manually reviewed.

## Next maintenance step

If the collection grows substantially, migrate paper metadata to a single
structured source such as `data/papers.yaml`, then generate the README and
topic pages. Generated counts, sorting, and cross-list references would prevent
drift, while candidate-discovery automation should continue to create review
issues rather than publishing directly.
