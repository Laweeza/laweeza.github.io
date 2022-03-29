---
title: 'String Search'
date: 2022-02-23T00:33:37-08:00
description: 'An easy string technical challenge.'
type: post
tags: ['string', 'regex']
---

## String Search Prompt:

Given an array of strings and a search string as parameters, return a sorted array with these rules:

- Exact match
- Partial match
- Everything else

Account for case sensitivity and white spaces.

```
const pokemon = ['Charmander', 'charmeleon', 'CHARIZARD', 'Venasaur', 'IVYSaur', 'Bulbasaue'];

function searchSearch(string, pokeArray) {
  let exactMatch = pokeArray.filter(poke => poke.toLowerCase().trim() === string.replace(/\s+/g, '').toLowerCase());
  if (exactMatch.length > 0) {
    return exactMatch;
  } else {
    return pokeArray.filter(poke => poke.toLowerCase().trim().includes(string.replace(/\s+/g, '').toLowerCase()));
  }
}
```

### Explanation:

Check to see if the array has an exact match with the search string.

If there is no exact match, check to see if the elements in the array includes the search string as a substring.

[Useful tool to check Regex](https://regex101.com/)
