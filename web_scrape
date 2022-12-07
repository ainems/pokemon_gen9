## import libraries
from bs4 import BeautifulSoup as bs
import pandas as pd
import requests

## load webpage
link = 'https://game8.co/games/Pokemon-Scarlet-Violet/archives/391663#hl_1'
r = requests.get(link)

## make soup!!
soup = bs(r.content,features='html.parser')

## get table of pokemon for gen 9
table = soup.select('table')[1]

## convert to dataframe
gen_9_df = pd.read_html(str(table),flavor='bs4')[0]

## get CSV
gen_9_df.to_csv('gen_9.csv')
