<div align="center">

<img src="https://raw.githubusercontent.com/Studio1HQ/Studio1HQ/main/assets/banners/Studio1.webp" alt="Studio1 Marketing Site (Earlier Version): Source of an earlier studio1hq.com site built with Next.js and MDX" width="100%" />

<br />
<br />

# Studio1 Marketing Site (Earlier Version)

### Source of an earlier studio1hq.com site built with Next.js and MDX

A Next.js 16 and MDX codebase for the Studio1 marketing site: service pages, blog, case studies, careers, a DevRel jobs board and five languages via next-intl.

<br />

[![Built by Studio1](https://img.shields.io/badge/Built_by_Studio1-f97316?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNjAgMTYwIiBmaWxsPSJub25lIj48cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTAgMzVDMCAxNi42ODA3IDE0LjA3NDQgMS42NDg0NCAzMiAwLjEyNjk1M1YxNDFINTEuMDUyM0M1Mi40MzA4IDEzNy4zNDQgNTQuNzQ0NiAxMzMuNjg5IDU3Ljk5MzggMTMwLjAzM0M2MS4xNDQ2IDEyNi41MDggNjQuNjg5MiAxMjMuNDQgNjguNjI3NyAxMjAuODI5QzcyLjU2NjIgMTE4LjM0OSA3Ni4zNTY5IDExNi43ODIgODAgMTE2LjEyOVY4Ni43NTQ0Qzc1LjQ3MDggODcuOTI5MiA3MS4zODQ2IDg5LjY5MTkgNjcuNzQxNSA5Mi4wNDE1QzY0IDk0LjUyMjUgNjAuNzUwOCA5Ny40NiA1Ny45OTM4IDEwMC44NTRDNTYuNTM0NSAxMDIuNzIgNTUuMjU0NSAxMDQuNjU5IDU0LjE1MzkgMTA2LjY3MVYwSDEyNUMxNDQuMzMgMCAxNjAgMTUuNjY5OSAxNjAgMzVWMTI1QzE2MCAxNDQuMzMgMTQ0LjMzIDE2MCAxMjUgMTYwSDEyNFYxOEgxMDQuOTQ4QzEwMy41NjkgMjEuNjgxNiAxMDEuMjU1IDI1LjM2MjggOTguMDA2MiAyOS4wNDQ0Qzk0Ljg1NTQgMzIuNTk0MiA5MS4zMTA4IDM1LjY4NDEgODcuMzcyMyAzOC4zMTRDODMuNDMzOCA0MC44MTIgNzkuNjQzMSA0Mi4zODk2IDc2IDQzLjA0NzRWNzIuNjMwNEM4MC41MjkyIDcxLjQ0NzMgODQuNjE1NCA2OS42NzI0IDg4LjI1ODUgNjcuMzA1N0M5MiA2NC44MDc2IDk1LjI0OTIgNjEuODQ5MSA5OC4wMDYyIDU4LjQzMDdDOTkuNDY1NSA1Ni41NTEzIDEwMC43NDUgNTQuNTk4NiAxMDEuODQ2IDUyLjU3MjNWMTYwSDM1QzE1LjY3IDE2MCAwIDE0NC4zMyAwIDEyNVYzNVoiIGZpbGw9IiNmZmZmZmYiLz48L3N2Zz4K)](https://studio1hq.com)
[![Live demo](https://img.shields.io/badge/Live_demo-1c1917?style=for-the-badge&logo=googlechrome&logoColor=white)](https://studio1hq.com)

[More examples](https://github.com/Studio1HQ) &nbsp;·&nbsp; [studio1hq.com](https://studio1hq.com)

</div>

<br />

## Overview

This repo holds the source of a Studio1 marketing site built with Next.js and MDX. It covers the services pages, a blog, case studies, a careers section and a DevRel jobs board, with content translated into English, Spanish, French, Hindi and Chinese.

It looks like an earlier version of the site. The `website` repo is the one currently published at [studio1hq.com](https://studio1hq.com) and was updated more recently, so treat this repo as reference code.

## Features

- **Service pages**: technical content marketing, developer video production, DX and documentation audits, and DevRel growth campaigns.
- **Blog**: MDX posts in `content/blog` rendered with `next-mdx-remote`.
- **Case studies**: MDX content with highlights, quotes, stats, related studies and a table of contents.
- **Careers**: job listings from Markdown files in `content/careers/jobs`, with detail pages.
- **DevRel jobs board**: a page plus a GitHub issue template (`submit-devrel-job.yml`) for submitting roles.
- **Internationalization**: `next-intl` with message files for `en`, `es`, `fr`, `hi` and `zh`.
- **Agent-readable site**: `public/llms.txt`, a sitemap route and a JSON 404 from `/api` that points to them. `pnpm test:agent-readiness` runs a check script.

## Tech stack

| Layer | Tool |
| --- | --- |
| Framework | [Next.js](https://nextjs.org) 16 (App Router), React 19, TypeScript |
| Content | [MDX](https://mdxjs.com) with `@next/mdx`, `next-mdx-remote` and `gray-matter` |
| i18n | [next-intl](https://next-intl.dev) |
| Styling | [Tailwind CSS](https://tailwindcss.com) 3, `tailwindcss-animate` |
| Animation | [Motion](https://motion.dev) |
| Package manager | [pnpm](https://pnpm.io) 9 |

## Getting started

### Prerequisites

- Node.js 24.x (see `.nvmrc` and `engines` in `package.json`)
- pnpm 9

### Installation

```bash
git clone https://github.com/Studio1HQ/Studio1.git
cd Studio1
pnpm install
```

### Environment variables

None were found in the build config, sitemap route or proxy. Add a `.env.local` if you extend the site with services that need keys.

### Run

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000). Other scripts: `pnpm build`, `pnpm start`, `pnpm lint`, `pnpm format`, `pnpm test:agent-readiness`.

## How it works

```text
app/(site)/        # English routes: services, blog, case-studies, careers, devrel-jobs, about-us, ...
app/[locale]/      # localized routes and metadata
app/api/           # JSON 404 payload pointing to sitemap and llms.txt
components/        # blog, case-studies, careers, about-us, sections, pages
content/           # blog and case-study MDX, careers Markdown, legal pages
messages/          # next-intl strings: en, es, fr, hi, zh
public/            # assets, case study images, llms.txt
AGENTS.md          # repository guidelines for contributors and coding agents
```

`.mcp.json` registers the `next-devtools` MCP server for local development.

## Resources

- [studio1hq.com](https://studio1hq.com): the live Studio1 site.
- [Studio1HQ/website](https://github.com/Studio1HQ/website): the current site repository.
- [Next.js documentation](https://nextjs.org/docs): framework reference.
- [next-intl documentation](https://next-intl.dev): internationalization library used here.

<br />

---

<div align="center">

<a href="https://studio1hq.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Studio1HQ/website/main/brand/studio1-logo-on-dark.svg" />
    <img src="https://raw.githubusercontent.com/Studio1HQ/website/main/brand/studio1-logo-on-light.svg" alt="Studio1" width="160" />
  </picture>
</a>

Built by **[Studio1](https://studio1hq.com)**, the technical content and DevRel partner for devtool teams.<br />
Browse more open-source examples at [github.com/Studio1HQ](https://github.com/Studio1HQ).

[![Website](https://img.shields.io/badge/studio1hq.com-0b0807?style=for-the-badge&logo=googlechrome&logoColor=white)](https://studio1hq.com)
[![Book a call](https://img.shields.io/badge/Book_a_strategy_call-f97316?style=for-the-badge&logo=googlecalendar&logoColor=white)](https://cal.com/studio1/collab)
[![X](https://img.shields.io/badge/%40Studio1HQ-141414?style=for-the-badge&logo=x&logoColor=white)](https://x.com/Studio1HQ)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/studio1hq/)

<sub><a href="https://studio1hq.com">studio1hq.com</a> · Technical content, docs, video and DevRel for devtools</sub>

</div>
