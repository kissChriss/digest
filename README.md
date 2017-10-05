#### Count the number of big and small letters in the string

#1. slow variant
```python
def func(word):
  small = 0
  big = 0
  sm_list = 'qwertyuiopasdfghjklzxcvbnm'
  bg_list = 'QWERTYUIOPASDFGHJKLZXCVBNM'
  for letter in word:
    if letter in  sm_list:
      small += 1
    if letter in bg_list:
      big += 1
  print ('small:', small)
  print ('big:', big)
  return word
  
func('YouR wOrD')
```

#2. fast variant
```python
def func(word):
  small = 0
  big = 0
  for letter in word:
    if 'a' <= letter <= 'z':
      small +=1
    if 'A' <= letter <= 'Z':
      big += 1
  print ('small:', small)
  print ('big:', big)
  return word

in_word = input('Enter your word: ')
func(in_word) 
```

#3 one more fast variant 
'''python
def func(word):
  small, big = 0, 0
  for letter in word:
    if letter.islower():
      small +=1
    elif letter.isupper():
      big += 1
  print ('small:', small)
  print ('big:', big)
  return word

in_word = input('Enter your word or string: ')
func(in_word) 
'''
