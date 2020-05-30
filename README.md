# web-scraping-demos
demos of web scraping using BeautifulSoup, Scrapy, Requests-Html, Scrapy, etc.

## Basic scraping using Jupyter Lab

In this demo we showcase and use various technologies : ``Jupyter Lab`` as a developer environment, ``Requests`` as a http client library, ``BeautifulSoup`` as a web page parsing library. As well as ``pipenv`` and ``pyenv`` as projects ecosystem management tools.

1. setup your environment

2. open a jupyter lab browser tab by issuing this command
  in your terminal : ``$ jupyter lab``
  it will open a Jupyter Lab notebook in a new browser tab

3. copy/paste the code below and run code (press play)

4. it will download Tesla Wikipedia page in html format in current directory

### setup your environment by issuing these commands, one by one, in the terminal

1. pyenv install 3.7.4
2. pyenv local 3.7.4

3. pipenv --python 3.7.4
4. pipenv install requests
5. pipenv install beautifulsoup4
6. pipenv install pandas

7. pipenv install jupyterlab

#### check installation by running these commands (optional)

``$ !pyenv local``
``$ !python -V``
``$ !pip list``

#### scraping code code

``import requests
import BeautifulSoup4
import pandas as pd

start_url = 'https://en.wikipedia.org/wiki/Tesla,_Inc.'

downloaded_html = requests.get(start_url)

soup = bs4.BeautifulSoup4(downloaded_html.text)

with open('downloaded.html', 'w') as file:
	file.write(soup.prettify())``

