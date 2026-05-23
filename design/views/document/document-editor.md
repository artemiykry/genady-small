# DocumentEditor

The editing surface for a document body.

- **Purpose** — produce a new `body` markdown string.
- **Shows** — current buffer; cursor; autocomplete popovers.
- **Actions** — emit changed body (consumer calls `edit_document`); insert `@person` / `[[entity]]` via autocomplete (syntax only — no function call).
- **States**
  - *idle* — buffer matches the saved body.
  - *dirty* — buffer diverges from saved body.
  - *autocomplete-open* — popover active over a `@` or `[[` trigger.
- **Composed of** — markdown text area, autocomplete popover, embed picker.
