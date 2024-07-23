# UKRI OA baseline values - exploration using open data sources

Code documented here is used to generate the dataset accompanying the 2024 report  
*"Monitoring and evaluation of UKRI's Open Access Policy: Exploring the use of open data sources to inform baseline values"*  
  
Report:  
Dataset: 

The repository contains SQL scripts used to collect bibliographic metadata of UKRI-funded and UK-affiliated research output (journal articles only) published between 2012 and 2022, as well as data on open access availability, publisher, national and international collaborations, citations, views and downloads, and altmetrics.

This project makes use of Curtin Open Knowledge Initiative (COKI) infrastructure, which is documented on GitHub: https://github.com/The-Academic-Observatory. Here, a number of open data sources (including Crossref, OpenAlex and Unpaywall) are ingested into a Google Big Query environment, which can then be queried via SQL.

The scripts use the following data sources:
OpenAlex (data snapshot 2023-12-23), provided by OurResearch via Amazon AWS (see https://docs.openalex.org/download-all-data/openalex-snapshot), ingested by COKI in Google Big Query
OpenAIRE (data snapshot 2024-01-16), provided by OpenAIRE via Zenodo , ingested by COKI in Google Big QUery
list of identifiers (ROR ID, OpenAlex ID, OpenAIRE ID) of Dutch research performing organisations - included in project dataset


The repository contains 2 SQL scripts:

openalex_works_20231223_rpo_nl_2022.sql
openaire_products_20240116_rpo_nl_2022.sql
These scripts are used to collect record-level data of research putput retrieved from OpenAlex and OpenAIRE, respectively, for all Dutch research performing organizations (RPOs) in scope of the pilot (UNL/NFU, NWO-i, KNAW, VH) for publication year 2022.

The pilot has made use of Curtin Open Knowledge Initiative (COKI) infrastructure, which is documented on GitHub: https://github.com/The-Academic-Observatory. Here, a number of open data sources (including Crossref, OpenAlex and OpenAIRE) are ingested into a Google Big Query environment, which can then be queried via SQL.

In particular,the scripts use the following data sources:

OpenAlex (data snapshot 2023-12-23), provided by OurResearch via Amazon AWS (see https://docs.openalex.org/download-all-data/openalex-snapshot), ingested by COKI in Google Big Query
OpenAIRE (data snapshot 2024-01-16), provided by OpenAIRE via Zenodo , ingested by COKI in Google Big QUery
list of identifiers (ROR ID, OpenAlex ID, OpenAIRE ID) of Dutch research performing organisations - included in project dataset
