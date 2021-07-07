# Mission-to-Mars
## Project Overview
This project use BeautifulSoup and Splinter to scrape Mars headlines, Mars facts data and full-resolution images of Mar's hemispheres and the titles of those images,store the scraped data on a Mongo database. Use a web application to display the data, and alter the design of the web application to accommodate these images to be mobile as well as desktop responsive.

## Resources
- Python file : scraping.py, app.py
- HTML : index.html
- Pandas file: Mission_to_Mars_Challenge.ipynb
- Mongo DB

## Pandas 
Pandas provide huge advantage in scraping of data from various platform because it provides the flexibility to check the code at each step and correct if any issues. In **Mission_to_Mars_Challenge.ipynb** we are scraping Mars data from following sites and building our own web page using splinter and BeautifulSoup inside python.

- https://redplanetscience.com : Mars news data
- https://spaceimages-mars.com : Mars space image and data facts.
- https://marshemispheres.com/ : Mars hemisphere images.

## Python
- scraping.py : Using the pandas code base, we are building **scraping.py** and defining each data scraping in functions. Finally building scrape_all function which collectively calls individual data scraping and storing data in dictionary.

- app.py : In this code, we are integrating HTML and python scraping.py code using Mongo db. We are calling scrape_all function to collect all data and store them in Mongo DB doing **upsert**. This helps in retrieval of data using HTML dynamically.

## Mongo DB
we are creating new database name as **mars_app** in Mongo DB. Inside the mars_app database , we are storing the data dictionary returned by scrape_all function which contains mars news, title, images and facts and store them as mars_data file.

## HTML
**Index.html** is created to access the python files and scrape the data dynamically. HTML uses bootstrap components and provides styling and alignment of data in the web page. We are accessing mongoDB inside HTML to show the data dynamically.

