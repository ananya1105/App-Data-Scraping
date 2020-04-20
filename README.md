# App-Data-Scraping
In the present scenario apps are the prefered choice over websites, this is the reason why many developers opt for 
Objective: This model aims at extracting metadata by hitting the google play-store API. This process has been accomplished using the playscrapper library.
Usage: The data extracted using playscrpper library can be used to learn about the popularity of various apps, attributes of apps commonly used in an area.
Anyone opting to proceed with this project should have basic understanding of python-programming and jupyternotebook. 
Dataset: The dataset used in the project is the data of customers. It has 7 fields:
1. apps	: List of urls of the apps installed in the device
2. contacts : contact information of the customers
3. crn : Unique Customer Identification Number 
4. deviceInfo	: Basic information about the device
5. location : Location of the device
6. sms : Sms received
7. time : Timestamp 
You can also find the dataset in this repository named as app-data.xlsx
There are total 15721 records.  
Libraries Used: pandas, numpy, ast, tqdm, play_scraper.
Methodology Used: 
1. One more column has been added to this dataset which is app_count that is the number of app url found in each device.
2. App list in the string format is converted into list format using the ast library.
3. A dataframe has been created(app_info) which contains fields like deviceInfo and apps. We have mapped app-url corresponding to each device.
4. Then we have created a unique list of apps-url.
5. Them a function get_details has been designed to fetch the meta-data corresponding to each app-url.
6. Meta-Data that we have fetched are stored in the columns name, rating and category as the columns to the app_info dataset. 
7. Final csv file obtained is named as app_info.csv. 
This output file can be used in numerous projects where we need app-metadata. Running playscraper everytime is not convenient because it takes pretty much time so it is better to have a csv file at handy. 

