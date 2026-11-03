# Treasury budget audit and screenshot coverage

The app uses the U.S. Treasury's September FY 2026 Monthly Treasury Statement. The photographs largely show FY 2025, and the pictured amounts cannot be substituted directly for FY 2026 figures. The complete screenshot-by-screenshot inventory is in [screenshot-coverage.csv](screenshot-coverage.csv). It records individual visible rows, including repeated rows at screenshot boundaries, subtotals, offsets, and unspecified remainders; figures in the inventory are transcribed from the pictures and can use different scopes or accounting conventions than the matched Treasury line.

## Coverage of the photographs

| Coverage status | Visible rows |
| --- | ---: |
| Treasury account or official category with a corresponding line | 234 |
| Represented by a broader account, rather than the separate pictured breakout | 110 |
| No separate comparable FY 2026 line identified | 8 |
| Unspecified remainder in the photo | 46 |
| Offset or accounting adjustment | 29 |
| TVA, shown as a fixed FY 2026 net offset | 1 |
| Internal transfer, not a separate spending cut | 1 |
| Duplicate tooltip, excluded | 1 |

The eight photographed items not independently identified as FY 2026 account lines are CISA, pandemic-era refundable tax credits, the Treasury Forfeiture Fund, IRS systems modernization, elective-pay clean-energy credits, the clean-vehicle credit, the semiconductor factory credit, and refundable corporate tax credits. The broader IRS, Treasury, or budget-function categories may include them, but their separate annual amounts could not be isolated from the verified FY 2026 Treasury table. Several other pictured items appear only as a broader line in the app—for example, the full NIST account instead of a separate CHIPS incentive line, the full VA departmental "other" account instead of a standalone PACT Act amount, and whole military department accounts instead of every branch and procurement subtype. These are identified explicitly in the inventory. A broad-account amount is not a verified amount for each of its components and must not be added to them.

The app now includes previously omitted Treasury accounts for student financial assistance, federal direct and family education loans, SBA disaster loans, conservation operations and farm-conservation programs, compensation for ill nuclear weapons workers, retiree health funds, and other lines. Student-loan and disaster-loan account amounts reflect federal credit accounting; they are not the face value of loans or reliable policy-savings estimates. The National Flood Insurance Fund is shown as gross outlays and a fixed offsetting-collections line so that their difference equals Treasury's reported net.

## FY 2026 totals

| Measure | Treasury value |
| --- | ---: |
| Net outlays | $7,395.8 billion |
| Receipts | $5,403.3 billion |
| Deficit | $1,992.5 billion |

These are reported in Treasury's [Table 9](https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v1/accounting/mts/mts_table_9?filter=record_date:eq:2026-09-30). The app contains all 19 reported budget functions, 77 [subfunctions](https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v1/accounting/mts/mts_table_9_outlays_functions_subfunctions?filter=record_date:eq:2026-09-30), and selected [Table 5 account lines](https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v1/accounting/mts/mts_table_5?filter=record_date:eq:2026-09-30&page%5Bsize%5D=1000). The accompanying [account inventory](treasury-line-items.csv) lists the displayed lines, their measurement basis, Treasury paths, and source records.

## Corrections and scope differences

- The FY 2026 premium-credit figure is $126.0 billion after combining Treasury's $149.2 billion HHS record with its negative $23.1 billion Treasury record. FY 2025's combined figure was $129.3 billion. The previous version displayed only the HHS record, so its FY 2026 line overstated the combined net.
- **Correction to the previous audit:** I compared the pictured FEMA *Disaster Relief Fund* with Treasury's broader *Disaster Relief* line without sufficiently distinguishing their scope. The screenshot shows $48.2 billion for FY 2025. Treasury Table 5 reports $51.9 billion for its broader Disaster Relief line; USAspending's FY 2025 [Disaster Relief Fund account](https://www.usaspending.gov/federal_account/070-0702) reports approximately $48.6 billion in gross outlays. The screenshot's fund amount and Treasury's broader line are not directly equivalent, and their remaining difference should not automatically be described as an error. For FY 2026, the app shows the broader Treasury line of $31.8 billion.
- SNAP is $95.4 billion in Treasury's FY 2026 account compared with $106.3 billion in the FY 2025 photograph. The Federal Crop Insurance Corporation Fund is $15.5 billion in FY 2026 versus $13.8 billion in FY 2025.
- The photographed Tennessee Valley Authority amount is a positive FY 2025 figure. Treasury reports FY 2026 TVA **net** outlays of −$1.4 billion, so the app identifies it as a fixed net offset. Gross activity and net outlays are different measures.

## Methods and limits

Treasury Table 5 reports account outlays; Tables 9 and 9A report functions and subfunctions. The table does not supply an official account-to-subfunction crosswalk, so the app's placements are editorial. Some broader Treasury lines span multiple subfunctions. Calculated reconciliation entries can reflect unmatched accounts, transfers, receipts, and classification differences and are fixed in the app. Parent and child rows describe overlapping spending and should never be added together.

I also checked USAspending's FY 2025 account-balance download to identify some pictured account definitions and classifications. Its FY 2026 period-12 federal-account download returned no account rows when checked on November 3, 2026, so it could not supply comparable full-year detail for the eight unmatched breakouts. USAspending explains the [definitions and differences between gross outlays, accounts and obligations](https://www.usaspending.gov/federal-spending-guide).

The app is an arithmetic scenario, not a policy score. Cuts hold net interest, offsets, and unassigned reconciliations fixed and stop positive net lines from falling below zero. They do not determine legal authority, timing, behavior, receipts, the economy, or future interest costs. Existing saved percentages are recalculated and capped if needed when the source data change.
