# python_mode
#python program to print
#mode of elements
from collections import Counter
#list of elements to calculate mode
n_num=[1,2,3,4,5,5,3,3,3,5,5]
n=len(n_num)
data=Counter(n_num)
print("Counter",data)
get_mode=dict(data)
print("get_mode after converting in dict",get_mode)
print("get_mode.items()",get_mode.items())
print("get_mode.items()",data.values())
mode=[k for k,v in get_mode.items() if v==max(list(data.values()))]
if len(mode)==n:
  get_mode="no mode found"
else:
  get_mode="Mode is/are:" +','.join(map(str,mode))
print(get_mode)
