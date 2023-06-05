## Python Tutorial
python is :
1. general purpose
2. case sensitive
3. interpreted language not compiled.

# this is a comment 

#### Data types in python:
str, int, float, complex, bool, None

list -- [1,2,"other"] -- somewhat like array but can hold any datatype, 

tuple -- (1,2,"other") -- somewhat like list but cannot be updated once created, 

range -- range(100) -- it produces a range of values like form 0 to 100,

dict -- {"key1":"value1","key2":"value2"} -- key value pair,

set -- {"val1","val2",1} -- does not hold data in order and no duplicates are kept, 

frozenset -- {"val1","val2",1} -- set that cannot be updated once created, 

bytes -- b'binary_value_you_cannot_read' -- holds binary data.

Immutable : str, tuple, frozenset, bytes

#### CRUD with python for various data types ######
-----------------
Basic data type | 
-----------------

-----------------------------------------------------------------------------------------------------
|data type   | create            | Read                  | Update                | Delete            |
|------------|-------------------|-----------------------|-----------------------|-------------------|
|------------|-------------------|-----------------------|-----------------------|-------------------|
|str         |str1 = ""          |str2 = str1[:2]        |str1[0] = "7" #err     |del str1           |
|            |str1 =str1 + "5min"|str2 = str1[-1]        |str is immutable       |                   |
|------------|-------------------|-----------------------|-----------------------|-------------------|
|int         |int1 = 1           |int2 = int1            |int1 = 2               |del int1           |
|------------|-------------------|-----------------------|-----------------------|-------------------|
|float       |f1 = 1.2           |f2= f1                 |f1 = 10*5.79           |del f1             | 
|------------|-------------------|-----------------------|-----------------------|-------------------|
|bool        |b1 = True          |b2= b1                 |b1 = False             |del b1             | 
-----------------------------------------------------------------------------------------------------

-----------------
Advanced once   |
-----------------

-----------------------------------------------------------------------------------------------------
|data type   | create            | Read                  | Update                | Delete            |
|------------|-------------------|-----------------------|-----------------------|-------------------|
|------------|-------------------|-----------------------|-----------------------|-------------------|
|list        |list1 = list()     |list2 = list1[:]       |list1[0] = 25          |del list1          |
|            |list1 = []         |copy list1 to list2    |list1.append(36)       |del list1[2:5]     |
|            |list1 = [1,2,3]    |list2 = list1[2:]      |list1 = list1+[5,10]   |list1.pop() #last  |
|            |                   |                       |list1.insert(2,"val")  |list.pop(5) #5th   |
|------------|-------------------|-----------------------|-----------------------|-------------------|
|tuple       |tuple1 = tuple()   |tuple2 = tuple1[:]     |tuple1[0] = 25 #err    |del tuple1         |
|            |tuple1 = ()        |copy tuple1 to tuple2  |tuples are immutable   |                   |
|            |tuple1 = (1,2,3)   |tuple2 = tuple1[2:]    |list1 = list1+(5,10)   |                   |
|------------|-------------------|-----------------------|-----------------------|-------------------|
|set         |set1 = set()       |set2 = set1.copy()     |set1.update({5,10})    |del set1           |
|            |set1 = {1,2,3}     |copy set1 to set2      |set1.add(1)            |set1.remove(5)     |
|            |                   |set have no indexes    |set2 = set1|{5,10}     |set1.pop()         |
|            |                   |                       |set2 = set1&{5,10}     |set1.clear()       |
|------------|-------------------|-----------------------|-----------------------|-------------------|
|dict        |dict1={}           |dict2 = dict1.copy()   |dict1.update({'k1':'v1'|del dict1          |
|            |dict1={'k1','v1'}  |copy dict1 to dict2    |,'k2':'v2'})           |del dict1["key1"]  |
|            |                   |value = dict1['k1']    |dict1['k1']='newV1'    |                   |
|            |                   |value=dict1.get('k2',0)|                       |                   |
|            |                   |allkeys=dict1.keys()   |                       |                   |
|            |                   |values=dict1.values()  |                       |                   |
|            |                   |allitems=dict1.items() |                       |                   |
-----------------------------------------------------------------------------------------------------

### conditions #####
```
if i>0 and j<0:

elif condition:
#Note: elif can be replaced with "else if"

else:
```
### loops #####
```
---
# for list - l1
for val in l1:
    print(val)
---
# for dict - dict1
for k,v in dict1.items():
    print(k,v)
OR
for k in dict1.keys():
    print(k,dict1[k])   
---
i = 0
while i<len(l1):
    print(l1[i])
    i++
---

```
### functions ####

```
def adder(param1,param2=2):
    return param1+param2

adder_in_lambda_style = lambda param1,param2 : param1+param2

def adder(*args):
    print(args)

def adder(**kargs):
    print(kargs)
```
### classes & Objects ###
```
class A:
    def __init__(self,var1_value=5):
        self.var1 = var1_value
    def A_printer(self):
        print(self.A)
```

### inheritance ###
```
class Person:
  def __init__(self, fname=1, lname=2):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

class Student(Person):
  def __init__(self, fname, lname):
  	super().__init__(fname, lname)

x = Student("Mike", "Olsen")
x.printname()
```
### file_handling ###
```
with open(r'.\app.log', 'r') as fh:
    file_data = fh.read()
    print(file_data)

OR 

fh = open(r'.\app.log', 'r')
file_data = fh.read()
print(file_data)
fh.close()
```
