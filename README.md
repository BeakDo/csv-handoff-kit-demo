# CSV Handoff Kit — sample report

## CSV 변경 내역 비교 예시

주문 CSV 두 개를 비교할 때 행 번호만 보면 정렬이 바뀐 것인지, 주문 자체가 바뀐 것인지 헷갈리기 쉽습니다. 이 예시에서는 `order_id`를 기준으로 지난 목록(`before.csv`)과 새 목록(`after.csv`)을 맞춥니다.

| 주문 번호 | 지난 목록 | 새 목록 | 결과 |
| --- | --- | --- | --- |
| 001 | 노트, pending | 노트, shipped | 상태 변경 |
| 002 | 펜, shipped | 펜, shipped | 그대로 |
| 003 | 폴더, pending | 없음 | 삭제 |
| 004 | 없음 | 연필, pending | 추가 |

두 CSV와 [완성된 HTML 보고서](sample-report.html)를 무료로 볼 수 있습니다. 모두 가상 문구 주문이며 실제 고객 정보는 없습니다. 보고서 파일을 내려받아 브라우저에서 열면 됩니다. 스크립트나 외부 리소스를 불러오지 않습니다.

작은 파일이라면 직접 비교해도 충분합니다. 반복해서 보고서를 만들거나 다른 사람에게 전달한 뒤 원본 파일로 결과를 다시 확인해야 한다면 [CSV Handoff Kit 상품 페이지](https://payhip.com/b/gNPq7)에서 미리보기와 사용 조건을 먼저 살펴보세요. 유료 파일은 **미화 1달러**이며, 이 저장소에는 실행 도구가 들어 있지 않습니다.

도구는 Python 3.10 이상과 터미널이 필요합니다. 파일당 최대 20 MiB의 CSV만 받고, 두 파일의 열 이름과 고유 키가 맞아야 합니다. XLSX나 비슷한 값 찾기는 지원하지 않습니다. 보고서에 원본 값이 담기므로 민감한 자료를 다룬다면 공유 전에 직접 확인해야 합니다.

## English

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

