Welcome to the web scraping crash course README!

# Udemy

## Udemy Course info:
* Course Title: Modern Web Scraping with Python using Scrapy Splash Selenium
* Course Link: https://www.udemy.com/course/web-scraping-in-python-using-scrapy-and-splash/

## Udemy Course projects:

### Project-1: worldometers (Part 1)
Learnings:
* scrapy commands (startproject, genspider, crawl)
* Basic scrapy shell commands
* Xpath expressions
* Build a spider (basic template)

### Project-2: worldometers (Part 2)
Learnings:
* Build a spider (basic template) capable to follow links
* Manage partial and absolute urls
* Export data in different formats

### Project-3: cigabuy (Part 1) 
Learnings:
* Build a spider (basic template) capable to manage pagination
* Set up obey robots.txt rules to false in settings.py
* Adjust default export encoding (add to settings.py utf-8 encoding)

### Project-4: cigabuy (Part 2) 
Learnings: 
* How to change scrapy default user agent to not being blocked:
> * Override default user-agent in settings.py
> * Override default request headers (user agent) in settings.py
> * Override default request headers (user agent) in the spyder python code (best option)


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

## Scrapy Commands:
scrapy: Allow to see all possible commands.

Available commands:

| command | action |
|---|---|
| crawl | Run a spider |
| edit | Edit spider |
| fetch | Fetch a URL using the Scrapy downloader |
| genspider | Generate new spider using pre-defined templates |
| runspider |  Run a self-contained spider (without creating a project) |
| settings | Get settings values |
| shell | Interactive scraping console |
| startproject | Create new project |
| version | Print Scrapy version |
| view | Open URL in browser, as seen by Scrapy |

Usage:

scrapy <command> [options] [args]

Examples:
* Set up a project: `scrapy startproject worldometers`
* Set up a spider: `scrapy genspider countries www.worldometers.info/world-population/population-by-country`
* Run a spider: `scrapy crawl countries` 
* Run a spyder and export data to .json: `scrapy crawl countries -o population_dataset.json`