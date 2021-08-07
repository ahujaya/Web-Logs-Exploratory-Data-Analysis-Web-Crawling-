# Web-Logs-Exploratory-Data-Analysis-Web-Crawling-
***Part I Data Manipulation — Tulip Hotel Web Log Data***

Here is the hypothetical background:
Hotel TULIP (a hypothetical organisation) is a five star hotel that locates in Australia. It is a very special hotel with an equally special purpose: Not only does it embody all the creative energy and spirit of TULIP-Lab, it’s a “learning environment” on which the tourism and hospitality students are trained for future hoteliers. In the past two decades, the Web server of Hotel TULIP has logged all the web traffic to the hotel website, and stored large amount of data related to the use of various web pages. The hotel’s CIO, Dr Bear Guts (not Bill Gates!), believes that those log files are great resources to help their Information Technology Division improve their potential customers’ online experience, and help their Market Promotion Division to identify potential customers and their behaviour patterns. Hence, Hotel TULIP would like to outsource the web usage mining task to Group-SIT742 (a hypothetical data analytics group with up to 3 data analysers) to analyse web log files
and discover user accessing patterns of different web pages. The Web server is using Microsoft Internet Information Service (IIS), and the Web log format can be found at: https://msdn.microsoft.com/en-us/library/ms525807(v=vs.90).aspx You are employed within Hotel TULIP working in the Information Technology Division. Your manager, Dr Beer Guts (also not Bill Gates!), has asked you to prepare a set of documents for Group-SIT742 so that they can have an initial understanding of the data to be analysed.

- Task Description
This task requires you to construct a data dictionary and develop a data exploration report for the provided Hotel TULIP Web log dataset. Without exploration or further analysis, ‘raw’ Web log data hardly reveals any insightful information. In this part, you are required to complete the Python code snippets to generate suitable numeric and visual description in the Hotel TULIP Web log dataset based on the detailed requirements in SIT742Task1.ipynb, and develop the report SIT742Task1Report.pdf to summarise the descriptive statistics information. The detailed requirements can also be found in the notebook SIT742Task1.ipynb, here we summarise them as follows:

1. ETL
- Data Loading:
Complete the Python code snippets in SIT742Task1.ipynb as required in notebook, and complete the data
dictionary and report.
Code Load (may need unzip first) the Hotel TULIP Web log data HTWebLog_p1.zip into dataframe df_ht,
and check how many files are loaded. Then check data statistics and general information by printing
its top 5 rows.
- Data Dictionary: Fill the data dictionary based on the Python code results.
For a data scientist or business analyst, after obtaining the dataset, the first crucial task is to obtain
a good understanding of the data to be analysed. This includes: examining the data attributes (or
equivalently, data fields), seeing what they look like, what is the data type for each field, and from this
information, determining suitable numerical/visual descriptions.

2. Data Cleaning (2 marks)
Complete the Python code snippets in SIT742Task1.ipynb as required in notebook, and complete the data
dictionary and report.
Code • Check which columns have NAs,
• For each of those columns, display how many records with NA values
• Remove all records with any NAs.
SIT742Task1Report Add proper results for:
• the number NAs for each column.
• the number of rows before removing NAs.
• the number of rows after removing NAs.
2 Descriptive Statistics
2.1 Traffic Analysis (4 marks)
Analyse the web traffic statistics;
Code • Discover on the traffics by analysing hourly requests.
• Plot into Bar Chart.
• Filter the hourly requests by removing any below 490,000 and above 400,000. (hourly_request_amount
>= 400000 & hourly_request_amount <= 490000)
Report • Please add a figure of Hourly Requests Bar Chart from your Notebook, and elaborate the
findings from the figure.
• Please add a table of filter result (hourly_request_amount >= 400000 & hourly_request_amount
<= 490000)
2.2 Server Analysis (4 marks)
Analyse the server status statistics;
Code Discover on the server status using ‘sc-status’ from DataFrame, then plot it into Pie Chart.
Report • How many types of status reported?
• Figure ‘Server Status’ in Pie Chart.
Page 3 of 5
SIT742 (Modern Data Science)
Full Marks: 25
Assessment Task 01
2021 Trimester 1, Due: 8:00pm AEST, 17/04/2021
2.3 Geographic Analysis (4 marks)
Analyse the server Geographic information statistics;
Code • Select all requests at 01 Jan 2007 from 20:00:00 pm to 20:59:59 pm.
• Discover the geographic information by analysing requests from country and city level.
• Plot countries and cities of all requests in two pie charts.
• List top 3 of both with the request numbers.
Report • How many requests raised in the period of time?
• How many countries and cities are involved?
• Figure ‘Request by Country’ and ‘Request by City’ in pie charts.
• List Top 3 countries and cites with the request numbers.

***Part II - Data Manipulation — Web Crawling***
Google Scholar is a web service that indexes the metadata of research articles on many scientists. Majority
of computer scientists choose to use Google scholar to track their publications and research development.
Therefore, the web crawling on Google Scholar can provide the citation information on all professors with a
public Google Scholar profile.

Task Description
In 2021, to better introduce all the emeritus professors, professors and associate professors in the school of
IT, Deakin university wants to collect all the citation information on them. You are required to implement
a web crawler, design and complete the code in the notebook and make sure that the web crawling code
meets the requirements. You are free to use any Python package for Web crawling.
3 Professor list generation
You will need to import the suitable (or your chosen)web crawling library and use the corresponding library
to crawl the School of IT staff list page: https://www.deakin.edu.au/information-technology/
staff-listing.
3.1 Import and install your web crawling library
You could use selenium by doing the pip install selenium, download the webdriver for chromedriver and
define your webdriver for crawling. But you are free to use any other library.
3.2 Crawl and Generate the list
The code must contain the necessary web crawling steps and necessary data save steps. The results of the
code running will generate the Professor-list.csv.

4 Professor Citation Information generation
4.1 Professor citation information generation 
You will need to use the generated Professor-list.csv to identify each professor’s google scholar profile
page in google scholar platform, and then to crawl the citation information from each google scholar profile.
You will need to design your code by using loops and condition statement (as some of the professors did
not have google scholar profile) to complete this requirement. The results of code running will generate the
Professor-citation-information.csv.
4.2 Identify the professor with the most citations
You are required to do the sort and print by using pandas function to find out the professor with the most
citations (please remove those without a public google scholar page).
4.3 Identify the associate professor with the most i10-index since 2016 
You are required to do the filer, sort and print by using pandas function to find out the associate professor
with the most i10-index since 2016 (please remove those without a public google scholar page).
4.4 Identify those with the citations-since2016 > 2500 
You are required to do the conditional filter and print to find out those (professors, associate professors)
with the citations-since2016 > 2500 (please remove those without a public google scholar page).
