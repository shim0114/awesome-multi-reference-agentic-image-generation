# Maintaining the Paper Collection

This guide keeps updates consistent, conservative, and easy to review.

## Review workflow

1. Search the existing files by normalized title, arXiv identifier, DOI, and
   known aliases.
2. Verify the title, authors, date, and venue/status on a primary paper page.
3. Read enough of the paper to verify the selected track; a keyword match is
   not sufficient.
4. Verify that project, code, model, and data links are controlled by the
   authors or their organization.
5. Add the paper newest-first within its research category.
6. Update the README's **Latest additions** only when the paper is among the
   most recent records in the collection.
7. Run the checks in the release checklist before merging.

Automated searches may create candidate issues, but must never publish papers
without human review.

## Track decisions

### Multi-reference

The method or benchmark must explicitly handle multiple visual references,
subjects, identities, learned concepts, or heterogeneous reference roles.
Multiple output images, multi-view reconstruction, or a multi-image training
dataset alone does not qualify.

### Agentic generation

An LLM, MLLM, VLM, or explicit controller must materially plan, route, call
tools, retrieve, critique, remember, collaborate, or revise image generation or
generative editing. A fixed pipeline, a one-shot prompt rewrite, or ordinary RL
training alone does not qualify.

### Direct intersection

Record separate evidence for both axes. The agent must act on a task that uses
multiple references, identities, concepts, or a persistent multi-entity visual
memory. Many objects, candidate outputs, or generated samples are not the same
as multiple visual references.

## Status and artifact rules

- Prefer official proceedings or an OpenReview decision over arXiv comments.
- Label an unreviewed work `arXiv preprint`; label a review submission
  `under review` unless an official decision is available.
- When a repository alone claims a venue, say `author-reported` rather than
  presenting it as independently verified.
- Omit missing resources in compact lists. In detailed indexes, distinguish a
  complete release from a README-only, demo-only, or announced repository.
- Treat renamed or extended submissions as one record unless the method changes
  materially. Keep the aliases in the detailed entry.

## Search queries

Use these as discovery prompts across arXiv, OpenReview, CVF, ACL Anthology,
ACM Digital Library, and author repositories. Re-check the paper itself before
including any result.

1. `("multi-reference" OR "multiple reference images") image generation`
2. `("multi-subject" OR "multi-identity") personalized image generation`
3. `("multi-concept" OR "content-style") diffusion customization`
4. `("image generation agent" OR "agentic image generation")`
5. `(LLM OR MLLM OR VLM) (plan OR critique OR repair) image generation`
6. `("visual search" OR "reference selection") agent image synthesis`
7. `("visual memory" OR "character sheet") multi-agent story visualization`
8. `("multi-reference benchmark" OR "multi-image conditioning benchmark")`

## Release checklist

- [ ] Exact paper titles and primary URLs are present.
- [ ] No duplicate arXiv IDs, DOIs, or normalized titles exist within a list.
- [ ] Categories and year ordering are correct.
- [ ] Venue and review-status claims have primary-source evidence.
- [ ] Artifact labels reflect what is actually available.
- [ ] Relative Markdown links resolve.
- [ ] `git diff --check` passes.
- [ ] `npx --yes markdownlint-cli2 README.md CONTRIBUTING.md 'papers/*.md' 'docs/*.md' '.github/*.md'` passes.

## Known edge cases

- The code link announced for SIGMA currently returns 404 and is deliberately
  labeled as an announced repository in the detailed list.
- IA-T2I and Search-T2I are one evolving paper lineage and must not be listed as
  two independent works.
- DiffusionGPT and DiffusionAgent share arXiv:2401.10061 and are one record.
