BBGsymbols
================

[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)

<style> body {text-align: justify} </style>

<!-- README.md is generated from README.Rmd. Please edit that file -->

## BBGsymbols

BBGsymbols provides a collection of Bloomberg related helper datasets
conveniently packaged for consumption in R. Install from
[github](https://github.com/bautheac/BBGsymbols/) with:
`devtools::install_github("bautheac/BBGsymbols")`.

### Fields

The ‘fields’ dataset gathers Bloomberg query fields that have been
carefully selected over time through experience, saving the user long
hours of browsing the depths of Bloomberg for the fitting fields. It
provides popular historical and contemporaneous data fields that are
likely to provide the necessary information and beyond for any rigorous
research or more applied work in finance and financial economics.
Financial instruments covered at the time of writing include ‘equity’,
referring to any equity like security, ‘fund’ encompassing any money
managing entity and ‘futures’ covering the futures markets. The author
welcomes pull requests that could help expanding the current coverage.

Dataset excerpt:

    #>   instrument      book                type subtype section subsection
    #> 1     equity key stats adjusted highlights    <NA>    <NA>       <NA>
    #> 2     equity key stats adjusted highlights    <NA>    <NA>       <NA>
    #> 3     equity key stats adjusted highlights    <NA>    <NA>       <NA>
    #> 4     equity key stats adjusted highlights    <NA>    <NA>       <NA>
    #> 5     equity key stats adjusted highlights    <NA>    <NA>       <NA>
    #> 6     equity key stats adjusted highlights    <NA>    <NA>       <NA>
    #>                                                                           name
    #> 1                                                        market capitalization
    #> 2                                                             enterprise value
    #> 3                                                             adjusted revenue
    #> 4                                                        adjusted gross profit
    #> 5 adjusted earnings before interest, tax, depreciation & amortization (EBITDA)
    #> 6                                                          adjusted net income
    #>      id                symbol
    #> 1 RR250 HISTORICAL_MARKET_CAP
    #> 2 RR472      ENTERPRISE_VALUE
    #> 3 IS010        SALES_REV_TURN
    #> 4 RR861          GROSS_PROFIT
    #> 5 RR009                EBITDA
    #> 6 RR530       EARN_FOR_COMMON
    #>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  description
    #> 1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                Total market value of all of a company's outstanding shares at period-end date stated in the company's fundamental currency (DS215, EQY_FUND_CRNCY).   The period-end date is the most recent for which full fundamental data has been collected.  Calculated as:\n\nShares Outstanding * Last Closing Price\n\nWhere:\nShares Outstanding is BS081, BS_SH_OUT\nLast Closing Price is PR005, PX_LAST\n\nShares Outstanding excludes treasury shares (BS091, BS_NUM_OF_TSY_SH)\n\nFor multiple share companies, market cap is the sum of market capitalization of all classes of common stock at period end date.\n\nFor current market cap, please refer to RR902, CUR_MKT_CAP \n\nFigure is reported in million; the Scaling Format Override (DY339,SCALING_FORMAT) can be used to change the display units for the field.
    #> 2                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   INDUSTRIALS, FINANCIALS, INSURANCE, UTILITIES, & REITS\n\nMeasure of a company's theoretical takeover price. Calculated as:  \n\nMarket Capitalization + EV Components\n\nWhere:\nHistorical Market Capitalization is RR250, HISTORICAL_MARKET_CAP\nEV Components is RR968, CUR_EV_COMPONENT \n\nMarket Capitalization calculation excludes Number of Treasury Shares (BS091, BS_NUM_OF_TSY_SH).\n\nFor limited partnerships, enterprise value is the value of the limited partner, and does not include any value assigned to the general partner.\n\nThe field returns the value in the fundamental Currency Override (DS215, EQY_FUND_CRNCY)\n\nFor current enterprise value, in the fundamental currency, use Current Enterprise Value (RR905, CURR_ENTP_VAL).\n\nFor current enterprise value in another currency, use Currency Adjusted Current Enterprise Value (RR937, CRNCY_ADJ_CURR_EV).\n\nFigure is reported in million; the Scaling Format Override (DY339, SCALING_FORMAT) can be used to change the display units for the field.\n\nThe related fields referenced herein may not be available in all enterprise products.
    #> 3                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    INDUSTRIALS\nAmount of sales generated by a company after the deduction of sales returns, allowances, discounts, and sales based taxes.  Includes revenues from financial subsidiaries in industrial companies if the consolidation includes those subsidiaries throughout the report.  Includes subsidies from federal or local government in certain industries (i.e. transportation or utilities).  Excludes turnover from joint ventures and/or associates.  Excludes inter-company revenue.  Excludes revenues from discontinued operations.  Figure is reported in millions; the Scaling Format Override (DY339, SCALING_FORMAT) can be used to change the display units for the field.  Users can set their preference to return 'GAAP' (Generally Accepted Accounting Principles) or 'ADJUSTED' data through Fundamental Analysis Defaults.  The field FA Adjusted Financials Override (DT094, FA_ADJUSTED) can be used to return Adjusted (excluding abnormal items) data ('Y') or GAAP data ('N').\n\nBANKS & FINANCIALS\nGross revenue from any operating activity.  Total revenue is defined as the sum of total interest income, investment income, trading profit (loss), commissions and fees earned and other operating income.  Excludes revenue from discontinued operations.  Revenue may be negative due to large trading account losses.\n\nINSURANCES\nAll revenues from any operating activities.  The sum of net premiums earned, realized investment gain (loss), investment income, real estate operations, and other income.\n\nUTILITIES\nIncludes revenues from electric, gas, water and other operating revenue.  All revenues from any operating activity (principal activities).  Gross revenues less adjustments.  Excludes internal or inter-company revenues, except for privately held companies (utility subsidiaries).\n\nREITS\nRevenues from real estate operating activities. Total of rental income, real estate sales (for Real Estate Operating companies), management and advisory fees, mortgage and note income and other operating income.  Excludes equity in income from unconsolidated entities.  Excludes gain/(loss) on sale of rental properties.
    #> 4                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   INDUSTRIALS & UTILITIES\nCompany's revenues less its cost of goods sold.  Calculated as:\n\nRevenues - Cost of Goods Sold\n\nWhere:\n   Revenue is IS010, SALE_REV_TURN\n   Cost of Good Sold is IS021, IS_COGS_TO_FE_AND_PP_AND_G\n\nNote:  Please reference Gross Profit Adjusted (IM130, IS_ADJUSTED_GROSS_PROFIT) for the adjusted value that excludes the impact of abnormal items.
    #> 5 Indicator of a company's financial performance which is essentially net income with interest, taxes, depreciation, and amortization added back to it, and can be used to analyze and compare profitability between companies and industries because it eliminates the effects of financing and accounting decisions. Figure is reported in millions; the Scaling Format Override (DY339, SCALING_FORMAT) can be used to change the display units for the field.\n\nINDUSTRIAL & UTILITIES \nCalculated as:\n\nOperating Income  + Depreciation & Amortization\n\nWhere:\nOperating Income or Losses is IS033, IS_OPER_INC \nDepreciation & Amortization IS CF011, CF_DEPR_AMORT <P>FINANCIALS\nCalculated as:\n\nOperating Income  + Depreciation & Amortization + Interest Expense\n\nWhere: \nOperating Income or Losses is IS033, IS_OPER_INC\nDepreciation & Amortization IS CF011, CF_DEPR_AMORT\nInterest Expense is IS022, IS_INT_EXPENSES\n\nThis ratio may not be meaningful for companies in the financial format where interest is a major component of revenue.\n\nREITS\nCalculated as:\n\nOperating Income  + Depreciation & Amortization + Interest Expense\n\nWhere:\nOperating Income or Losses is IS033, IS_OPER_INC\nDepreciation & Amortization IS CF011, CF_DEPR_AMORT\nInterest Expense is IS034, IS_INT_EXPENSE\n\nMUNICIPAL REVENUE \nCalculated as:\n\nNormalized Profit + Depreciation Expenses+ Amortization Expense+ Interest Expense Operating + Interest Expense\n\nWhere: \nNormalized Profit is F0222, TOTAL_NORMALIZED_PROFIT \nDepreciation Expense is IS070, IS_DEPR_EXP or CF011, CF_DEPR_AMORT\nAmortization is IM011, IS_AMORTIZATION_EXPENSE\nInterest Expense Operating is IS674, IS_INTEREST_EXPENSES_OPERATING\nInterest Expense is IS034, IS_INT_EXPENSE\n\nINDEX:\nThis field returns the aggregate of all equity contributions. Each equity contribution is calculated as:\n\n(EBITDA value for each equity * respective number of shares in the index * FX Rate) / (Index Divisor * Coverage Factor)\n\nWhere:\nEBITDA is (RR856,TRAIL_12M_EBITDA_PER_SHARE) for annual periodicity and (RR555, EBITDA_PER_SH) for interim periodicities.\nNumber of shares of a security in the index can be obtained on MEMB\nFX Rate is applied to securities that have a different fundamental currency EQY_FUND_CRNCY from the index's Index Divisor is IN018, INDX_DIVISOR\n\nCoverage factor is defined as: 1 - (unused market cap / index market cap)\nWhere:\nUnused market cap is the sum of securities' market cap that do not have an equity contribution to the index value\nSecurity market cap is last price(PR005,PX_LAST)*number of shares outstanding(IS060,IS_AVG_NUM_SH_FOR_EPS)\nIndex market cap is the sum of securities' market cap.
    #> 6                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    Net Income Available To Common Shareholders. Figure is scaled in millions. The Scaling Format Override (DY339, SCALING_FORMAT) can be used to change the display units for the field. Calculated as:\n\nNet Income  - Total Cash Preferred Dividend  - Other Adjustments\n\nWhere:\n   Net Income is  IS050, NET_INCOME\n   Total Cash Preferred Dividends is IS051, IS_TOT_CASH_PFD_DVD\n   Other Adjustments is  IS168, OTHER_ADJUSTMENTS\n\nPlease reference Net Income to Common Adjusted (IS810, IS_NI_AVAILABLE_TO_COMMON_ADJ) for the adjusted value that excludes the impact of abnormal items.

### Months

The ‘months’ dataset details the symbols used to refer to calendar
months in Bloomberg and financial markets in general. It is particularly
useful when working with financial derivative instruments such as
futures contracts.

Dataset excerpt:

    #>        name symbol
    #> 1:  January      F
    #> 2: February      G
    #> 3:    March      H
    #> 4:    April      J
    #> 5:      May      K
    #> 6:     June      M

### Rolls

The ‘rolls’ dataset details the symbols used to refer to the various
roll types and adjustments available in Bloomberg when working with
futures term structure contracts. These symbols can be used to construct
bespoke tickers that allow the user to query Bloomberg for futures term
structure data with the desired roll characteristics.

Dataset excerpt:

    #>    roll symbol                     name
    #> 1: type      A       With active future
    #> 2: type      B        Bloomberg default
    #> 3: type      D        At first delivery
    #> 4: type      F       Fixed day of month
    #> 5: type      N Relative to first notice
    #> 6: type      O     At option expiration

### CFTC tickers

The ‘tickers\_cftc’ dataset gathers Bloomberg position data tickers for
a number of futures series. These tickers allow direct retrieval from
Bloomberg via pullit of corresponding position data as reported by the
US Commodity Futures Trading Commission (CFTC) in a collection of weekly
market reports including the ‘legacy’, ‘disaggregated’, ‘supplemental’
and ‘traders in financial futures’ (TFF) reports. See `?tickers_cftc`
for details. Dataset excerpt:

    #>                    name  asset class active contract ticker  MIC format
    #> 1: LIBOR rate - 1-month fixed income             EMA Comdty XCME legacy
    #> 2: LIBOR rate - 1-month fixed income             EMA Comdty XCME legacy
    #> 3: LIBOR rate - 1-month fixed income             EMA Comdty XCME legacy
    #> 4: LIBOR rate - 1-month fixed income             EMA Comdty XCME legacy
    #> 5: LIBOR rate - 1-month fixed income             EMA Comdty XCME legacy
    #> 6: LIBOR rate - 1-month fixed income             EMA Comdty XCME legacy
    #>      underlying    unit    participant  position         ticker
    #> 1: futures only traders non-commercial      long IMM11TNL Index
    #> 2: futures only traders non-commercial     short IMM11TNS Index
    #> 3: futures only traders non-commercial spreading IMM11TNP Index
    #> 4: futures only traders          total      long IMM11TTL Index
    #> 5: futures only traders          total     short IMM11TTS Index
    #> 6: futures only traders          total     total IMM11TTO Index

### Futures tickers

The ‘tickers\_futures’ dataset gathers futures active contract Bloomberg
tickers as well as a collection of qualitative information for several
popular futures series including commodity, currency, financial and
index futures with underlyings from various asset classes.

Dataset excerpt:

    #>        ticker                                         name asset class
    #> 1 BSDA Comdty Carbon allowance - California - vintage 2016     climate
    #> 2  V6A Comdty                                       Butter   commodity
    #> 3 CHEA Comdty                                       Cheese   commodity
    #> 4  DAA Comdty                               Milk-class III   commodity
    #> 5  KVA Comdty                                Milk-Class IV   commodity
    #> 6  LEA Comdty                             Milk-non fat dry   commodity
    #>          sector subsector currency  MIC term structure length contract size
    #> 1          <NA>      <NA>      USD IFED                    50          1000
    #> 2 agriculturals     dairy      USD XCME                    24         20000
    #> 3 agriculturals     dairy      USD XCME                    25         20000
    #> 4 agriculturals     dairy      USD XCME                    24        200000
    #> 5 agriculturals     dairy      USD XCME                    23        200000
    #> 6 agriculturals     dairy      USD XCME                    24         44000
    #>   trading unit point value tick size tick value         FIGI
    #> 1   allowances        1000     0.010         10 BBG00H5NQBM9
    #> 2       pounds         200     0.025          5 BBG00DP4KKM4
    #> 3       pounds       20000     0.001         20 BBG00DP4KKP1
    #> 4       pounds        2000     0.010         20 BBG00DP4KK71
    #> 5       pounds        2000     0.010         20 BBG00DP4KKJ8
    #> 6       pounds         440     0.025         11 BBG00DP4KKB6
    #>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             description
    #> 1                                                                                                                                                                                                                                                                                                               ICE US: California Carbon Allowance Vintage 2016 Future\nDescription: Physically delivered greenhouse gas emissions allowances where each is an allowance issued by the California Air Resources Board or a linked program (California Carbon Allowance) representing one metric ton of CO2 equivalent under California Assembly Bill 32 "California Global Warming Solutions Act of 2006" and its associated regulations, rules and amendments, all together known as the "California Cap and Trade Program". \n Launch Date: October 15, 2012 \n Exchange Symbol: CAO
    #> 2                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           Valued at 20,000 times the USDA monthly weighted  average price per pound in the U.S. for Grade AA  butter.
    #> 3                                                                                                                                                                       CME Cash Settled Cheese Futures\nQuote Unit: US Dollars per pound. Although CME contract specifications states 'Pricing Unit U.S. cents per pound ', BBG has confirmed with CME group the quotes displayed/provided to Bloomberg are U.S. Dollars per pound.\n\nLaunch Date: June 20, 2010\nExchange code:CSC\n\nFinal Settlement Procedure: Cash settled based upon the USDA monthly weighted average price in the U.S. for cheese. The reported USDA monthly weighted average price for cheese uses both 40 pound cheddar block and 500 pound barrel prices.\n\nContract Specifications: http://www.cmegroup.com/trading/agricultural/dairy/cheese_contract_specifications.html\nSource of info: cmegroup.com
    #> 4 Description: Class III Milk Futures - Commodity Specifications: 2,000 times the USDA Class III Price for fluid milk. Class III Milk Futures represent milk used in the manufacturing of Cheddar Cheese. \n**Effective July 6, 2015 and pending all relevant CFTC regulatory review periods, CME will close Open-Outcry (PIT) for all Futures except for S&P 500 Futures {SPA Index DES<GO>}. On the Bloomberg, PIT ticker tail will remain for historical Open-Outcry reference and will thereafter represent CME Clearport Pricing Data.**\nSource of Info: cmegroup.com \n **DEAA is no longer supported, you will be able to see the same data in DAA ELEC <COMDTY>.**\nExchange ticker: DA\nSource of info: cmegroup.com\n\nFor CME & CBOT Block Thresholds and Reporting Times, please refer to:\nhttp://www.cmegroup.com/market-regulation/rule-filings/2017/12/17-420_APPC.pdf
    #> 5                                                                                                                                                                                                                                                                                                                                                             Class IV Milk is used to manufacture butter and   non-fat dry milk.\n **Effective July 6, 2015 and pending all relevant CFTC regulatory review periods, CME will close Open-Outcry (PIT) for all Futures except for S&P 500 Futures {SPA Index DES<GO>}. On the Bloomberg, PIT ticker tail will remain for historical Open-Outcry reference and will thereafter represent CME Clearport Pricing Data.**\nExchange Ticker: DK\n Contracts Listed: All Calender Months\n Settlement Procedure: Cash Settlement.\n CME Group
    #> 6                                                                                                                                                                                                                                                                                                                                     Description: Nonfat Dry Milk - Contract consists of product  that is no more than 180 days old in a range of   42,000 to 45,000 pounds in 25-kilogram bags.\n**Effective July 6, 2015 and pending all relevant CFTC regulatory review periods, CME will close Open-Outcry (PIT) for all Futures except for S&P 500 Futures {SPA Index DES<GO>}. On the Bloomberg, PIT ticker tail will remain for historical Open-Outcry reference and will thereafter represent CME Clearport Pricing Data.**\nExchange ticker: NF\nSource of info: cmegroup.com

### finRes

Although BBGsymbols is self-contained with consumption value on its own,
it belongs to [finRes](https://bautheac.github.io/finRes/) where it
plays an important role in providing support to
[pullit](https://github.io/bautheac/pullit/) and
[storethat](https://github.io/bautheac/storethat/) for collecting,
storing and retrieving financial data as well as facilitating their
integrity.
