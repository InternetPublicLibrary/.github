# Contributing to the Internet Public Library

This guide applies to every repository in the [InternetPublicLibrary](https://github.com/InternetPublicLibrary) organization that does not have its own `CONTRIBUTING.md`. A repository's own guide (or `AGENTS.md`) wins where it is more specific.

## Opening an issue

Blank issues are disabled. Pick the form that fits:

| Form | Use it for |
| --- | --- |
| **Bug report** | Something on the site or in the build is broken. |
| **Feature request** | A new capability or an improvement. |
| **Content suggestion** | A website, article, book or educational resource to add to the library. One resource per issue. |
| **Task** | Maintainer and roadmap work: refactors, infrastructure, docs, chores. |

You can also suggest a resource without a GitHub account at [ipl.better-web.org/en-US/submit-resource/](https://ipl.better-web.org/en-US/submit-resource/).

## Opening a pull request

1. Open or find an issue first, unless the change is trivial (typo, broken link).
2. Create a branch (see naming below) and keep the PR focused on one change.
3. Fill in the PR template: ELI5, what and why, linked issues (`Closes #12`), how you tested it (commands and results), screenshots for UI changes, AI disclosure and the checklist.
4. Make sure the build and tests pass, and consider both language editions (en-US and pt-BR).

## ELI5: "Explain it like I'm five"

Every issue and PR starts with an ELI5: one or two sentences that someone with no technical background can understand. It helps reviewers, translators and future readers know *what* and *why* before reading the details.

> **Technical:** Replace the client-side substring match in `javascript/search.js` with a Fuse.js index built from `api/search.json`, threshold 0.3.
>
> **ELI5:** Search will still find the right page when you make a small typo, like "pyhton" instead of "python".

Avoid jargon, file names and acronyms in the ELI5. Put them in the technical section.

## AI disclosure policy

**AI tools are welcome. Undisclosed AI use is not.**

Why: reviewers read AI-generated text and code differently. They check more carefully for confident mistakes, invented facts, made-up APIs and license issues. Disclosure lets them review at the right depth, and keeps the project's history honest.

Every issue and PR declares one level:

| Level | Meaning | Label |
| --- | --- | --- |
| No AI used | A human wrote all of it. | `ai:none` |
| AI-assisted | A human wrote it; AI helped with parts (autocomplete, suggestions, rephrasing). | `ai:assisted` |
| AI-generated | AI wrote most of it; a human reviewed it. | `ai:generated` |

Rules:

- Name the tools or models you used (for example "Claude (Claude Code)", "GitHub Copilot").
- A human is always responsible. If you submit it, you must have read and understood every line and be able to explain it in review.
- Do not paste content an AI produced from sources you cannot verify (quotes, statistics, links). Check links and facts yourself.
- Commits with significant AI help may carry a `Co-Authored-By:` trailer naming the tool, for example `Co-Authored-By: Claude <noreply@anthropic.com>`. The human remains the author.

Maintainers apply the matching `ai:*` label during triage. The full label set is in [`.github/labels.yml`](.github/labels.yml).

## Commits

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<optional scope>): <short summary in the imperative>
```

Types: `feat`, `fix`, `docs`, `content`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`. Examples:

```
feat(search): add category filter to search results
fix(i18n): link pt-BR language switch to the matching page
content(computing): add MIT OpenCourseWare algorithms course
```

**Sign your commits** (GPG or SSH signing) so they show as "Verified" on GitHub. See [GitHub's guide to signing commits](https://docs.github.com/en/authentication/managing-commit-signature-verification/signing-commits). Never rewrite another person's authorship.

## Branch names

`<type>/<issue-number>-<short-description>`, for example `feat/42-search-filters`, `fix/57-pt-br-menu`, `docs/61-api-endpoints`.

## Review expectations

- At least one maintainer approval before merge; CI must be green.
- Reviewers check correctness, en-US/pt-BR parity, accessibility for UI changes, and that the AI disclosure matches the work.
- Address every review comment, by changing the code or by replying with your reasoning.
- Keep PRs small. Large PRs take longer to review and may be asked to split.

## License

By contributing, you agree that your contribution is licensed under the license of the repository you contribute to (see its `LICENSE` file).
