# P3_Geospatial_Data
![portada](https://www.acquia.com/sites/acquia.com/files/styles/desktop_hero_image_1x/public/images/2017-12/GettyImages-838600642.jpg?itok=kXtdMcha)
​
# Objetive
The objective of this project is to determine the best office location for a new company in the gaming industry. 
​
- **Designers** --> near to companies that do design.
- **30% of the company** --> have at least 1 child.
- **Developers** --> to be near tech startups that have raised at least 1 Million dollars.
- **Executives** --> like Starbucks.
- **Account managers** --> travel a lot.
- **Average age between 25 and 40** -->some place to go party.
- **CEO** --> vegan.
- **Maintenance guy** --> basketball court
- **Dog—"Dobby"** --> hairdresser every month. 
​
Based on all the information given by the employees, the first filters I applied to look for possible locations were:
 1. Near other tech companies for potential business between them.
 2. Close to public transport stops for comfortable employee mobility.
 3. Close to coffee, food or bar joints to satify a proper work life balance
​
# Working plan 
​
![workingflow](https://github.com/AnaAGG/P3_Geospatial_Data/blob/main/Images/Work_Flow.jpg)
​
First, I started by filtering a Crunchbase tech-company database using MongoDB. I obtained a set of XXX companies with coordinates located in **Madrid, London, and Berlin**. 
​
The coordinates were used to realice the Google Geocode, Places, and Nearby Places  APIS calls using "Tech Companies", "Cafeteria/Bars", and "Public Transport" as my keyword searches.
​
Once all the information was downloaded in json format, 
​
For the final decision of the location I have made a normalisation and assigned weights to the distances obtained. In the end, a ranking was obtained on which the final decision was based. 
​
The following resources have been used to achieve the objective of this project: 
​
-  [Google Cloud Api](https://cloud.google.com/apis/docs/overview): get access to global data and  content from thousands trusted sources. To access all the necessary information about the resources surrounding the possible locations of the enterprise. 
- [MongoDB](https://www.mongodb.com/): is a document database with the scalability and flexibility that we want using querying and indexing.
​
​
### Structure of the project files
​
The structure of this project is composed of:
 1. A folder of notebooks: 
    
    a) **Explore_Companies.ipynb** -->with the preliminary analysis where I search for companies that meet the requirements established a priori to be able to pre-select locations. 
​
    b) **APIs.ipynb** --> the call is made to the Api of "Foursquare Developers", where we will get some preferred conditions where we want our company to be located. 
​
    c) **Geospatial queries.ipynb** --> we make the spatial queries to calculate the distance between each point obtained in the Foursquare API and the locations selected at the beginning.
​
    d) **Madrid vs Barcelona vs Bilbao vs Gijon.ipynb** --> the relationship between each selected parameter (train stations, bars, vegan restaurants, basketball courts, and children's schools) and the possible locations (Madrid, Barcelona, Gijon and Bilbao) is evaluated. For this purpose, a normalisation and categorisation has been used. 
​
 2. scr folder: folder where all the .py files are stored with all the explained functions used during the whole project. The .py files included are: 
    a) APIsFunctions used in the APIs.ipynb
    b) GeospatialFunctions used in the Gespatial queries.ipynb
    c) CleaningFunctions used in the Madrid vs Barcelona vs Bilbao vs Gijon.ipynb
​
 3. Output: all the dataframes imported and saved in csv format. 
​
​
# Libraries
​
[sys](https://docs.python.org/3/library/sys.html)
​
[requests](https://pypi.org/project/requests/2.7.0/)
​
[pandas](https://pandas.pydata.org/)
​
[dotenv](https://pypi.org/project/python-dotenv/)
​
[pymongo](https://www.mongodb.com/2)
​
[json](https://docs.python.org/3/library/json.html)
​
[os](https://docs.python.org/3/library/os.html)
​
[geopandas](https://geopandas.org/)
​
[shapely](https://pypi.org/project/Shapely/)
​
[reduce](https://docs.python.org/3/library/functools.html)
​
[operator](https://docs.python.org/3/library/operator.html)
​
[import dumps](https://pymongo.readthedocs.io/en/stable/api/bson/json_util.html)
​
[re](https://docs.python.org/3/library/re.html)