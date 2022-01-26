
## Activities in Spring 2021

These are jupyter notebook-based activities to practice Python or other concepts:

### Data wrangling using pandas

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

### Merging: exact merging and fuzzy/probabilistic record linkage

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

- [05_merging_session2_codeexample.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/05_merging_session2_codeexample.ipynb)
  - **Data**: public SD business tax certificate data; public PPP loan data on large loans
  - **Concepts covered**:
    - Regex for string cleaning
    - String distance/similarity measures: edit distance, jaccard, jarowinkler
    - `recordlinkage` package and steps in fuzzy/probabilistic matching
  - **Activity**: [05_merging_session2_activityblank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/05_merging_session2_activityblank.ipynb)
  - **Solutions for activity**: [05_merging_session2_activitysolutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/05_merging_session2_activitysolutions.ipynb)


### Intro to text as data

- [06_textasdata_partI_textmining_examplecode.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/06_textasdata_partI_textmining_examplecode.ipynb)

  - **Data**: simplified data from airbnb NYC listings. Stored in `public_data/airbnb_text.zip`
  - **Concepts covered**:
    - Scoring based on dictionary of words
    - Part of speech tagging using `nltk`
    - Named entity tagging using `spaCy`
    - Sentiment analysis using `VADER`

- [06_textasdata_partII_topicmodeling_examplecode.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/06_textasdata_partII_topicmodeling_examplecode.ipynb)
  - **Data**: simplified airbnb listings
  - **Concepts covered**:
    - Using `sklearn` to create a unigram document-term matrix
    - LDA topic modeling using `gensim`
    - Visualizing topics 
    - Obtaining top words per topic using `gensim`
    - Obtaining document-level topic probabilities using `gensim`
  - **Solutions code**: [06_textasdata_partII_topicmodeling_solution.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/06_textasdata_partII_topicmodeling_solution.ipynb)


### APIs/scraping

- [07_apis_examplecode_blank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/07_apis_examplecode_blank.ipynb)

  - **APIs**: NAEP data explorer; Yelp API
  - **Concepts covered**:
    - Writing a query
    - Using `requests` to execute a query and return a response
    - Processing a response
    - Yelp Fusion API business search and reviews endpoints
  - **Solutions code**: [07_apis_examplecode_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/07_apis_examplecode_solutions.ipynb)

- [07_apis_examplecode_twitter.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/07_apis_examplecode_twitter.ipynb)
  - **API**: `tweepy` wrapper for Twitter API
  - **Concepts covered**:
    - Authenticating
    - Using `Cursor` class
    - searching for tweets based on hashtag using `search` method
    - extracting followers of an account using `followers` method
    - extracting tweets from a specific user using `user_timeline` method

- [09_intro_scraping.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/09_intro_scraping.ipynb)
  - **Data**: DC due process hearings for special education; DOJ press releases
  - **Concepts covered**:
    - Parsing content using `BeautifulSoup`
    - Extract links using `href` attribute
    - Extracting other attributes

### SQL

- [08_SQL_examplecode.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/08_SQL_examplecode.ipynb)
  - **Data**: case initiations and diversions from Cook County SAO
  - **Concepts covered**:
    - Establishing connection to MySQL database
    - Row and column filtering using `select` and `where`
    - Subqueries
    - Aggregation using `group by`
 - **Activity**: [08_SQL_activity.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/08_SQL_activity.ipynb)
 


