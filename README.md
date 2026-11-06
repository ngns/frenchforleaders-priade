# French for Leaders

This repository is the PRIADE governance companion for French for Leaders. It
holds the project context, working instructions, and durable bindings for the
website repository.

French for Leaders provides individual French coaching for leaders and teams,
with a focus on business communication in Switzerland and across French-speaking
markets. The current messaging emphasises lessons tailored to each client's
industry, working situations, goals, and schedule, delivered in person, online,
or through a hybrid model. The website's principal goal is an initial consultation.

## Repositories and workspace

| Repository | Role | Path within the project umbrella |
| --- | --- | --- |
| [frenchforleaders-priade](https://github.com/ngns/frenchforleaders-priade) | Project context and PRIADE governance | `frenchforleaders-priade/` |
| [frenchforleaders-website](https://github.com/ngns/frenchforleaders-website) | Website source | `applications/frenchforleaders-website/` |

```text
french-for-leaders/                 # Local umbrella; not a Git repository
├── AGENTS.md                       # Local framework and routing instructions
├── .runtime/priade/                # Local binding and execution contexts
├── frenchforleaders-priade/        # This repository
│   ├── AGENTS.md
│   ├── README.md
│   └── .priade/
│       ├── framework-binding.json
│       ├── governance.json
│       └── repository-bindings/
└── applications/
    └── frenchforleaders-website/   # Separate Git repository
```

The project ID is `frenchforleaders`. The companion declares PRIADE Scenario 2
with framework version `2.11` and schema `2.0`. Durable governance belongs here;
machine-specific framework paths, provider contexts, and runtime state belong
in the local umbrella. Product repositories contain no PRIADE-owned files.

## Source material

The operator maintains the source collection in `75_FrenchForLeaders`. Its local
location is recorded in the umbrella's `AGENTS.md`; the source files are not
copied into this public repository.

| Source within `75_FrenchForLeaders` | Purpose |
| --- | --- |
| `Webpage/FrenchforLeaders_Webpage Messaging New.docx` | Business positioning and current undated website messaging draft |
| `Webpage/FrenchforLeaders_Webpage Messaging New_v20260730.docx` | Dated messaging used for the July prototype |
| `Webpage/Prototyp/French-for-Leaders_Webprototyp_Stand_20260731.md` | Prototype decisions, page structure, and historical open items |
| `Webpage/Prototyp/French-for-Leaders_Webprototyp_v1_20260731.html` | Self-contained visual prototype |
| `CI:CD/` | Corporate identity manual, application guidance, and document references |
| `Logo/Final/` | Final Tricolore, Anthrazit, and negative logo variants |
| `Bildkonzept/` | Image selections, originals, and licence documents |
| `Flyer/FFL_Flyer Image_20261009_final.pdf` | Final October flyer reference |
| `Briefschaften/` | Letter and offer templates, with usage notes |
| `Formulare/` | Self-assessment and individual/group evaluation templates |
| `Unterricht/` | Lesson materials and participation certificate templates |
| `Sales/` | Internal sales material |

The messaging documents contain drafts and unresolved placeholders. The July
prototype records first-person coach copy, a one-page German presentation, and
consultation calls to action. Its open items are a historical checklist, not a
verified description of the current website. Check the relevant dated source and
the current implementation before making a new content decision. Older messaging
and the website repository's own draft content may describe different audiences
or offers.

Preserve Swiss German spelling and the established visual identity. Do not infer
approved prices, qualifications, testimonials, contact details, or outcome
guarantees from placeholders or earlier drafts. Keep internal sales information,
participant information, and licensed source assets in their authorised locations.

## Website baseline

The website was cloned from its existing `main` branch on 6 November 2026. The
version-one baseline is the branch [`v1/main`](https://github.com/ngns/frenchforleaders-website/tree/v1/main)
at commit [`c65bf89177d41c6fd31dbc3efbb3ebda0896181e`](https://github.com/ngns/frenchforleaders-website/commit/c65bf89177d41c6fd31dbc3efbb3ebda0896181e).
`main` remains the working branch for subsequent changes. The V1 marker is a
branch, not a Git tag.

The existing implementation uses React, TypeScript, Vite, and Tailwind CSS. Its
build produces static files in `dist/public` and bundles an Express server for
serving them. The package manager is pinned in the website's `package.json`.

From the website checkout, the existing commands are:

```sh
pnpm install --frozen-lockfile
pnpm dev
pnpm check
pnpm build
pnpm preview
```

These are the repository's existing development commands; dependency installation
and application validation are separate from this governance bootstrap.

## Working with PRIADE

Start from the local umbrella and read its `AGENTS.md`. It supplies the explicit
framework locator, repository inventory, workspace binding, and routing commands.
Select the companion for governance and project documentation, or the website
for application changes. Route multi-repository work separately for each selected
repository. Use the bound provider for Git operations and keep local runtime data
outside both repositories.

For a new workstation, create a non-Git umbrella, clone this companion into it,
and supply an explicitly chosen compatible PRIADE framework checkout. With the
framework at the configured relative locator `../priade`, run from the umbrella:

```sh
../priade/runtime/priade/priade.sh init-project \
  --project-root . \
  --framework ../priade \
  --companion frenchforleaders-priade
```

The committed governance catalog identifies the website repository. PRIADE uses
it to reconstruct the application checkout and local bindings. Do not copy
another workstation's `.runtime/` directory or infer a framework from nearby
directory names.

Validate each repository from the configured umbrella:

```sh
../priade/runtime/priade/priade.sh check --scenario governed-app \
  --workspace-binding .runtime/priade/workspace-binding.json \
  --workspace frenchforleaders-priade

../priade/runtime/priade/priade.sh check --scenario governed-app \
  --workspace-binding .runtime/priade/workspace-binding.json \
  --workspace applications/frenchforleaders-website
```
