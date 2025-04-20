# Data Summary Report: Single Social Events in Taiwan (2005–2020)

## Data Description

The dataset, titled "11-112 內政部單身聯誼活動報名人數資料集," records participation in single social events organized by Taiwan's Ministry of the Interior from 2016 to 2020 (corresponding to Republic of China years 105 to 112). It includes 106 events across multiple Taiwanese counties, capturing variables such as the event year, series number, duration, location, total applicants, and gender distribution (male and female applicants). The dataset, presumed to originate from government statistics or event registration systems, is designed to analyze participation trends, gender ratios, and regional preferences in social engagement activities. Detailed metadata is provided in the codebook (`codebook.md`), which confirms the absence of missing values across all variables and specifies data types: integer for `Year`, `Series`, `Applicant_count`, `Applicant_m`, and `Applicant_f`, and character for `Schedule` and `Location`.

## Data Summary

### Variable Overview

The dataset comprises 106 observations with seven variables, covering events from 2016 to 2020. The `Year` variable, representing the event year, ranges from 105 to 112 (2016–2020), with a mean of 108.35 and a standard deviation of 2.18, indicating a balanced distribution across the period (see `single-variable-summary.json`). Numeric variables related to participation—`Applicant_count`, `Applicant_m`, and `Applicant_f`—provide insights into event scale and gender dynamics. According to the codebook, `Applicant_count` averages approximately 871 participants per event, with a median of 868, ranging from 497 to 1,194 (SD ≈ 180). Male applicants (`Applicant_m`) dominate, averaging ~742 (median: 741, range: 429–1,033, SD ≈ 150), while female applicants (`Applicant_f`) average ~129 (median: 126, range: 46–190, SD ≈ 30). The codebook confirms that `Applicant_count` equals the sum of `Applicant_m` and `Applicant_f`, ensuring data consistency. The `Schedule` variable indicates event duration (e.g., "1日" for one day, "2日" for two days, or "半日" for half-day), and `Location` specifies the hosting county (e.g., 臺中, 苗栗), with multiple counties represented.

### Yearly Participation Trends

Analysis of yearly participation trends, detailed in `yearly_participation_trends.json`, reveals fluctuations in event popularity. Total applicants grew from 5,081 in 2016 (12 events, average 423 per event) to a peak of 11,980 in 2020 (12 events, average 998 per event). Notable growth occurred between 2016 and 2017 (65.91% increase) and between 2019 and 2020 (43.30% increase), though declines were observed in 2018 (–17.33%) and 2019 (–13.73%). The number of events per year varied, with a high of 18 in 2019 and a low of 9 in 2019, suggesting varying organizational intensity. The average applicants per event peaked in 2020 at 998, reflecting increased interest or capacity. No missing values were reported for `Year`, `Series`, or `Applicant_count`, aligning with the codebook’s claims.

### Gender Dynamics by Year and Location

The gender composition of participants, analyzed in `sex_ratio_year_location.json`, highlights a consistent male predominance across years and locations. Male proportions ranged from 0.55 (Taipei, 2017) to 0.88 (Kaohsiung, 2020), averaging around 0.79 across the dataset, while female proportions ranged from 0.12 to 0.45. For example, in 2020, Yunlin reported a male proportion of 0.87 and a female proportion of 0.13, while Taipei in 2017 had a more balanced ratio (0.55 male, 0.45 female). Locations like Kaohsiung and Yunlin consistently showed higher male participation, whereas Taipei occasionally exhibited greater gender balance. Total applicants per year-location combination varied widely, from 185 (Pingtung, 2018) to 2,400 (Taichung, 2020). No missing values were found for `Year`, `Location`, `Applicant_count`, `Applicant_m`, or `Applicant_f`, reinforcing data reliability.

### Participation by Location and Schedule

The distribution of applicants by location and event duration, summarized in `applicant_count_location_schedule.json`, reveals regional and format preferences. Taichung hosted the most applicants for one-day events (6,283 across 7 events, average 898 per event) and half-day events (3,741 across 6 events, average 624 per event). Nantou led in two-day events with 7,028 applicants across 8 events (average 878 per event). Half-day events, less common, had lower averages (e.g., 187 in Yilan), suggesting shorter formats attracted fewer participants. Locations like Yilan and Kaohsiung hosted diverse event formats, with Yilan’s one-day events averaging 728 applicants and Kaohsiung’s one-day events averaging 614. The dataset includes unique cases like "苗栗/新竹" (617 applicants, one event), indicating joint-hosted events. No missing values were reported for `Location`, `Schedule`, or `Applicant_count`.

### Data Integrity and Limitations

The absence of missing values across all variables, as verified in the JSON summaries and codebook, ensures robust data integrity for analysis. However, the `Year` variable in the summaries (105–112) extends beyond the codebook’s stated range (111–112), suggesting either a documentation error or an expanded dataset. This discrepancy warrants caution when interpreting trends before 2016. Additionally, the `Schedule` variable includes "半日" (half-day), not mentioned in the codebook’s examples, indicating potential undocumented formats. These inconsistencies highlight the need for further validation of the dataset’s temporal and categorical scope.

## References

- Codebook: `codebook.md`
- Single Variable Summary: `single-variable-summary.json`
- Yearly Participation Trends: `yearly_participation_trends.json`
- Sex Ratio by Year and Location: `sex_ratio_year_location.json`
- Applicant Count by Location and Schedule: `applicant_count_location_schedule.json`
