# OSF Dataset UNIBE Dashboard
![Display_unibe](https://img.shields.io/badge/Application%20Type-Streamlit-informational?style=flat&logo=streamlit&logoColor=white&color=red)

The OSF Data Dashboard facilitates data collection from the Open Science Framework (OSF) API for the University of Bern. Prior to querying the API, the application conducts web scraping of the official University of Bern website [https://www.unibe.ch/facultiesinstitutes/index_eng.html](https://www.unibe.ch/facultiesinstitutes/index_eng.html) to gather information about the university's faculties and institutes.

## Data Collection Process

The data collection process for "Check OSF Data" follows these steps:

1. Collection of all universities in the first phase.
2. Retrieval of the "About Us" section for each university.
3. Extraction of individuals listed on each "About Us" page, iterating through associated links.
4. Generation of a comprehensive CSV containing names and other relevant details.
5. Use of the CSV to obtain ORCID IDs.
6. Utilization of both name and ORCID ID to collect data from OSF.
7. Subsequent processing of the CSV to create the final dataset.

## Key Features

- Engaging Streamlit app showcasing publication records from OSF.
- Visually appealing interface for ease of data exploration.
- Step-by-step data collection and processing illustrated through visuals.
- Discover more details in the `osf` directory.

## Usage

Use the deployed live application: [https://osfdasboard.streamlit.app/](https://osfdasboard.streamlit.app/)

To run the application manually:

```bash
pip install -r requirements.txt
streamlit run ui.py
```

## File Structure

- `extract_from_osf.py`: Script for extracting data from OSF API.
- `filter_out.py`: Script for filtering out relevant data.
- `orcidxofs.csv`: CSV file containing ORCID IDs and names.
- `orcidxofs_2.csv`: Intermediate CSV file for data processing.
- `out.csv`: Output CSV file containing the final dataset.
- `requirements.txt`: List of required Python packages.
- `temp.csv`: Temporary CSV file used during data collection.
- `ui.py`: Streamlit app code for the dashboard.
- `unique_institute.py`: Script for handling unique institutes.
- `unique_institutes.csv`: CSV file containing information about unique institutes.
- `userinfo.csv`: CSV file containing user information.



## Contribution

Contributions to this project are welcome. If you encounter any issues, have suggestions, or want to add new features, please feel free to create a pull request or raise an issue in the repository.

Thank you for using the UNIBE Project Dashboard! If you have any questions or feedback, feel free to reach out to us.
