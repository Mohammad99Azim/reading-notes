# Web Scraping

Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort. In this article, we will go through an easy example of how to automate


**Example**

downloading hundreds of files from the New York MTA. This is a great exercise for web scraping beginners who are looking to understand how to web scrape.

### New York MTA Data
We will be downloading turnstile data from this site:

`` http://web.mta.info/developers/turnstile.html ``

hundreds of .txt files exist on the site. Below is a snippet of what some of the data looks like. Each date is a link to the .txt file that you can download.

![the_data](https://miro.medium.com/max/233/1*5Hwlx8IZxJ0m7AIx0TnddA.png)


#### Important !!!
Important notes about web scraping:
 - Read through the website’s Terms and Conditions to understand how you can legally use the data. Most sites prohibit you from using the data for commercial purposes.
 - Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be blocked from the site as well.


### Python Code

We start by importing the following libraries.

```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```


Next, we set the url to the website and access the site with our requests library.

```
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)

```

If the access was successful, you should see the following output:

![output](https://miro.medium.com/max/414/1*fyqRGzG8IbhhjxF2Q5MU_Q.png)





[link](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)
