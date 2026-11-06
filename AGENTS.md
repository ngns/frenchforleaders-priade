# AGENTS.md

<!-- BEGIN PRIADE GOVERNANCE -->
This companion repository explicitly owns PRIADE Scenario 2 governance.

## External Governance Identity

PRIADE Governance Resolution: operator-workspace-binding
PRIADE Framework Version: `2.11`
PRIADE Project ID: frenchforleaders
PRIADE Repository ID: frenchforleaders-priade
PRIADE Repository Role: companion

Durable project governance, repository bindings, policies, personas, and
application-specific skills live in this companion. Product repositories remain
free of PRIADE-owned files. The non-Git project umbrella supplies the exact
workspace binding, framework entrypoint, repository target, and external
runtime context. Never infer those values from sibling directories.
<!-- END PRIADE GOVERNANCE -->

## Project Scope

This companion governs French for Leaders and the
`ngns/frenchforleaders-website` application. Read `README.md` for project context
and the source-material index. Keep project guidance and durable governance in
this repository, application changes in the explicitly bound website checkout,
and machine-specific paths and execution state in the non-Git umbrella.

Read the umbrella's `AGENTS.md` before acting. Use its exact framework entrypoint,
workspace binding, repository selection, and atomic sync or routing command.
Bootstrap intent follows its initialization path before normal routing. Do not
use the personal Scenario 2 fallback when these local instructions supply a
command. Do not scan sibling projects or infer repository or framework bindings.

## Content and Source Material

- The source collection is `75_FrenchForLeaders`; its exact local path belongs
  in the umbrella instructions. Read only sources relevant to the task.
- Current business messaging focuses on French coaching for leaders and teams,
  adapted to their industry and working situations. The website's principal
  conversion is an initial consultation.
- Use the applicable dated messaging, final identity assets, and recorded design
  decisions. Treat draft placeholders, earlier audience definitions, and the
  July prototype's open items as historical context until checked against the
  current source and implementation.
- Use Swiss German spelling in German copy. Follow the first-person coach voice
  documented for the website. Preserve the established brand identity.
- Do not invent or silently approve prices, qualifications, testimonials, contact
  information, or claims about learning outcomes. Resolve material conflicts
  with the operator when the available sources do not settle them.
- This companion is public. Keep internal lead lists, correspondence, participant
  data, credentials, and licensed source files out of commits. Refer to the
  source collection without copying it wholesale.

## Website and Version Control

- The website checkout is `applications/frenchforleaders-website` relative to
  the umbrella. Its application code remains separate from this repository.
- `v1/main` records the original website baseline at
  `c65bf89177d41c6fd31dbc3efbb3ebda0896181e`; use `main` for new work unless the
  operator explicitly chooses another branch. Do not move the baseline as part
  of routine work.
- Inspect the selected repository's branch and working tree before changes.
  Preserve unrelated work and stage only the intended files. Use the existing
  package manager and lockfile for website work.
- Validate documentation and bindings for governance changes. For website code
  changes, run relevant existing checks and build commands; verify rendered
  behaviour when the change affects the interface. Report any checks not run or
  failures that remain.
- Keep `.runtime/`, local manifests, dependency directories, build output, and
  machine-specific absolute paths outside committed governance.

## Computer and Browser Access

- System-wide computer control is not authorised. Do not use desktop mouse or
  keyboard automation, OS-wide accessibility, system screen capture, or arbitrary
  native-app control.
- Use a separate isolated headless Playwright browser by default. Do not attach
  to or launch an external user Chrome/Edge session, existing profile, or remote
  debugging session. A connector controlling such a browser is not isolation.
- For browser screenshots, use a virtual viewport at least 1280 pixels wide,
  normally 1600 by 1100. Verify legibility and capture the relevant element or
  adjust the viewport when needed.
- If login or MFA requires user interaction, prefer the ChatGPT internal browser
  when available and request the specific confirmation. Never request passwords,
  tokens, or MFA codes in chat.
