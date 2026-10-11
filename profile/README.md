<p align="center">
  <img src="https://raw.githubusercontent.com/InternetPublicLibrary/.github/main/profile/logo.png" alt="Internet Public Library logo" width="120" height="120">
</p>

<h1 align="center">Internet Public Library</h1>

<p align="center">
  A free, community-curated, Wikipedia-style library of internet resources — in English and Portuguese.<br>
  <a href="https://ipl.better-web.org">ipl.better-web.org</a> ·
  <a href="https://ipl.better-web.org/en-US/">English</a> ·
  <a href="https://ipl.better-web.org/pt-BR/">Português</a> ·
  a project of the <a href="https://better-web.org">Better Web Initiative</a> (open source)
</p>

---

IPL organizes the web's best learning resources — sites, tools, databases, courses, publications and events —
into a library of categories, subcategories and sections, each with an article, a community wiki and a discussion.
Everything is open: the site, the content, the data and the services that let readers contribute.

## Repositories

| | Repository | What it is | License |
| --- | --- | --- | --- |
| 🌐 | [IPLibrary-website](https://github.com/InternetPublicLibrary/IPLibrary-website) | The site: Jekyll layouts, design system, data, curated resources and the build | GPL-3.0 |
| 📘 | [en-US](https://github.com/InternetPublicLibrary/en-US) | English pages (git submodule of the site) | GPL-3.0 |
| 📗 | [pt-BR](https://github.com/InternetPublicLibrary/pt-BR) | Portuguese pages (git submodule of the site) | GPL-3.0 |
| ✏️ | [contribute](https://github.com/InternetPublicLibrary/contribute) | Signed-in edits and resource suggestions as reviewed pull requests — GitHub or ORCID sign-in, Cloudflare Workers (hard fork of Staticman) | MIT |
| 💬 | [discuss](https://github.com/InternetPublicLibrary/discuss) | Comments on IPL pages in GitHub Discussions — GitHub or ORCID sign-in (hard fork of giscus) | MIT |
| ⚙️ | [.github](https://github.com/InternetPublicLibrary/.github) | This profile, default issue forms, PR template and [contributing guide](https://github.com/InternetPublicLibrary/.github/blob/main/CONTRIBUTING.md) | — |

## How to contribute

- **Suggest a resource** — [Submit a resource](https://ipl.better-web.org/en-US/submit-resource/) ·
  [Enviar recurso](https://ipl.better-web.org/pt-BR/enviar-recurso/). It opens a prefilled issue that maintainers review.
- **Improve a page** — every page has an **Edit** tab that opens its source file on GitHub.
- **Report a problem** — [Report issues](https://ipl.better-web.org/en-US/report-issues/) ·
  [Reportar problemas](https://ipl.better-web.org/pt-BR/reportar-problemas/).
- **Translate** — [Help translate](https://ipl.better-web.org/en-US/translate/) or bring IPL to a new language.
- **Code** — issues and pull requests in each repository; templates ask for an ELI5 summary and an AI-use
  disclosure, and code owners review every change.

## Under the hood

Jekyll and Tailwind CSS on Cloudflare Pages; YAML data for the library tree and resources; Playwright and axe
for end-to-end and accessibility tests; Cloudflare Workers for the `contribute` and `discuss` services.
