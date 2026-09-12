# CSV Handoff Kit — sample report

Compare two CSV exports, hand over a readable report, and recheck the report against the original files.

This repository contains the **free sample inputs and report**, not the full toolkit. The downloadable Python toolkit is **US$1** at [the Payhip product page](https://payhip.com/b/gNPq7). The seller owns this sample repository and the linked product.

## Inspect the example

Download `sample-report.html` and open it in your browser. It contains no scripts or external resources. The included CSVs use made-up stationery orders, not customer data.

| Order ID | Before | After | Result |
| --- | --- | --- | --- |
| 001 | Notebook, pending | Notebook, shipped | Status changed |
| 002 | Pen, shipped | Pen, shipped | Unchanged |
| 003 | Folder, pending | Missing | Removed |
| 004 | Missing | Pencil, pending | Added |

The leading zeros are preserved. Rows are matched by `order_id`, not by their position in a spreadsheet.

## What the paid download adds

- Python scripts to generate an HTML + JSON report ZIP from your own before/after CSVs.
- A verifier that recomputes both reports from the original files and stored comparison settings.
- Compound keys, explicit UTF-8/CP949 encodings, 11 automated tests, and English/Korean instructions.

The scripts run locally without network calls or third-party runtime packages. No subscription or service account is needed to run them.

## Check fit before buying

Python 3.10+ and terminal use are required. Tested on Windows/Python 3.12 only. This is not an installer, graphical app or Excel add-in.

Comma-separated CSV only, up to 20 MiB per input. Both files need the same column names and unique nonblank keys. Exact text comparisons only: no XLSX, fuzzy matching, number/date normalization or automatic encoding detection. Reports contain source values and are not anonymized.

Rechecking confirms that the same input bytes and settings produce the same report. It is **not** a digital signature, sender authentication, legal certification or a guarantee of business correctness. Comparable free CSV comparison tools exist; the paid item packages this handoff workflow and its examples.

The product was developed with AI assistance. Automated tests and an example run were checked; independent human review is not claimed.

The download includes an MIT license and a 14-day suitability refund policy. No installation service, custom processing, support SLA or future features are promised. See the product page for the full purchase scope.

## License

These sample files use the MIT license in `LICENSE.txt`.
