# ## Fulltime Week1 Quiz

# * Write a function ```readcurrency(filename)```
# that takes a filename as its argument.

# * This function reads the lines of a file, which are of the form

# ```
# USD 1.141911
# ```

# Where the first value is a currency and the second value is the
# Euro's value in that currency.

# * Return a list of dictionaries from this data, with each
# line of the file corresponding to an element in the dictionary.

# * Each element should have two keys, "symbol" and "rate" with the
# appropriate values.

# * The list will look like:

# ```python
# [
#   {"symbol": "AED", "rate": 4.194468},
#   {"symbol": "AFD", "rate": 83.493676},
#   {"symbol": "ALL", #... and so on
# ]
# ```
# * Upload your solution to a github repository. Either a new
# repository or in a folder in an existing one. Send me the link.

# #### Bonus

# * Write a second function ```save(filename, data)```

# * This takes a filename and the list constructed by the first list.

# * It wraps the list in a dictionary with a single key, "data"

# * It saves that dictionary to the json file specified by filename 

# ### Source of data (Not part of the quiz)

# * [https://fixer.io] A key for basic access comes with a free account 

# * Python code used:

# ```python
# import requests
# import json

# API_KEY = None
# KEY_FILE = "/home/redcartel/.credentials/fixer.io_key"
# OUTPUT_FILE = "currency.txt"

# with open(KEY_FILE, "r") as file_object:
#     API_KEY = file_object.readline().strip()

# URL = "http://data.fixer.io/api/latest?access_key=" + API_KEY

# return_text = requests.get(URL).text
# data = json.loads(requests.get(URL).text)
# rates = data["rates"]

# with open(OUTPUT_FILE, "w") as file_object:
#     for key in sorted(rates):
#         print(key, rates[key], file=file_object)
# ```

def readcurrency(file):

  with open(file, 'r') as f:
    file = "currency.txt"
    lines = f.readlines()
    word = lines.split()

    list1 =[]
    list2 =[]

for i in word:
  list1[i].append(word)
  i ^= 1
  return list[0]

for i in word:
  list2[i].append(word)
  i ^= 1
  return list[1]



new_key = { i : symbol for i in list[0] }

new_value = { i : rate for i in list[1] }

new_dictionary = zip(new_key , new_value)

print(new_dictionary)


