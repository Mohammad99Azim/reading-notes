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

Next we parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure. If you are interested in learning more about this library, check out the [BeatifulSoup documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/).   **Check it later**

```
soup = BeautifulSoup(response.text, “html.parser”)
```
We use the method .findAll to locate all of our <a> tags.
 
```
soup.findAll('a')
```

 This code gives us every line of code that has an <a> tag. The information that we are interested in 
 
 
 Next, let’s extract the actual link that we want. Let’s test out the first link.
 
 ```
one_a_tag = soup.findAll(‘a’)[38]
link = one_a_tag[‘href’]
 ```

 This code saves the first text file, ‘data/nyct/turnstile/turnstile_180922.txt’ to our variable link. The full url to download the data is actually ‘http://web.mta.info/developers/data/nyct/turnstile/turnstile_180922.txt’ which I discovered by clicking on the first data file on the website as a test. We can use our urllib.request library to download this file path to our computer. We provide request.urlretrieve with two parameters: file url and the filename. For my files, I named them “turnstile_180922.txt”, “turnstile_180901”, etc.


```
download_url = 'http://web.mta.info/developers/'+ link
urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])
```
Last but not least, we should include this line of code so that we can pause our code for a second so that we are not spamming the website with requests. This helps us avoid getting flagged as a spammer.
 
```
time.sleep(1)
```

Full Code
 ```
 # Import libraries
import requests
import urllib.request
import time
from bs4 import BeautifulSoup

# Set the URL you want to webscrape from
url = 'http://web.mta.info/developers/turnstile.html'

# Connect to the URL
response = requests.get(url)

# Parse HTML and save to BeautifulSoup object¶
soup = BeautifulSoup(response.text, "html.parser")

# To download the whole data set, let's do a for loop through all a tags
line_count = 1 #variable to track what line you are on
for one_a_tag in soup.findAll('a'):  #'a' tags are for links
    if line_count >= 36: #code for text files starts at line 36
        link = one_a_tag['href']
        download_url = 'http://web.mta.info/developers/'+ link
        urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:]) 
        time.sleep(1) #pause the code for a sec
    #add 1 for next line
    line_count +=1
 ```
 



[link](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)
 
 
[tips](https://www.danielherediamejias.com/6-basic-tips-to-perform-web-scraping-with-python/)
