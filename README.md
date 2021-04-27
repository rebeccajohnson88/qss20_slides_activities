# QSS20 public repo

This repo has content for the Spring 2021 iteration of QSS20: Modern Statistical Computing.

## Activities

These are jupyter notebook-based activities to practice Python or other concepts:

- [00_latex_output_examples_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/00_latex_output_examples_solutions.ipynb)
  - **Data**: DC crime reports in 2020
  - **Concepts covered**:
    - Writing a pandas dataframe or table to use in LaTeX
    - Row filtering
    - Saving figures
    - Iterating and saving figures with informative names


- [01_pandas_datacleaning_examples.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/01_pandas_datacleaning_examples.ipynb) 
  - **Data**: sample of Chicago health/hygiene inspection results
  - **Concepts covered**:
    - Cleaning column names (eg subbing out spaces and changing to lowercase)
    - Checking datatypes within a pandas dataframe and recasting
    - Creating new true/false variables using `np.where`
    - Creating new categorical variables that involve recoding an existing categorical variable using `map` and a dictionary

- [02_more_pandas_datacleaning.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/02_more_pandas_datacleaning.ipynb)
  - **Data**: DC crime reports in 2020
  - **Concepts covered**:
    - Aggregation using `groupby` and `agg`
    - Lambda functions within aggregation
    - Recoding variables using `np.where`
    - Recoding variables using `np.select`
    - Recoding variables using `map` and dictionary
    - Loop to find matches within a broader pool of data
    - Function to find matches within a broader pool of data

- [03_merging_session1.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/03_merging_session1.ipynb)
  - **Data**: San Diego business tax certificate data; Census NAICS code data
  - **Concepts covered**:
    - Data cleaning such as extraneous rows/columns
    - Recasting join cols to allow join (e.g., converting `int` to character)
    - `pd.merge` and different types of exact joins using join keys
    - Post-merge diagnostics
    
- [04_basicregex_formerging.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/04_basicregex_formerging.ipynb)
   - **Data**: Food Research Action Center (FRAC) data on district and school's election of community eligibility provision (CEP) for Free or Reduced Price Lunch (FRPL)
   - **Concepts covered**: 
     - Pattern construction using `re` module
     - `re.sub` for replacement
     - `re.findall` 
     - `re.match` and how to work with match objects using `.group()`
     - Throughout, review of list comprehension 

- [https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/05_merging_session2_blank.ipynb](05_merging_session2_blank.ipynb) 
  - **Data**: public SD business tax certificate data; public PPP loan data on large loans
  - **Concepts covered**:
    - Regex for string cleaning
    - String distance/similarity measures: edit distance, jaccard, jarowinkler
    - `recordlinkage` package and steps in fuzzy/probabilistic matching

