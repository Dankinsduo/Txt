files = ['1.txt', '2.txt', '3.txt']
list_1 = []
for file in files:
  with open (file, 'r') as f:
      lines = f.readlines()
      list_1.append(lines)

list_sort = sorted(list_1, key=len)

with open('new.txt', 'w', encoding='UTF-8') as f:
  for lst in list_sort:
      f.write(''.join(lst) + '\n')