# Contributing to Awesome LLM for Biomedicine

Thank you for helping keep this list useful. It is a curated research and engineering resource for biomedical and clinical language models, datasets, tools, benchmarks, and papers.

## What belongs here

- **Models** — biomedical, clinical, molecular, protein, genomics, or medical vision-language models.
- **Datasets and benchmarks** — resources with documented provenance, tasks, and access requirements.
- **Tools** — libraries, pipelines, agent frameworks, or formats that support biomedical LLM work.
- **Papers** — influential work that defines or advances the field.
- **Corrections** — outdated descriptions, broken links, misplaced entries, or licensing/access notes.

General-purpose resources without a clear biomedical use case do not belong here. Closed models may be included when they are important to the field, but the entry should say when a model is not open-weight.

## Before opening a pull request

Please check that:

- The resource is not already listed under another name or section.
- The primary link is stable and points to an official project page, model card, dataset page, or paper.
- The description explains the biomedical use case in one concise line.
- Claims such as parameter counts, dataset sizes, benchmark results, and access requirements are supported by the linked source.
- The entry is placed in the most specific existing section.
- New or changed links work, and the README keeps its current bullet-list format.

For a local lint check, run:

```bash
npx --yes awesome-lint README.md
```

## How to submit a resource

1. Open an issue using the resource-suggestion template, or fork the repository and create a branch.
2. Add one bullet to the appropriate section of `README.md`.
3. Keep the description to one line and avoid marketing language or unsupported superlatives.
4. Open a pull request with a descriptive title and enough context for review.

Suggested entry pattern:

```markdown
- [Resource](https://example.org) - Task or domain. One concise description of what it provides.
```

For models, include parameter count or pretraining data only when the source documents it. For datasets, include the task and meaningful size or access requirements when known. For papers, include the year, full title, and an open-access link when available.

## Review principles

Submissions are reviewed for relevance, clarity, source quality, public accessibility, and whether they add something distinct from an existing entry. The list does not rank resources, endorse clinical use, or replace independent safety, privacy, regulatory, or licensing review.

## Questions

Open an [issue](https://github.com/infonality/awesome-llm-biomedicine/issues) if you are unsure where a resource belongs or whether an entry needs updating.
