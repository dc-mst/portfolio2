---
title: Overwriting dictionary key
summary: Avoing for loop overwriting dictionary keys
date: 2023-05-22
lastmod: 2023-05-22
tags: [ Python ]
---

```
mylist = ['word1', 'word2', 'word3']

def get_word_by_type(word_list):
    pokedex = {}
    for word_name in word_list:
        url       = f'https://myapi.co/api/word/{word_name}'
        response  = requests.get(url)
        weight    = response.json()['weight']
        abilities = []
        for ability in response.json()['abilities']:
            abilities.append(ability['ability']['name'].title())
        for t in response.json()['types']:
            worddex.setdefault(t['type']['name'], {})[word_name] = {'Language': language, 'Length' : length}}
    return worddex
            
get_word_by_type(mylist)
```