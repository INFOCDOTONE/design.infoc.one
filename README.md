# INFOC ONE — Design

The public design reference for **INFOC ONE**, the Singapore-first, AI-native business suite that unifies finance, payroll, sales, inventory, POS, projects, and planning around a single architectural contract.

Full reference: **https://design.infoc.one**

## The idea

Singapore SMEs run on 3 to 5 disconnected tools, and month-end becomes a reconciliation crisis. INFOC ONE replaces that with one connected system: eight applications on one ledger, with AI on top.

```
ONE ERP   ONE HRM   ONE CRM   ONE POS   ONE WMS   ONE EPM   ONE PSA   ONE AI
```

## Design principles

- **Singapore first, not Singapore adapted.** CPF, GST, InvoiceNow, and PayNow are first-class features built into the core data model.
- **Statutory values are data, never code.** Government-set rates live as effective-dated data, so a change is a data edit, not a release.
- **One writer, one truth.** For anything that matters, exactly one part of the system is allowed to write it.
- **AI proposes; humans approve.** No agent can act alone on a consequential financial action.
- **Data is permanent.** Posted records are corrected by reversal, never erased.

## Architecture at a glance

- A modular monolith: one deployable engine with strict per-domain module boundaries, bound by a single shared contract (ONEKernel).
- Physical per-tenant isolation, so one company can never reach another company's data.
- Compliance held as effective-dated data, dated to each document.
- Six domain Beacons (Finance, Sales, HR, Operations, Service, Compliance) that watch the business and propose, never post, on their own.

## Product

<table>
  <tr>
    <td width="50%"><img src="product/pulse-home.png" width="100%" alt="Business Pulse"><br><sub>Business Pulse: your day at a glance</sub></td>
    <td width="50%"><img src="product/one-ai-chats.png" width="100%" alt="Ask ONE AI"><br><sub>Ask ONE AI in plain language</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="product/one-beacon.png" width="100%" alt="Beacon proposals"><br><sub>Beacon proposals waiting on your approval</sub></td>
    <td width="50%"><img src="product/erp-home.png" width="100%" alt="ONE ERP"><br><sub>ONE ERP, the ledger spine</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="product/crm-beacon.png" width="100%" alt="Sales Beacon"><br><sub>Sales Beacon watching the pipeline</sub></td>
    <td width="50%"><img src="product/hr-beacon.png" width="100%" alt="HR Beacon"><br><sub>HR Beacon watching payroll and CPF</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="product/epm-budget.png" width="100%" alt="EPM budgeting"><br><sub>EPM budgeting and planning</sub></td>
    <td width="50%"><img src="product/epm-cashflow.png" width="100%" alt="EPM cashflow"><br><sub>Cashflow projected from the ledger</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="product/one-ai-ledger.png" width="100%" alt="AI ledger"><br><sub>Every AI action traceable in the ledger</sub></td>
    <td width="50%"><img src="product/group-pulse.png" width="100%" alt="Group Pulse"><br><sub>Group Pulse across entities</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="product/flow-today.png" width="100%" alt="Today's flow"><br><sub>Today's flow at a glance</sub></td>
    <td width="50%"><img src="product/crm-ledger.png" width="100%" alt="CRM ledger"><br><sub>CRM activity on one ledger</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="product/hrm-ledger.png" width="100%" alt="Payroll ledger"><br><sub>Payroll posted to the same ledger</sub></td>
    <td width="50%"><img src="product/psa-ledger.png" width="100%" alt="PSA ledger"><br><sub>PSA projects, time, and margin</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="product/epm-ledger.png" width="100%" alt="EPM consolidation"><br><sub>EPM consolidation</sub></td>
    <td width="50%"><img src="product/epm-ai-evidence.png" width="100%" alt="AI evidence"><br><sub>AI evidence attached to the numbers</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="product/erp-pulse.png" width="100%" alt="ERP daily pulse"><br><sub>ERP daily pulse</sub></td>
    <td width="50%"></td>
  </tr>
</table>

---

Built Singapore-first. Full design reference at **https://design.infoc.one**
