# Nike Financial Performance & Profitability Analysis

## Overview

This project analyses Nike's financial performance from FY2020 to FY2026 using financial statement data retrieved programmatically from the SEC EDGAR Company Facts API.

The objective is to evaluate how Nike's financial performance has evolved, identify the main drivers of changes in profitability and cash generation, assess its financial position, and explore potential FY2027 operating outcomes through scenario analysis.

## Key Areas of Analysis

- Revenue growth and profitability trends
- Gross margin and SG&A cost development
- EBIT and net income performance
- Operating cash flow and free cash flow
- Working-capital cash flow impacts
- Liquidity and leverage
- Return on Assets (ROA) and Return on Equity (ROE)
- FY2027 Bear, Base and Bull scenario analysis

## Tools & Methods

- **Python**
- **pandas** for data manipulation and financial analysis
- **requests** for SEC EDGAR API data retrieval
- **matplotlib** for financial data visualisation
- Financial ratio and margin analysis
- Cash flow and working-capital analysis
- Scenario-based financial forecasting

## Data Source

Financial statement data are retrieved from the SEC EDGAR Company Facts API using Nike's CIK.

Annual 10-K observations are filtered to fiscal-year data, duplicate reporting dates are resolved by retaining the latest filed observation, and monetary values are converted to USD billions.

Selected figures and financial definitions were cross-checked against Nike's annual filings.

## Key Findings

- Nike experienced significant operating pressure in FY2025, with revenue declining 9.84% and EBIT declining 42.22%.
- EBIT margin fell from 12.73% in FY2024 to 8.16% in FY2025 and remained at 8.30% in FY2026, indicating stabilisation rather than a full profitability recovery.
- Free cash flow declined from $6.62bn in FY2024 to $2.18bn in FY2026.
- FY2026 operating cash flow was affected by unfavourable working-capital movements, particularly receivables and payables/other operating liabilities.
- Interest-bearing borrowings declined from $9.66bn in FY2020 to $7.94bn in FY2026, while the Current Ratio declined to 1.96.
- ROA declined from 16.58% in FY2021 to 8.29% in FY2026, while ROE declined from 55.01% to 22.14%.
- The FY2027 scenario analysis produces EBIT outcomes ranging from approximately $3.38bn in the Bear case to $5.21bn in the Bull case, with a Base-case estimate of approximately $4.30bn.

## FY2027 Scenario Analysis

Three illustrative scenarios are constructed using revenue growth and EBIT margin as the primary operating drivers:

| Scenario | Revenue Growth | EBIT Margin | FY2027 Revenue | FY2027 EBIT |
|----------|---------------:|------------:|---------------:|------------:|
| Bear | -3.0% | 7.5% | $45.01bn | $3.38bn |
| Base | 3.0% | 9.0% | $47.79bn | $4.30bn |
| Bull | 7.0% | 10.5% | $49.65bn | $5.21bn |

These scenarios are illustrative analytical assumptions and do not represent Nike management guidance or market consensus forecasts.

## Methodology Notes

- EBIT is constructed using pre-tax income and net interest and was validated against Nike's reported EBIT figures.
- Interest-bearing borrowings include short-term borrowings and current and noncurrent long-term debt but exclude operating lease liabilities.
- The SEC standardized `ShortTermBorrowings` concept does not provide a FY2026 observation for Nike. Nike's FY2026 filing reports Notes Payable of $0, so FY2026 short-term borrowings are manually set to $0.0bn.
- Working-capital analysis focuses on selected standardized components available through SEC XBRL data.
- ROA and ROE use average total assets and average shareholders' equity.
- Scenario results are illustrative rather than predictive forecasts.

## Project Structure

```text
nike_financial_analysis/
├── nike_financial_analysis.ipynb
├── README.md
├── requirements.txt
└── .gitignore

## Author

**Eleftherios Evangelou**

MSc Banking & Finance | Finance & Data Analytics