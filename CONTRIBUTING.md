# Contributing

Thanks for helping keep the collection accurate and current. You can suggest a
paper with the [issue form](https://github.com/zsyverse/awesome-multi-reference-agentic-image-generation/issues/new?template=paper.yml)
or open a pull request.

## Before submitting

Search all three paper indexes by title, arXiv identifier, DOI, and known alias.
A paper can belong to more than one track, but renamed or extended versions of
the same work should remain one record.

The paper must fit at least one track:

1. **Multi-reference image generation** — generation conditioned on multiple
   visual references, subjects, concepts, identities, styles, or reference
   roles.
2. **Agentic image generation** — an LLM/VLM agent or explicit controller
   plans, invokes tools, retrieves, critiques, remembers, collaborates, or
   iteratively refines image generation or generative editing.
3. **Direct intersection** — both properties are explicit. State separate
   evidence for the multi-reference axis and the agentic axis.

## Required metadata

- Exact paper title from the primary source.
- Primary paper URL: official proceedings, OpenReview, or arXiv abstract.
- Publication month and accurate venue/status.
- Official project, code, model, data, or demo links when available.
- One concise sentence explaining the paper's contribution and relevance.

Use `arXiv preprint` or `under review` when appropriate. Do not infer acceptance
from a repository name, personal page, search snippet, or anonymous submission.
Only link artifacts maintained by the authors or their organization.

## Entry format

Regular paper entries use a compact, mobile-friendly format:

```markdown
- [**Exact Paper Title**](primary-paper-url) — *Venue / status, Year*.
  One sentence explaining the contribution. [Project](url) · [Code](url)
```

Benchmark comparison tables and the intersection evidence matrix may retain
extra columns when those fields are necessary.

## Placement and ordering

- Choose the narrowest correct research category.
- Keep entries newest-first within each category.
- Separate foundations, benchmarks, and adjacent work from core methods.
- Do not list a benchmark as a generation method.
- Do not list a single-reference method as multi-reference without a clearly
  labeled foundational role.
- Omit missing artifacts rather than adding empty badges to compact lists.

## Pull-request checklist

- [ ] I searched for duplicate identifiers, aliases, and titles.
- [ ] The title and venue/status match a primary source.
- [ ] Project and code links are official and their release status is accurate.
- [ ] The entry contains a concise relevance sentence.
- [ ] The category and newest-first ordering are correct.
- [ ] `git diff --check` and Markdown lint pass.

Maintainers use the more detailed [maintenance guide](.github/MAINTAINING.md)
for status, artifact, and intersection decisions.
