## Firm Attention to Macroeconomic News
Sample: 1994-2020\
Frequency: annual\
Coverage: publicly traded firms in the U.S.

### Data files
1. attn_firmlevel.csv
2. attn_firmlevel.dta

### Contents
Firm-level attention data from [Firm Inattention and the Efficacy of Monetary Policy: A Text-Based Approach](https://wentingsong.com/files/song_stern_inattention.pdf) by Wenting Song and Samuel Stern.
  
  > This paper provides empirical evidence of the importance of firm attention to macroeconomic dynamics. We construct a text-based measure of attention to macroeconomic news and document that attention is **polarized across firms** and **countercyclical**. Differences in attention lead to **asymmetric responses to monetary policy**: expansionary monetary shocks raise market values of attentive firms more than those of inattentive firms, and contractionary shocks lower values of attentive firms by less. Attention also mitigates the effects of macroeconomic uncertainty on firm performance. In a quantitative rational inattention model that is calibrated with this new text-based measure, inattention drives monetary non-neutrality. As average attention varies over the business cycle, so does the efficacy of monetary policy.   

### Variable descriptions
- For details on variable construction, refer to the main text of the [paper](https://wentingsong.com/files/song_stern_inattention.pdf).
- The main attention variables are `d_tot_<macro_topic>` (e.g., `d_tot_general`): firm attention to macroeconomic news measured based on the full texts of its annual report.
- Data is provided in csv and dta formats, each containing the following variables:

  | Variable name                   | Description                                                         |
  | ------------------------------- | ------------------------------------------------------------------- |
  | `accession_number`              | Accession number                                                    |
  | `cik`                           | SEC's CIK number                                                    |
  | `name`                          | Firm name                                                           |
  | `filing_type`                   | SEC filing type                                                     |
  | `sic`                           | SIC industry code                                                   |
  | `filingdate`                    | Filing date                                                         |
  | `conformdate`                   | Conform date                                                        |
  | `fyear`                         | Fiscal year                                                         |
  | `d_<sec_section>_<macro_topic>` | **Prevalence attention measure** for <macro_topic> in <sec_section> |
  | `s_<sec_section>_<macro_topic>` | **Intensity attention measure** for <macro_topic> in <sec_section>  |
  | `len_total_raw`                 | Word count                                                          |
  | `len_total`                     | Word count excl. stop words                                         |
  | `len_unique_raw`                | Unique words                                                        |
  | `len_unique`                    | Unique words excl. stop words                                       |
  | `jaccard`                       | Jaccard score                                                       |

- Details for `<macro_topic>`  
  | Variable name | Description                             |
  | ------------- | --------------------------------------- |
  | `general`     | Attention to general macroeconomic news |
  | `gdp`         | Attention to output news                |
  | `employment`  | Attention to employment news            |
  | `consumption` | Attention to consumptions news          |
  | `inflation`   | Attention to inflation news             |
  | `investment`  | Attention to investment news            |
  | `housing`     | Attention to housing news               |
  | `oil`         | Attention to oil news                   |
  | `forex`       | Attention to foreign exchange news      |

- Details for `<sec_section>`
  | Variable name | Description                                                   |
  | ------------- | ------------------------------------------------------------- |
  | `tot`         | Attention in the entire annual report (baseline measure)      |
  | `ops`         | Attention in operations-related sections (Items 1 and 7)      |
  | `rsk`         | Attention in risk-related sections (Items 1A and 7A)          |
  | `data`        | Attention in data-disclosure sections (Items 6, 8, 9, and 15) |
