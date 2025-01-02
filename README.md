# nosql_challenge

For this challenge, data from the UK Food Standards Agency was used to evaluate establishments and ratings data to inform future article content. The Resource folder & data is in a Zip file due to its size, so please download the file for use throughout the analysis. 
Prior to performing the analysis, ensure proper connection to MongoDB by running the command "brew services start mongodb-community@6.0" in the command line terminal - followed by "mongod", and launching Jupyter Notebook.

**Part 1:**
In Part 1, we set dependencies to access MongoDB and create databases through Jupyter Notebook. We start by importing the data provided in the Resources folder ("establishments.json") into our "uk_foods" database, by navigating to the local folder in Terminal and using the command: "mongoimport --type json -d uk_foods -c establishments --drop --jsonArray Resources/establishments.json"

Other dependencies include pymongo and pprint, to support us in using Python to view our MongoDB database in Jupyter Notebook.
Finally, we have to declare our MongoDB port as MongoClient(port=27017)

Once dependencies have been declared, we can set up our references to the database "uk_foods" and collection "establishments", and ensure that all data has been properly uploaded.

**Part 2:**
In Part 2, we begin updating and manipulating the data that was provided for us in the JSON file ("CRUD"). 

We first add a new restaurant that is not included in the initial JSON file, and update missing fields based on existing documents. We also filter for and delete files that are from the Dover Local Authority, as we will not be using those in our analysis.

Finally, we update numerical data types across the total collection, adjusting Latitude and Longitude to contain decimals and ratingvalue to be integers

**Part 3:**
In part 3, we answer questions around different restaurants and businesses, from top rated to low hygiene, to help inform our articles. This analysis uses skills such as filtering, grouping, sorting and limiting that are common functions within SQL/NoSQL databases, and converts answers to our questions into dataframes which can be used for future analysis.
