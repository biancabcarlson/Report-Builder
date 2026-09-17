# Report Builder

**🔗 Live demo:** https://biancabcarlson.github.io/Report-Builder/

Every case report needs the same skeleton — case ID, account info, summary, findings, disposition — but retyping it each time (or copy-pasting an old report and forgetting to update something) wastes time and invites mistakes. Define your template once — section headers and fields, fully customizable, nothing prescribed by the tool — then fill in a form and get a consistently formatted report every time.

## Web demo

The default template is prefilled from the `simulated-account` fixture (case info, account summary, Suspected Fraud Dates, findings, documents collected, a disposition marked "if confirmed fraud") plus a few editing conveniences:

- **Transactions Captured** — pulled from the fixture, editable in place; add or remove rows and the total recalculates live. **Undo remove** brings back an accidental deletion.
- **Suspected Fraud Dates** — a native date picker, side by side in a fixed two-column layout so one box can't grow into the other.
- **Summary / Key Observations** — expand to a larger textarea for editing, then collapse back down without losing anything typed.
- **Documents Collected** — an editable list; add a row per document, remove any with **✕**. Renders as a bulleted list in the generated report.
- **Paste results from other tools here** — one or more paste-in boxes for output from other tools in the series (e.g. Timeline Builder's "Copy Timeline," the Calculator's "Copy results"); pasted text stays as-is, monospaced, in the preview and the report. **+ Add tool output** adds another block; **✕** only appears once a block has text in it, so the first empty box can't be deleted by mistake. **Undo remove** brings back the last block removed.

**Submit Report** asks "Are you sure?" before finalizing — one explicit confirm step, so the report can't be finalized by an accidental click.

Runs entirely client-side; nothing is saved, uploaded, or sent anywhere.

## Python CLI

```
python report_template_filler.py template.json answers.json -o report.md
```

## Privacy Mode

The 🔒 Privacy Mode toggle (top right, shared across the suite via `localStorage`) blurs the account holder's name in the generated report preview.

## Other tools in this series

- [Case Calculator](https://biancabcarlson.github.io/Case-Calculator/)
- [Report Builder](https://biancabcarlson.github.io/Report-Builder/) *(this repo)*
- [OSINT Assistant](https://biancabcarlson.github.io/OSINT-Assistant/)
- [Documents Folder](https://biancabcarlson.github.io/Documents-Folder/)
- [Entity Match](https://biancabcarlson.github.io/Entity-Match/)
- [Timeline Builder](https://biancabcarlson.github.io/Timeline-Builder/)
