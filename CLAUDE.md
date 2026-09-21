# Project notes

## Source of truth
Pulse is an attached local codebase folder (`Pulse/`), not a GitHub repo. Browse with the
`local_*` tools (`local_ls`, `local_read`, `local_grep`). Key docs:

- `Pulse/docs/ARCHITECTURE.md` — layers, record spine, module contract, permissions, Helios chain
- `Pulse/docs/HELIOS.md` — tools, effects (read/write/external), confirmation hashes, channels
- `Pulse/packages/core/src/domain/core-module.ts` — core routes + navigation (sections: primary, work, data, admin)
- `Pulse/apps/demo/pulse.config.ts` — client config: branding, terminology, modules, home widgets, features
- `Pulse/packages/modules/site-visits` — the reusable module fixture

## Mockup files
- `Pulse v4 Glass.dc.html` — the Rivet Steel build: dark liquid glass on gunmetal `#2B3440` with
  safety orange `#F2691B` as the single accent, icon rail with hover labels, Home = Helios chat +
  right rail, plus the page set (action inbox, work queues, approvals, timesheets, payroll run,
  job margin, invoices, assets, compliance, records, activity, automations, system health,
  modules, notifications, settings).
- Modules live in the sidebar, pages in the top bar. Nothing else.

## Running the demo
- `python3 serve.py` (or double-click `Start Demo.command`) serves `Pulse v4 Glass.dc.html` at
  http://pulse.localhost:8080, plus only the files it needs. The preview pane's launcher can't read
  ~/Downloads (macOS privacy), so start the server from the shell and attach the pane via `.claude/launch.json`.
- `vendor/` holds React 18.3.1 and the fonts so the demo runs offline; the page loads them before `support.js`.
- Upcoming dates in the mockup data are computed from today (helpers at the top of the logic script).
- `DEMO-SCRIPT.md` lists the questions Helios has real answers for.

## The Rivet Steel data
- Every figure on a screen is generated in one block near the top of the logic script (`BIZ`,
  `COUNTRIES`, `SITES`, `JOB_DEFS`, `WORKERS`, `INVOICES`, `SUPPLIERS`, `VANS`, `HOUSES`, `CERTS`).
  Counts, values and badges are computed from those rows, so a filter pill and the list under it
  cannot disagree. Change the constants, not the copy.
- The three story threads run identically on Home, the Briefing agent, Work and Activity:
  312 unprocessed invoices worth €486,200 with 28 past terms at €71,400; week 38 payroll of
  €218,600 for 134 men with 9 timesheets missing, all at Aarhus; and Aarhus Logistics Hub, an
  €840,000 fixed price job at 62% complete whose margin has fallen from 18% to 9.4%, a €72,000 swing.
- Invoices, Timesheets, Payroll Run, Job Margin, Assets and Compliance all render through one list
  page (`buildDataPage`) plus one template block, so a new module page is a data definition rather
  than new markup.

## Conventions the mockups should keep
- Helios never executes write/external tools; it proposes and waits for a confirmation bound to hashed arguments.
- The action inbox answers three things per item: what happened, why it matters, what I can do.
- Metrics, nav, pages and Helios tools all come from the registry — module contributions are labelled as the module's.
