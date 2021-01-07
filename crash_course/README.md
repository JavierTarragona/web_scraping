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
* How to change scrapy default user agent to not being blocked (adding google chrome default):
> * Override default user-agent in settings.py
> * Override default request headers (user agent) in settings.py
> * Override default request headers (user agent) in the spyder python code (best option)

### Project-5: imdb
Learnings:
* Build a spider (CrawlSpider template) capable to follow links using rules property.
* Build a spider (CrawlSpider template) capable to manage pagination using rules property.
* How to change default user-agent in CrawlSpider template.
* Xpath expression using normalize-space function (remove white spaces).

### Project-6: livecoin (splash)
Learnings: 
* Build a spider (basic template) capable to crawl pages that use java using splash.
* Configure settings.py to use scrapy-splash (https://github.com/scrapy-plugins/scrapy-splash).

### Project-7: livecoin (selenium)
Learnings: 
* Build a spider (basic template) capable to crawl pages that use java using selenium (more intuitive).
* Install selenium (https://selenium-python.readthedocs.io/).

### Project-8: cigabuy (Part 3) 
Learnings:
* Techniques to avoid getting blacklisted by websites while scraping them:
> * Modify concurrent_request variable in settings.py.
> * Modify download_delay variable in settings.py adding a delay between each request sent.
> * Modify autothrottle_start_delay in settings.py.
> * Modify user agent.
* Build a random rotator user agent:
> * Build customed middleware (UserAgentRotatorMiddleware) in middlewares.py
> * Adjust settings to use (UserAgentRotatorMiddleware)

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
* Pipeline: In this component are defined data pipeline task as: cleaning, remove and storing in db.
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
* Set up a spider (specific template): `scrapy genspider -t crawl best_movies imdb.com`
* Run a spider: `scrapy crawl countries` 
* Run a spyder and export data to .json: `scrapy crawl countries -o population_dataset.json`