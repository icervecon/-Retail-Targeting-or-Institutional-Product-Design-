# Replication Package

## Paper

**Title:** *Retail Targeting or Institutional Product Design? Distribution Structures in European UCITS Funds*

**Author:** Ignacio Cervera

This repository contains the data and code required to reproduce the empirical results reported in the paper.

---

## Repository Contents

* `UCITS_Replication_Dataset.xlsx`
  Public replication dataset.

* `UCITS_Replication_Notebook.ipynb`
  Python notebook reproducing the empirical analyses and tables reported in the paper.

* `Management_Group_Mapping.xlsx`
  Mapping file documenting the harmonized management-group classification.

---

## Data Availability

The original dataset was constructed using proprietary information obtained from the London Stock Exchange Group (LSEG) and MiFID II target-market disclosures.

Because the underlying LSEG data are proprietary and subject to licensing restrictions, the original dataset cannot be publicly redistributed.

The replication dataset included in this repository contains all variables required to reproduce the empirical analyses while respecting these licensing restrictions.

---

## Reproducibility Statement

The replication dataset has been designed to reproduce the empirical analyses reported in the paper while respecting the licensing restrictions associated with proprietary LSEG data.

The original proprietary database cannot be publicly redistributed. The public replication dataset therefore contains only the variables required to reproduce the empirical results and excludes restricted information covered by the original data license.

Any differences between the public replication dataset and the original proprietary database are solely attributable to the removal of restricted information and do not affect the empirical results reported in the paper.

---

## Management-Group Harmonization

Management-group classifications were manually harmonized by the author.

Multiple legal entities and country-specific management companies belonging to the same asset-management organization were consolidated into a single management-group identifier. The objective was to capture economically meaningful management platforms rather than legal entities reported by data vendors.

The harmonization mapping is documented in:

`Management_Group_Mapping.xlsx`

---

## Variable Definitions

| Variable                         | Description                                                                              |
| -------------------------------- | ---------------------------------------------------------------------------------------- |
| `fund_id`                        | Anonymous fund identifier.                                                               |
| `management_group_id`            | Harmonized management-group identifier.                                                  |
| `domicile`                       | Fund domicile jurisdiction.                                                              |
| `asset_class_clean`              | Harmonized asset-class classification.                                                   |
| `asset_type_norm`                | Normalized asset-type category.                                                          |
| `has_paid_dividends_i`           | Indicator equal to 1 if the fund exhibits an observed dividend-distribution event.       |
| `effective_income_i`             | Indicator equal to 1 if a non-missing distribution amount is reported.                   |
| `distribution_amount_recorded_i` | Indicator equal to 1 when a cash distribution amount is recorded in the source database. |
| `income_fund_i`                  | Indicator identifying income-oriented fund structures according to LSEG classifications. |
| `dividend_paid`                  | Raw dividend-payment indicator.                                                          |
| `retail_eligible_i`              | Retail-investor compatibility indicator.                                                 |
| `professional_eligible_i`        | Professional-investor compatibility indicator.                                           |
| `eligible_counterparty_i`        | Eligible-counterparty compatibility indicator.                                           |
| `basic_investor_i`               | Basic-investor target-market indicator.                                                  |
| `informed_investor_i`            | Informed-investor target-market indicator.                                               |
| `advanced_investor_i`            | Advanced-investor target-market indicator.                                               |
| `cl1_i` – `cl4_i`                | Investor sophistication category indicators.                                             |
| `log_tna`                        | Natural logarithm of total net assets.                                                   |
| `fund_age_years`                 | Fund age in years.                                                                       |
| `ter`                            | Total Expense Ratio.                                                                     |
| `sharpe_3y`                      | Three-year Sharpe ratio.                                                                 |
| `fixed_income_i`                 | Fixed-income fund indicator.                                                             |
| `equity_i`                       | Equity fund indicator.                                                                   |
| `mixed_assets_i`                 | Mixed-assets fund indicator.                                                             |
| `ireland_i`                      | Ireland domicile indicator.                                                              |
| `luxembourg_i`                   | Luxembourg domicile indicator.                                                           |
| `uk_i`                           | United Kingdom domicile indicator.                                                       |
| `retail_x_fixed_income`          | Interaction between retail compatibility and fixed-income classification.                |
| `disclosure_available_i`         | Availability of MiFID II target-market disclosures.                                      |
| `main_sample`                    | Main estimation sample indicator.                                                        |
| `effective_income_sample`        | Effective-income estimation sample indicator.                                            |
| `soph_sample`                    | Investor-sophistication sample indicator.                                                |
| `cl_sample`                      | Sophistication-category sample indicator.                                                |
| `combined_sample`                | Combined estimation sample indicator.                                                    |
| `sophistication_group`           | Investor sophistication grouping variable.                                               |
| `mgmt_n_funds`                   | Number of funds within the management group.                                             |
| `mgmt_dividend_rate`             | Dividend-distribution rate within the management group.                                  |
| `mgmt_effective_income_rate`     | Effective-income rate within the management group.                                       |
| `mgmt_retail_rate`               | Retail-compatibility rate within the management group.                                   |
| `mgmt_fixed_income_rate`         | Fixed-income rate within the management group.                                           |

---

## Replication Instructions

1. Download all repository files.
2. Place the dataset and notebook in the same working directory.
3. Open `UCITS_Replication_Notebook.ipynb`.
4. Run all notebook cells sequentially.
5. The notebook reproduces all tables reported in the paper.

---

## Software

The analyses were conducted in Python 3 using:

* pandas
* numpy
* statsmodels
* scipy
* openpyxl

---

## Contact

**Ignacio Cervera**
Universidad Pontificia Comillas
Madrid, Spain
