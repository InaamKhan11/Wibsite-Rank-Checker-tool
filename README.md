# Wibsite-Rank-Checker-tool

from googlesearch import search

import math

import urllib

my_website = "https://manfarid.pk"

print(f'Welcome to SEO Python keyword Rank finder, {my_website}')

keywords = [
  'manfarid', 'golarchi fruit', 'chicken drumsticks price',
  'chicken leg piece price in pakistan', 'chicken drum stick price',
  'saram fish', 'saram fish price in karachi', 'chicken online karachi',
  'cheekoo', 'surmai machi',]

print('\n\n\nSearching the whole Google for you...\n\n\n')


y = 0
for x in keywords:
  urls = search(keywords[y], tld="com", num=100, stop=100, pause=2)

  found = False
  for index, url in enumerate(urls):
    if my_website in url:
      print(
        f"\n{y+1}. Keyword: '{keywords[y]}' Rank: {index+1}, page:{math.ceil((index+1)/10)} \n"
      )

      found = True
      break

  if not found:
    print(f"\n{y+1}. Keyword: '{keywords[y]}' not found in first 100 pages.\n")
  y = y + 1

input('press enter to exit')



This is the output

Welcome to SEO Python keyword Rank finder, https://manfarid.pk

Searching the whole Google for you...

1. Keyword: 'manfarid' Rank: 1, page:1


2. Keyword: 'golarchi fruit' Rank: 1, page:1


3. Keyword: 'chicken drumsticks price' Rank: 7, page:1


4. Keyword: 'chicken leg piece price in pakistan' Rank: 8, page:1


5. Keyword: 'chicken drum stick price' Rank: 4, page:1


6. Keyword: 'saram fish' Rank: 7, page:1


7. Keyword: 'saram fish price in karachi' Rank: 4, page:1


8. Keyword: 'chicken online karachi' Rank: 11, page:2


9. Keyword: 'cheekoo' Rank: 4, page:1


10. Keyword: 'surmai machi' not found in first 100 pages.

press enter to exit
