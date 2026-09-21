# Rivet Steel — Pulse demo script

Rivet Steel erects structural steel: 134 men, nine live sites, five countries, run off Google
Sheets, WhatsApp and Alan's own head. The demo shows the five things that hurt and the five
screens that fix them.

## Start and stop

1. Double-click **Start Demo.command**. Chrome opens at **http://pulse.localhost:8080**.
2. Close that Terminal window when you're done. That stops the demo.

The first time, macOS may ask whether Terminal can access your Downloads folder: click **Allow**.
No internet needed; React and the fonts are bundled in `vendor/`.

## The five pains, and where to show them

| Alan's problem | Screen | The number to land on |
|---|---|---|
| ~100 supplier invoice emails a day, lost within twenty minutes | **Invoices › Inbox** | 312 unprocessed, €486,200, 28 past terms |
| Three currencies, five VAT regimes, one spreadsheet | **Invoices › VAT & Country** | €64,872 reclaimable, three reverse-charge countries |
| Timesheets keyed twice; half sole traders, half PAYE | **Work › Timesheets** and **Work › Payroll Run** | 134 men, 9 missing, €218,600 due Thursday |
| Fixed price jobs only tell you how they went afterwards | **Dashboard › Job Margin** | Aarhus: €840,000, 62% done, 18% → 9.4%, a €72,000 swing |
| Vans, insurance and certs expiring across five countries | **Records › Assets** and **Records › Compliance** | 38 vans, 2 unaccounted, 11 certs inside 30 days |

## Questions Helios answers

Type these on Home, or click the matching suggestion. The wording can change; Helios listens for
the key words.

| Ask | Helios shows | Key words it listens for |
|---|---|---|
| How bad is the invoice backlog? | 312 unprocessed split five ways by country | invoice, backlog, unprocessed, supplier, overdue |
| Where is margin slipping? | Aarhus at 9.4%, €94,000 at risk across nine live jobs | margin, Aarhus, fixed price, job, variation |
| What is missing for Thursday's payroll? | Week 38 by country, nine sheets short | payroll, timesheet, hours, Thursday, missing |
| What expires in the next month? | Eleven documents, Denmark first at six days | cert, insurance, expiring, Safe Pass, road tax |
| Where are the two missing vans? | Both, with no keeper and no tracker ping | van, fleet, house, accommodation, asset |
| Chase the nine on WhatsApp | An external tool: drafts it and waits for your yes | chase, WhatsApp, message, draft, send |

Anything else gets: "Everything I reach goes through a registered tool with a declared permission,
and none of them covers that question yet." It then offers buttons for the questions above, so
click one and carry on.

## Watch out for

- **The WhatsApp chase:** stop at the **NEEDS YOUR YES** card, which is the point to make. Clicking
  **Confirm and send** or **Edit the message** makes Helios draft the same message again.
- **Stay in dark mode.** Light mode is there, but the deck was built on gunmetal.
- **Old link:** `localhost:8080/Pulse%20v4%20Glass.dc.html` no longer works. Use http://pulse.localhost:8080.

## The numbers, if you get asked

134 workers · 9 live sites · 5 countries · 67 sole traders and 67 PAYE · 21 main contractor
clients · €1.42M monthly revenue · €194,000 overdue owed to Rivet Steel · ~100 supplier invoices a
day · 38 vans · 22 rented houses.

Every count on a screen is computed from the rows underneath it, so a filter and a badge cannot
disagree.
