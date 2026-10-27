# The EACW's glosses in other languages

Glosses of the EACW's items in languages of wider communication, for showing a speaker an elicitation prompt in a language they know. **The English gloss and its Clarification are always the baseline**; these glosses translate them.

One file per language, named by its ISO 639-3 code (`fra.tsv`, `arb.tsv`, `amh.tsv`), with these columns:

| Column | |
|---|---|
| `ref` | the EACW reference |
| `gloss` | the gloss; it may give two options separated by a comma, or a short phrase, since it is a prompt, not a file name |
| `clarification` | the language's own short note on its gloss (register, a regional sense, a warning), usually empty |
| `status` | `machine` (made and audited by machine translation) or `checked` (checked by a person) |
| `checked_by` | who checked it |
| `back_translation` | an independent translation of the gloss back into English, made without seeing the English |
| `earlier` | earlier glosses shipped in a released edition, so an update can tell them apart |

`STATUS.tsv` gives each language's status (*Fully human audited*, *Partially human audited* or *Machine audited only*), the sections done, and the edition it was last released with.

**How they are made:** each gloss is translated from the English and its Clarification, with dictionaries and other lists as cross-checks; translated back into English independently; and judged against the English, item by item, with anything unsettled flagged for a person. Earlier glosses are kept as evidence and never translated over; a checked gloss is never changed by machine.

Corrections are welcome: open an [issue](../../issues) with the reference, the language and the better gloss.
