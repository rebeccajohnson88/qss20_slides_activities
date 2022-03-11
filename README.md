# QSS20 public repo

This repo has content for the Spring 2021 and Winter 2022 iterations of QSS20: Modern Statistical Computing at Dartmouth College.

## Slides and Activities (Winter '22)

These are jupyter notebook-based activities to practice Python or other concepts, along with accompanying slides:

### Data wrangling, merging, and probabilistic linkage

- [00_pandas_datacleaning_blank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/00_pandas_datacleaning_blank.ipynb)
  - **Data**: DC crime reports in 2020
  - **Concepts covered**:
    - Aggregation using `groupby` and `agg`
    - Lambda functions within aggregation
    - Recoding variables using `np.where`
    - Recoding variables using `np.select`
    - Recoding variables using `map` and dictionary
  - **Slides**: [qss20_w22_unit2_pandas.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/qss20_w22_unit2_pandas.pdf)
  - **Solutions**: [00_pandas_datacleaning_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/00_pandas_datacleaning_solutions.ipynb)
  - **Responses to class questions**: [00_classquestions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/00_classquestions.ipynb)

- [01_example_plotting.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/01_example_plotting.ipynb)
  - **Data**: DC crime reports in 2020
  - **Concepts covered**:
    - Plotting using the `plotnine` wrapper for R's `ggplot2`
    - Types of plots covered: line graph; bar chart; facetted line; line grouped/colored by attribute


- [02_loopsfunctions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/02_loopsfunctions.ipynb)
  - **Data**: DC crime reports in 2020
  - **Concepts covered**:
    - `for loop` to find matches within a broader pool of data
    - user-defined function to find matches within a broader pool of data
    - using list comprehension to apply a function iteratively over list elements 
   -  **Slides**: [03_qss20_w22_unit3_loopvfunction.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/03_qss20_w22_unit3_loopvfunction.pdf)
   -  **Solutions**: [02_loopsfunctions_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/02_loopsfunctions_solutions.ipynb)


- [03_merging_exact_blank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/03_merging_exact_blank.ipynb)
  - **Data**: San Diego business tax certificate data; Census NAICS code data
  - **Concepts covered**:
    - Data cleaning such as extraneous rows/columns
    - Recasting join cols to allow join (e.g., converting `int` to character)
    - `pd.merge` and different types of exact joins using join keys
    - Post-merge diagnostics
   - **Slides**: [05_qss20_w22_unit5_mergingexact.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/05_qss20_w22_unit5_mergingexact.pdf)
   - **Solutions**: [03_merging_exact_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/03_merging_exact_solutions.ipynb)


- [04_basicregex_blank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/04_basicregex_blank.ipynb)
   - **Data**: Food Research Action Center (FRAC) data on district and school's election of community eligibility provision (CEP) for Free or Reduced Price Lunch (FRPL)
   - **Concepts covered**: 
     - Pattern construction using `re` module
     - `re.sub` for replacement
     - `re.findall` 
     - `re.match` and how to work with match objects using `.group()`
     - Throughout, review of list comprehension 
    - **Slides**: [06_qss20_w22_unit6_regex.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/06_qss20_w22_unit6_regex.pdf)
    - **Example code**: [05_merging_fuzzy_codeexample.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/05_merging_fuzzy_codeexample.ipynb)
  - **Solutions for activity**: [https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/04_basicregex_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/04_basicregex_solutions.ipynb)

- [05_merging_fuzzy_activity_blank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/05_merging_fuzzy_activity_blank.ipynb)
  - **Data**: public SD business tax certificate data; public PPP loan data on large loans
  - **Concepts covered**:
    - Regex for string cleaning
    - String distance/similarity measures: edit distance, jaccard, jarowinkler
    - `recordlinkage` package and steps in fuzzy/probabilistic matching
  - **Slides**: [07_qss20_w22_unit7_fuzzymatching.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/07_qss20_w22_unit7_fuzzymatching.pdf)
  - **Example code**: [05_merging_fuzzy_codeexample.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/05_merging_fuzzy_codeexample.ipynb)
  - **Solutions for activity**: [05_merging_fuzzy_activity_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/05_merging_fuzzy_activity_solutions.ipynb)

### Text as data

- [06_textasdata_partI_textmining_examplecode.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/06_textasdata_partI_textmining_examplecode.ipynb)

  - **Data**: simplified data from airbnb NYC listings. Stored in `public_data/airbnb_text.zip`
  - **Concepts covered**:
    - Scoring based on dictionary of words
    - Part of speech tagging using `nltk`
    - Named entity tagging using `spaCy`
    - Sentiment analysis using `VADER`
   - **Slides**: [08_qss20_w22_unit8_textasdata.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/08_qss20_w22_unit8_textasdata.pdf)


- [06_textasdata_partII_topicmodeling.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/06_textasdata_partII_topicmodeling.ipynb)
  - **Data**: simplified airbnb listings
  - **Concepts covered**:
    - Using `sklearn` to create a unigram document-term matrix
    - LDA topic modeling using `gensim`
    - Visualizing topics 
    - Obtaining top words per topic using `gensim`
    - Obtaining document-level topic probabilities using `gensim`
  - **Slides**: [08_qss20_w22_unit8_textasdata.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/08_qss20_w22_unit8_textasdata.pdf)
  - **Solutions**: [06_textasdata_partII_topicmodeling_solution.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/06_textasdata_partII_topicmodeling_solution.ipynb)

### Intro to SQL




### APIs, intro to supervised machine learning, static and interactive geo-visualization 

- [07_apispart1_examplecode_blank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/07_apispart1_examplecode_blank.ipynb)

  - **APIs**: NAEP data explorer; Yelp API
  - **Concepts covered**:
    - Writing a query
    - Using `requests` to execute a query and return a response
    - Processing a response
    - Yelp Fusion API business search and reviews endpoints
  - **Slides**: [09_qss20_w22_unit9_APIs.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/09_qss20_w22_unit9_APIs.pdf)

- [08_apis_twitter_essentialendpoint_examplecode.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/08_apis_twitter_essentialendpoint_examplecode.ipynb)
  - **API**: `tweepy` wrapper for Twitter API
  - **Concepts covered**:
    - Authenticating
    - searching for tweets based on hashtag using `search_recent_tweets` method
    - searching for attributes of users tweeting
    - extracting followers of an account using `get_users_followers` method
    - extracting tweets from a specific user using `get_users_tweets` method
   - **Slides**: [09_qss20_w22_unit9_APIs.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/09_qss20_w22_unit9_APIs.pdf)
   - **Blank activity**: [08_apis_twitter_activity_blank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/08_apis_twitter_activity_blank.ipynb)
   - **Activity solutions**: [08_apis_twitter_activity_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/08_apis_twitter_activity_solutions.ipynb)

- [09_binaryclassification_activity_blank.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/09_binaryclassification_activity_blank.ipynb)
  - **Data**: Unstructured yelp reviews with labeled sentiment scores 
  - **Concepts covered**:
    - Tree-based methods versus regularization
    - Preprocessing to prepare for a model
    - Train-test split
    - (Basic) hyperparameter tuning
    - Model evaluation
   - **Slides**: [10_qss20_w22_unit10_introML.pdf](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/slides/w22_slides/10_qss20_w22_unit10_introML.pdf)
   - **Activity solutions**: [09_binaryclassification_activity_solutions.ipynb](https://github.com/rebeccajohnson88/qss20_slides_activities/blob/main/activities/w22_activities/solutions/09_binaryclassification_activity_solutions.ipynb)


