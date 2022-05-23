# Data on COVID-19 (coronavirus) by _Our World in Data_


### 🗂️ Download our complete COVID-19 dataset : [CSV](https://covid.ourworldindata.org/data/owid-covid-data.csv) | [XLSX](https://covid.ourworldindata.org/data/owid-covid-data.xlsx) | [JSON](https://covid.ourworldindata.org/data/owid-covid-data.json)

Our complete COVID-19 dataset is a collection of the COVID-19 data maintained by [_Our World in Data_](https://ourworldindata.org/coronavirus). We will update it daily throughout the duration of the COVID-19 pandemic (more information on our updating process and schedule [here](https://docs.owid.io/projects/covid/en/latest/data-pipeline.html#overview)). It includes the following data:

| Metrics                     | Source                                                    | Updated | Countries |
|-----------------------------|-----------------------------------------------------------|---------|-----------|
| Vaccinations                | Official data collated by the Our World in Data team      | Daily   | 218       |
| Tests & positivity          | Official data collated by the Our World in Data team      | Weekly  | 188       |
| Hospital & ICU              | Official data collated by the Our World in Data team      | Daily   | 47        |
| Confirmed cases             | JHU CSSE COVID-19 Data                                    | Daily   | 217        |
| Confirmed deaths            | JHU CSSE COVID-19 Data                                    | Daily   | 217       |
| Reproduction rate           | Arroyo-Marioli F, Bullano F, Kucinskas S, Rondón-Moreno C | Daily   | 192        |
| Policy responses            | Oxford COVID-19 Government Response Tracker               | Daily   | 187        |
| Other variables of interest | International organizations (UN, World Bank, OECD, IHME…) | Fixed   | 241       |

A [specific section of this repository](https://github.com/owid/covid-19-data/tree/master/public/data/vaccinations) is also dedicated to **vaccinations**, with a lighter dataset containing only vaccination data.


## The data you find here and our data sources

- **Confirmed cases and deaths:** our data comes from the [COVID-19 Data Repository by the Center for Systems Science and Engineering (CSSE) at Johns Hopkins University](https://github.com/CSSEGISandData/COVID-19) (JHU). We discuss how and when JHU collects and publishes this data [here](https://ourworldindata.org/coronavirus-source-data). The cases & deaths dataset is updated daily.
  - Note: confirmed cases and deaths are collected by Johns Hopkins University by date of report, rathen than date of test/death. Therefore the number they report on a given day does not necessarily represent the actual number on that date, because of the long reporting chain that exists between a new case/death and its inclusion in statistics. This also means that time series can show sudden changes (negative or positive) when a country corrects historical data, because it had previously under- or overestimated the number of cases/deaths.
- **Hospitalizations and intensive care unit (ICU) admissions:** our data is collected from official sources and collated by Our World in Data. The complete list of country-by-country sources is available [here](https://github.com/owid/covid-19-data/blob/master/public/data/hospitalizations/locations.csv).
- **Testing for COVID-19:** this data is collected by the _Our World in Data_ team from official reports; you can find further details in our post on COVID-19 testing, including our [checklist of questions to understand testing data](https://ourworldindata.org/coronavirus-testing#our-checklist-for-covid-19-testing-data), information on [geographical and temporal coverage](https://ourworldindata.org/coronavirus-testing#which-countries-do-we-have-testing-data-for), and [detailed country-by-country source information](https://ourworldindata.org/coronavirus-testing#source-information-country-by-country). The testing dataset is updated around twice a week.
- **Vaccinations against COVID-19:** this data is collected by the _Our World in Data_ team from official reports.
- **Other variables:** this data is collected from a variety of sources (United Nations, World Bank, Global Burden of Disease, Blavatnik School of Government, etc.). More information is available in [our codebook](https://github.com/owid/covid-19-data/tree/master/public/data/owid-covid-codebook.csv).


## The variables explanation will be used accroding to Data_ COVID-19 dataset

**Our complete COVID-19 dataset is available in [CSV](https://covid.ourworldindata.org/data/owid-covid-data.csv), [XLSX](https://covid.ourworldindata.org/data/owid-covid-data.xlsx), and [JSON](https://covid.ourworldindata.org/data/owid-covid-data.json) formats, and includes all of our historical data on the pandemic up to the date of publication.**


The variables represent all of our main data related to confirmed cases, deaths, hospitalizations, and testing, as well as other variables of potential interest.

### Confirmed cases
| Variable                         | Description                                                                                                                                                                                            |
|:---------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|                          
| `new_cases`                      | New confirmed cases of COVID-19. Counts can include probable cases, where reported. In rare 

### Confirmed deaths
| Variable                          | Description                                                                                                                                                                                               |
|:----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `new_deaths`                      | New deaths attributed to COVID-19. Counts can include probable deaths, where reported. In rare cases where our source reports a negative daily change due to a data correction, we set this metric to NA. |
| `new_deaths_per_million`          | New deaths attributed to COVID-19 per 1,000,000 people. Counts can include probable deaths, where reported.                                                                                                                                                                          |

#### Notes:
* Due to varying protocols and challenges in the attribution of the cause of death, the number of confirmed deaths may not accurately represent the true number of deaths caused by COVID-19.


### Policy responses
| Variable           | Description                                                                                                                                                                                                         |
|:-------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stringency_index` | Government Response Stringency Index: composite measure based on 9 response indicators including school closures, workplace closures, and travel bans, rescaled to a value from 0 to 100 (100 = strictest response) |

### Reproduction rate
| Variable            | Description                                                                                                                                   |
|:--------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| `reproduction_rate` | Real-time estimate of the effective reproduction rate (R) of COVID-19. See https://github.com/crondonm/TrackingR/tree/main/Estimates-Database |



### Vaccinations
| Variable                                     | Description                                                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `people_fully_vaccinated`                    | Total number of people who received all doses prescribed by the initial vaccination protocol               |                                                                                                                                                                                                                                                                                                         
| `people_fully_vaccinated_per_hundred`        | Total number of people who received all doses prescribed by the initial vaccination protocol per 100 people in the total population                                                                                                                                                                                                               |                                                                                  |

### Others
| Variable                     | Description                                                                                                                                                                                                                                |
|:-----------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iso_code`                   | ISO 3166-1 alpha-3 – three-letter country codes                                                                                                                                                                                            |
| `continent`                  | Continent of the geographical location                                                                                                                                                                                                     |
| `location`                   | Geographical location                                                                                                                                                                                                                      |
| `date`                       | Date of observation                                                                                                                                                                                                                        |

A [full codebook](https://github.com/owid/covid-19-data/tree/master/public/data/owid-covid-codebook.csv) is made available, with a description and source for each variable in the dataset.


## Additional files and information

If you are interested in the individual files that make up the complete dataset, or more detailed information, other files can be found in the subfolders:

- [`latest`](https://github.com/owid/covid-19-data/tree/master/public/data/latest): shortened version of our complete dataset with only the latest value for each location and metric (within a limit of 2 weeks in the past). This file is available in CSV, XLSX, and JSON formats.
- [`jhu`](https://github.com/owid/covid-19-data/tree/master/public/data/jhu): data from the COVID-19 Data Repository by the Center for Systems Science and Engineering (CSSE) at Johns Hopkins University, related to confirmed cases and deaths. We also automatically export JHU's subnational case and death data for a few countries (Australia, Canada, China, Denmark, France, Netherlands, New Zealand, United Kingdom, United States) to a reshaped and compressed file ([`subnational_cases_deaths.zip`](https://covid.ourworldindata.org/data/jhu/subnational_cases_deaths.zip)).
- [`testing`](https://github.com/owid/covid-19-data/tree/master/public/data/testing): data from various official sources, related to COVID-19 tests performed in each country. This folder contains two files with more detailed information:
  - [`covid-testing-all-observations.csv`](https://github.com/owid/covid-19-data/blob/master/public/data/testing/covid-testing-all-observations.csv) includes, for each historical observation, the source of the individual data point, and sometimes notes on data collection;
  - [`covid-testing-latest-data-source-details.csv`](https://github.com/owid/covid-19-data/blob/master/public/data/testing/covid-testing-latest-data-source-details.csv) includes, for each country in our testing dataset, the latest figures and a detailed description of how the country’s data is collected;
- [`excess_mortality`](https://github.com/owid/covid-19-data/tree/master/public/data/excess_mortality): data on excess mortality during the pandemic, sourced from [the Human Mortality Database](https://www.mortality.org/) and [the UK Office for National Statistics](https://www.ons.gov.uk/peoplepopulationandcommunity/birthsdeathsandmarriages/deaths/articles/comparisonsofallcausemortalitybetweeneuropeancountriesandregions/januarytojune2020);
- [`vaccinations`](https://github.com/owid/covid-19-data/tree/master/public/data/vaccinations): data from various official sources, related to COVID-19 vaccinations in each country;
- [`archived`](https://github.com/owid/covid-19-data/tree/master/public/data/archived): data from other providers that we have stopped using and updating;
- [`internal`](https://github.com/owid/covid-19-data/tree/master/public/data/internal): data extracts intended for internal use at _Our World in Data_. They may change or be deleted without notice so we discourage using them.


## Stable URLs

The `/public` path of this repository is hosted at `https://covid.ourworldindata.org/`. For example, you can access the
CSV for the complete dataset at `https://covid.ourworldindata.org/data/owid-covid-data.csv` or the CSV with latest data
at `https://covid.ourworldindata.org/data/latest/owid-covid-latest.csv`.

We have the goal to keep all stable URLs working, even when we have to restructure this repository. If you need regular updates, please consider using the `covid.ourworldindata.org` URLs rather than pointing to GitHub.


## License

All visualizations, data, and code produced by _Our World in Data_ are completely open access under the [Creative Commons BY license](https://creativecommons.org/licenses/by/4.0/). You have the permission to use, distribute, and reproduce these in any medium, provided the source and authors are credited.

In the case of our vaccination dataset, please give the following citation:
> Mathieu, E., Ritchie, H., Ortiz-Ospina, E. _et al._ A global database of COVID-19 vaccinations. _Nat Hum Behav_ (2021). [https://doi.org/10.1038/s41562-021-01122-8](https://doi.org/10.1038/s41562-021-01122-8)

In the case of our testing dataset, please give the following citation:
> Hasell, J., Mathieu, E., Beltekian, D. _et al._ A cross-country database of COVID-19 testing. _Sci Data_ **7**, 345 (2020). [https://doi.org/10.1038/s41597-020-00688-8](https://doi.org/10.1038/s41597-020-00688-8)

The data produced by third parties and made available by _Our World in Data_ is subject to the license terms from the original third-party authors. We will always indicate the original source of the data in our database, and you should always check the license of any such third-party data before use.


## Authors

This data has been collected, aggregated, and documented by Cameron Appel, Diana Beltekian, Daniel Gavrilov, Charlie Giattino, Joe Hasell, Bobbie Macdonald, Edouard Mathieu, Esteban Ortiz-Ospina, Hannah Ritchie, Lucas Rodés-Guirao, Max Roser.

The mission of _Our World in Data_ is to make data and research on the world's largest problems understandable and accessible. [Read more about our mission](https://ourworldindata.org/about).
 
