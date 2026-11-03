# Treasury budget audit

The app now uses the U.S. Treasury's September FY 2026 Monthly Treasury Statement. The photographed overview is largely FY 2025: its $7.01 trillion total matches FY 2025 federal outlays. The figures in the photos are not automatically valid FY 2026 values, and some do not match the closest Treasury FY 2025 record on a comparable basis.

## FY 2026 totals

| Measure | Treasury value |
| --- | ---: |
| Net outlays | $7,395.8 billion |
| Receipts | $5,403.3 billion |
| Deficit | $1,992.5 billion |

These are reported in Treasury's [Table 9](https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v1/accounting/mts/mts_table_9?filter=record_date:eq:2026-09-30). The app contains all 19 reported budget functions and 77 [subfunctions](https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v1/accounting/mts/mts_table_9_outlays_functions_subfunctions?filter=record_date:eq:2026-09-30), together with 216 selected [Table 5 agency and account lines](https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v1/accounting/mts/mts_table_5?filter=record_date:eq:2026-09-30&page%5Bsize%5D=1000). The accompanying CSV lists every selected account, its Treasury path and direct source link.

## Examples checked against the photos

Amounts are billions of dollars, rounded to one decimal. The screenshot is the visible figure; the Treasury columns are the closest named Treasury account, which can have a different scope. FY 2025 account figures are from Treasury's FY 2025 statement, matched by account path.

| Screenshot line | Screenshot | Treasury FY 2025 | Treasury FY 2026 | Comparison |
| --- | ---: | ---: | ---: | --- |
| SNAP | 106.3 | 106.3 | 95.4 | Same named Treasury account. |
| Medicaid grants to states | 668.1 | 668.1 | 723.0 | Same named Treasury account. |
| Federal crop insurance fund | 13.8 | 13.8 | 15.5 | Treasury's net fund outlays. |
| EPA state and tribal assistance grants | 29.7 | 29.7 | 10.8 | Same named Treasury account. |
| NASA exploration | 7.6 | 7.6 | 7.9 | Same named Treasury account. |
| FEMA Disaster Relief | 48.2 | 51.9 | 31.8 | The pictured amount does not match this Treasury account's FY 2025 figure. |
| National Institutes of Health | 46.3 | 47.3 | 45.6 | Treasury reports NIH as an agency total; scope may differ from the screenshot. |
| IRS enforcement | 6.0 | 7.0 | 5.3 | Treasury's account is broader than the pictured allocation; the screenshot also shows IRS enforcement under justice. |

Medicare's pictured component amounts cannot be treated as additions to net Medicare spending. Treasury FY 2026 reports $1,072.6 billion in net Medicare outlays, while the three Table 5 benefit-payment lines sum to $1,275.7 billion before reconciliation to the net function. The app retains the $203.1 billion reconciliation and limits cuts so the positive net line cannot fall below zero. Holding offsets fixed is a simplifying assumption; actual savings from a policy could be lower or higher.

## What was and was not verified

Treasury amounts were checked against the published September FY 2022–2026 function, subfunction, and account tables; account values in the CSV are reported amounts, not proposed savings. Account-to-subfunction placements in the app are editorial matches because Table 5 does not publish that crosswalk. Calculated reconciliation entries can reflect unmatched accounts, transfers, receipts, and classification differences, and are fixed in the app. Parent and child rows describe overlapping spending and should never be added together.

Not every fine-grained item visible in the photographs can be independently matched to a distinct Treasury Table 5 account. Those amounts were not copied as verified FY 2026 lines; in particular, the Treasury categories can aggregate military branches, veterans programs, education grants, and tax credits differently. The CSV is an inventory of the account lines that could be traced to Table 5, not a claim that every screenshot label was separately verified.

A cut in the app is an arithmetic scenario, not a policy score. It does not establish whether Congress can legally make a cut, how quickly obligations would change, or the effects on receipts, economic activity, or future interest. Net interest and reconciliation entries are held fixed. Some spending lines include benefits or other commitments.
