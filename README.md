# 📊 Scopus Data Retrieval & Processing Pipeline

This repository contains a Python-based workflow for retrieving, cleaning, and structuring publication metadata from the **Elsevier Scopus API**. The main objective is to build a curated dataset of journal articles for downstream analysis. The code was developed for the below project, which we ask you to cite in case you use our code in your research:

Brooks, C., Farkas, M. (2026): Chasing Ratings, Losing Impact: Journal Selection Behaviour in Business and Management Studies. Research Policy, forthcoming.

---

## 🚀 Overview

The notebook performs the following key steps:

1. **Retrieve journal metadata**
   - Uses the Elsevier API via the [pybliometrics](https://pybliometrics.readthedocs.io/en/stable/) package (version 3.5.2)
   - Iterates over a list of journals and publication years provided by the user. Journals can be identified by Scopus source ID, eISSN, ISSN or title.

2. **Download article-level data**
   - Collects metadata such as:
     - Article titles
     - Authors
     - Publication details
     - Identifiers (e.g., EID)

3. **Clean and filter data**
   - Removes duplicates
   - Performs consistency checks
   - Filters false-positive journal matches
   - Handles missing values
   - Applies restrictions (e.g., number of coauthors)

4. **Prepare final dataset**
   - Outputs a structured datasets that can be linked at the desired level using author, affiliation and article identifiers provided by Scopus (article level or affiliation level or article-author-affiliation level). See the example_data folder.
