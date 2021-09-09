# Public Dataset for "Estimates of COVID-19 Cases and Deaths Among Nursing Home Residents Not Reported in Federal Data" 

This dataset contains estimates of total COVID-19 cases and deaths among nursing homes residents as of May 24, 2020 in a sample of 20 states that required nursing homes to report cases and deaths starting from the beginning of the pandemic.

The data are at the facility level. CMS provider numbers (provnum), facility names (provname), and state (stabbrev) are provided. 

The main derived variables are
* cases_adj_524: inferred true count of resident cases as of May 24, 2020; calculated as the maximum of the state and federal (NHSN) reports of cases among nursing home residents
* deaths_adj_524: inferred true count of resident deaths as of May 24, 2020; maximum of the state and federal (NHSN) reports of deaths among nursing home residents
* cases_underreport: number of cases that were missed by the federal (NHSN) report (cases_adj_524 - fed_cases_res_524)
* deaths_underreport: number of deaths that were missed by the federal (NHSN) report (deaths_adj_524 - deaths_cases_res_524) 

The raw source variables for these variables are:
* fed_cases_res_524: The NHSN report of cases 
* fed_deaths_res_524: The NHSN report of deaths
* state_cases_res_524: The state department of health report of cases
* state_deaths_res_524: The state department of health report of deaths

For more information on the state data, see eMethods1 in the manuscript.
To obtain total cases and/or deaths for another date, one can add the underreport counts to the NHSN total at the date of interest. The NHSN report used was from year-end 2020. Occasionally, this data is revised, so numbers may not exactly match current reports. 
