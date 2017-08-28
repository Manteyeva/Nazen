# Nazen
Dictionary

We are given a list of lists in the following format:
[ [‘apple’, ‘banana’, ‘oranges’],
  [‘apartment’, ‘house’, ‘fan’],
  [‘automobile’, ‘wheel’, ‘car’]] (‘wheel = my_list[2][1])
Our aim is to output the following table, where each entry is right adjusted:
    apple     apartment automobile
   banana         house      wheel
  oranges           fan        car

Method to solve this problem:
For each member of our dataset find maximum length.
Use these numbers to right adjust strings

my_list = [['apple', 'banana', 'oranges'],
           ['apartment', 'house', 'fan'],
           ['automobile', 'wheel', 'car']]
new_list = []
for item in my_list:
    listOfLengths = [len(element) for element in item] 
    maximum = max(listOfLengths)
    new_list.append(maximum) 
print (new_list) (1)

for i in range(3):
    wholeString = ''
    for j in range(3):
        component = my_list[j][i].rjust(new_list[j])
        wholeString = wholeString + component + ' '
    print(wholeString)

Answer:
    apple     apartment automobile
   banana         house      wheel
  oranges           fan        car



