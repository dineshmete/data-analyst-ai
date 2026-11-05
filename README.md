# Data Analyst AI

A chat-based sales data analyst built on Open WebUI. A user uploads a CSV file, asks questions in plain language, and gets answers computed by pandas code that runs through Open WebUI's Code Interpreter. The language model is NVIDIA Nemotron 3.5 Lightning (free), connected through an API.

The setup checks every row against the formula TotalSales = Quantity × UnitPrice, flags mismatches, and saves a corrected file when the user asks for one. Follow-up questions then use the corrected file.

Tested on a 10-row sales dataset. One row (OrderID 105) had a +200 mismatch. Corrected total: 34,028 (recorded total: 34,228).

## Tools
- Open WebUI (local chat interface)
- NVIDIA Nemotron 3.5 Lightning (free, via API)
- Code Interpreter (runs the model's pandas code)

## Files
- `Data_Analyst_AI_Project_Report.docx`: full project report
- `sales.csv`: original test data
- `sales_corrected.csv`: corrected data (OrderID 105 TotalSales = 4,796)
- `category_chart_corrected.png`: total sales by category, corrected data

## Limitations
- Tested on one small file only.
- Code runs on the host machine and is not isolated.
- Early test runs gave inconsistent answers, so results should be checked against the source data.
