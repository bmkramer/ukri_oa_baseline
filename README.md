# UKRI OA baseline values - exploration using open data sources

Code documented here is used to generate the dataset accompanying the 2024 report  
*"Monitoring and evaluation of UKRI's Open Access Policy: Exploring the use of open data sources to inform baseline values"*  
  
Report:  
Dataset: 

The repository contains SQL scripts used to collect bibliographic metadata of UKRI-funded and UK-affiliated research output (journal articles only) published between 2012 and 2022, as well as data on open access availability, publisher, national and international collaborations, citations, views and downloads, and altmetrics. 

This project makes use of **Curtin Open Knowledge Initiative (COKI)** infrastructure, which is documented on GitHub: https://github.com/The-Academic-Observatory. Here, a number of open data sources (including Crossref, OpenAlex and Unpaywall) are ingested into a **Google Big Query** environment, which can then be queried via SQL. Additional data sources can be ingested manually, and similarly queried via SQL.

## Data sources  
The scripts use the following data sources included in the COKI Google Big Query environment:

- **Crossref Metadata Plus** (data snapshot 2023-10-31), provided by Crossref (see https://www.crossref.org/services/metadata-retrieval/metadata-plus/)
- **OpenAlex** (data snapshot 2023-10-18), provided by OurResearch via Amazon AWS (see https://docs.openalex.org/download-all-data/openalex-snapshot)
- **Unpaywall** (data snapshot 2023-11-27), provided by OurResearch (see https://unpaywall.org/products/data-feed)
- **Crossref Event Data** (data snapshot 2023-04-01), provided by Crossref (NB The Crossref Event Data API is scheduled to be [replaced](https://community.crossref.org/t/relationships-endpoint-update-and-event-data-api-sunsetting/4214) by the Relationships API in the near future) 

In addition, a number of supplementary open data sources were manually added to the Google Big Query environment for this project. 
These are included in this repository in the folder [supplementary_sources](/supplementary_sources)

- **Gateway to Research** - data on UKRI-funded publications for publication years 2012-2022 (13 csv files), downloaded from Gateway to Research web UI (https://gtr.ukri.org/) between 2023-11-05 and 2023-11-13
- **Crossref member data** - Crossref member IDs and publisher names, created by querying Crossref member route API (https://api.crossref.org/swagger-ui/index.html#/Members) on 2024-01-23 (1 csv file)
- **IRUS UK data** - Usage metrics collected through IRUS_UK web UI (https://irus.jisc.ac.uk/r5/report/item/irus_ir_master/) on 2023-04-03, for all items with type 'article' in repositories included in IRUS UK which saw at least one type of usage (views or downloads) in the period Jan-Dec 2023 (1 csv file, zipped)





The repository contains 2 SQL scripts:

openalex_works_20231223_rpo_nl_2022.sql
openaire_products_20240116_rpo_nl_2022.sql
These scripts are used to collect record-level data of research putput retrieved from OpenAlex and OpenAIRE, respectively, for all Dutch research performing organizations (RPOs) in scope of the pilot (UNL/NFU, NWO-i, KNAW, VH) for publication year 2022.

The pilot has made use of Curtin Open Knowledge Initiative (COKI) infrastructure, which is documented on GitHub: https://github.com/The-Academic-Observatory. Here, a number of open data sources (including Crossref, OpenAlex and OpenAIRE) are ingested into a Google Big Query environment, which can then be queried via SQL.

In particular,the scripts use the following data sources:

OpenAlex (data snapshot 2023-12-23), provided by OurResearch via Amazon AWS (see https://docs.openalex.org/download-all-data/openalex-snapshot), ingested by COKI in Google Big Query
OpenAIRE (data snapshot 2024-01-16), provided by OpenAIRE via Zenodo , ingested by COKI in Google Big QUery
list of identifiers (ROR ID, OpenAlex ID, OpenAIRE ID) of Dutch research performing organisations - included in project dataset
