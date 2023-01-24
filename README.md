## Web Scraping. Sentimental analysis of textual data.
Web Scraping was performed based on the CNN site by using diverse libriries and packages such as: Selenium (Webdriver, Webdriver Select, WebDriver By), Pandas, BeautifulSoup, Requests. Sentimental Analysis was accomplished based on following tools: Natural Language Toolkit, Pandas, REGEX, SEABORN, VADERSENTIMENT, WORDCLOUD, Topic Modeling with GENSIM. 

Let's dive into the process with more amount of details.

Web scraping is the process of collecting and parsing raw data from the Web.
There are several steps that should be considered before performing the Web Scrapping.

## Scrutinizing the Website
To reach a web server we send an HTTP request (query) to the server of the page we want to scrape. The server responds by sending the HTML content of the web page. Since we use Python for our requests, we need a third-party HTTP library, and we will use Requests.
## Decipher the Information in URLs
The base URL represents the path to the search functionality of the website. We have parameters that are in the format of a key-value pair.
Query parameters are defined set of parameters attached to the end of a url. They are expansions of the URL that are used to aid figure out specific content or actions based on the data being passed.
Origin: The beginning of the query parameters is denoted by a question mark (?). 
Content: The pieces of information of a query parameter are enclosed in key-value pairs, keys and values are joined together by an equal sign (key=value).
Divider: Every URL might have multiple query parameters, which are separated from each other by an ampersand (&) in between each. These can be created by any variation of object types or lengths such as String, Arrays and Numbers.

Some websites are built deliberetely to forbid users from scraping their data with a web page. In this case we can use Selenium libriry.
## Selenium - The link for installation - https://selenium-python.readthedocs.io/installation.html 
Selenium is an open-source tool that automates web browsers. It provides a single interface that lets us write test scripts in programming languages.
1. Selenium WebDriver - is a web framework that permits you to execute cross-browser tests. This tool is used for automating web-based application testing to verify that it performs expectedly.Selenium WebDriver allows you to choose a programming language to create test scripts
2. Selenium.webdriver Select - The 'Select' class in Selenium WebDriver is used for selecting and deselecting option in a dropdown. The objects of Select type can be initialized by passing the dropdown webElement as parameter to its constructor.
3. Selenium.webdriver By - WebDriver will respect the context in the specified in the selector. Describes a mechanism for locating an element on the page. 

## Pandas -
This library is for keeping the records of our  scrapped  in the form of tables (CSV)
## BeautifulSoup - The link for installation - https://beautiful-soup-4.readthedocs.io/en/latest/
This library is for searching through the HTML  in  code  an organized and  simple way.
## Requests - 
This library is for sending HTTP requests and  the HTML data from the target web
pages to obtain the information we are looking for.


## ANALYSIS PART
 This part might depend on depth of desired analysis. I would like to descibe several important steps.
 
 ## Step 1: Tokenise
Given a character sequence and a defined document unit, tokenization is the task of chopping it up into pieces, called tokens , perhaps at the same time throwing away certain characters, such as punctuation.
## Step 2: Normilise
There are always variations of the same word in the dataset. For instance: words might distinquish in terms of their case: ‘and’ and ‘And’ or their suffix: ‘give’, ‘given’ and ‘giving’. This is where normalisation comes in to standardise.
To normalise a word is to transform it into its root form.
Lemmatisation is one of ways to normalise text (We use WordNetLemmatizer from nltk to lemmatise our tokens).
## Step 3: Remove Stop Words
Stop words are common words which provide little to no value to the meaning of the text (We can use nltk’s stopwords corpus).
## Step 4. Count Vectorise
Count vectorise is to convert a collection of text documents to a matrix of token counts (We can use sklearn's CountVectorizer). CountVectorizer converts text into a matrix of 'm' by 'n' where 'm' is the amount of text records, 'n' is the amount of unique tokens through all records and the elements of the matrix refer to the totally of a token for a given record.
## Step 5. Transform to TF-IDF representation
tf-idf stands for term frequency inverse document frequency. (We can use sklearn's TfidfTransformer).
When transforming to tf-idf representation, we convert the counts to weighted frequency where we acquire more significance to less frequent words and less importance to more frequent words by using a weight named inverse document frequency.






