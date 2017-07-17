# Pokedex
Build a Pokedex to recognize Pokemons on the Gameboy screen by Opencv in Python3.6.    
This article is based on pyimagesearch (Python2.7):     
http://www.pyimagesearch.com/category/building-a-pokedex/

# How to use

1. Scrape the pictures of pokemon from Internet and save them in the folder 'sprites'
```
python3 parse_and_download.py --pokemon-list pokemon_list.html --sprites sprites
```

2. Store the features of each picture in the index.cpickle file 
```
python3 index.py --sprites sprites --index index.cpickle
```

3. Crop the Gameboy screen from the input picture.
```
python3 find_screen.py --query queries/query_marowak.jpg
```

4. Search which Pokemon is in the cropped picture.
```
python3 search.py --index index.cpickle --query cropped.png
```
