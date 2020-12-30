Welcome to the web scraping crash course README!

# Udemy
* Course Title: Modern Web Scraping with Python using Scrapy Splash Selenium
* Course Link: https://www.udemy.com/course/web-scraping-in-python-using-scrapy-and-splash/

# Scrapy

## Scrapy documentation: 
https://docs.scrapy.org/en/latest/index.html

## Scrapy components:

Scrapy has 5 main components:
* Spyder: In this component is defined what is going to be extracted from the webpage. Scrappy has built in 5 type of spyders (spyder clases).
> * scrapy.Spider
> * CrawlSpyder
> * XMLFeedSpyder
> * CSVFeedSpyder
> * SitemapSpider
* Middleware: This component manages all the process related with the request and response.
* Scheduler: This Component is responsible to preserve the order of the tasks.
* Pipeline: In this component are defined data pipeline task as: cleaning, remove and storing
* Engine: Coordinates all the other components.