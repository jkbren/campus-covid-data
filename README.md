# campus-covid-data
Institutes of higher education (IHE) can play a large role in mitigating the spread of COVD-19, and this is especially true as we await large scale vaccination. There is not a national repository for recording the amount of testing and case counts for individuals affiliated with universities, and as such, many administrators and local policymakers are not equipped with the most up-to-date data to inform their decision-making. This dataset is designed to be a stopgap to this problem---a holdover until nationwide or statewide policies are enacted to more systematically collect this data.

In creating this dataset, we rely on IHEs' "COVID Dashboards", which vary in their sophistication and informativeness, but more often than not, they report the number of student/faculty/staff cases affiliated with the IHE. If a college or university has put in place a regular testing protocol, they often report the daily or weekly number of tests that have been conducted as well. These data help us piece together an ever-incomplete picture of the impact / role that IHEs have on the broader community and taken together should inform decision-making at the local and institutional levels (i.e. whether to allow students back for in-person classes, hybrid classes, online only, etc.).


## Data and findings
This dataset was built by heavily relying on a python to Google sheets interface. I learned about this
tool [here](https://www.twilio.com/blog/2017/02/an-easy-way-to-read-and-write-to-a-google-spreadsheet-in-python.html). To recreate the dataset entirely, you will need
to go through the steps to enable API acccess [here](https://gspread.readthedocs.io/en/latest/oauth2.html#enable-api-access).

State-by-state Google sheets (with separate tabs for each school) and a [Reference](https://docs.google.com/spreadsheets/d/1GMu4fful47nUIFlwl293cPqPGG0XX3uIl0zno-bTJbY/edit?usp=sharing) Google sheet can be found in this drive [here](https://drive.google.com/drive/folders/19MLhkjQl3qhlGSmwD2MVbqOE_7ZaID0j?usp=sharing).

- - - -

<p align="center">
<img src="maps_so_far_2020-01-04.png" alt="county_level" width="95%"/>
</p>

**<p align="center">Current status of the Campus Covid dataset.**

## Limitations
There are tons. First---because this dataset was formed to address the lack of nationwide (or in most cases, statewide) standards that compel institutes of higher education to report their testing and case count data---there is very likely human error in the collection or reporting of data. Data for many IHEs were collected through a crowdsourced effort (survey link [here](https://neu.co1.qualtrics.com/jfe/form/SV_8dE7jqvikKSlgYR)). Second, many schools rely on self-reported data, which can also present an opportunity for human error. Third, as time goes on, IHEs may update their own counts of testing and cases, which might produce inconsistencies with the data used here.


## Notebooks
1. [Automate the creation of individual google sheets](https://github.com/campus-covid-data/code/create_google_sheets.ipynb)
2. [Pull data from Google Sheets](https://github.com/campus-covid-data/code/retrieve_data_from_google_sheets.ipynb)

## Other datasets
1. nyt_cases_as_of_12-11.csv - New York Times case counts (https://www.nytimes.com/interactive/2020/us/covid-college-cases-tracker.html)
2. party_school_rankings.tsv - party school ranking data scaped from niche.com (https://www.niche.com/colleges/search/top-party-schools/)
3. ipeds_data.csv - IPEDS school data (https://nces.ed.gov/ipeds/use-the-data)


## Installation and Usage

In order to use this code, first clone/download the repository. 
Below is a simple example usage. Please feel free to reach 
out if you find any bugs, have any questions, or if for some reason
the code does not run. 

### Requirements  <a name="requirements"/>

This code is written in [Python 3.x](https://www.python.org) and uses 
the following packages:

* [Pandas](https://pandas.pydata.org/)
* [Numpy](http://numpy.scipy.org/)
* [geopandas](https://geopandas.org/) (for replicating the map figures)
* [gspread](https://gspread.readthedocs.io/en/latest/) 


## Citation   <a name="citation"/>

If you use findings from this work and/or some of the aggregated data provided in your own research, please cite the following:

Bibtex: 
```text
@article{klein2020distancing,
  title = {The emergence and persistence of collective physical distancing during the COVID-19 outbreak},
  author = {Brennan Klein and Timothy LaRock and Stefan McCabe and Leo Torres and Lisa Friedland and and Maciej Kos and Filippo Privitera and and Brennan Lake and Moritz U. G. Kraemer and John S. and Brownstein and David Lazer and Tina Eliassi-Rad and Samuel V. Scarpino and Matteo Chinazzi and Alessandro Vespignani},
  journal = {arXiv},
  year = {2020},
  url = {\url{https://www.mobs-lab.org/uploads/6/7/8/7/6787877/assessing_mobility_changes_in_the_united_states_during_the_covid_19_outbreak.pdf}}
}
```

## See also:

* Chinazzi, M., Davis, J.T., Ajelli, M., Gioannini, C., Litvinova, M., Merler, S., Pastore y Piontti, A., Mu, K., Rossi, L., Sun, K., Viboud, C., Xiong, X., Yu, H., Halloran, M.E., Longini Jr., I.M., & Vespignani, A. (2020). The effect of travel restrictions on the spread of the 2019 novel coronavirus (COVID-19) outbreak. *Science*. doi: [10.1126/science.aba9757](https://doi.org/10.1126/science.aba9757)
