###  LIST:
# 1. it is a heteregeneous datatype (i.e) list can have any data type inside it.
# 2. inside list elements are seperated by comma.
# 3. Every element has it own individual 

SAMPLE PROGRAM:
a = list() # []
print(a)
a = []
print(a)

SAMPLE PROGRAM
a = [1,2,3,'Mag,esh',123.123,'i love India',123,1239,'2131231']
  #  0 1 2     3       4          5          6   7      8

print(a)
print(a[3])
print(type(a[7])) # int

OUTPUT:
"mag,esh"
1239

STRING:
str() # any datatype into str
###list() # it convert any iterable datatype into list

# iterable datatype - for a datatype which we can do iteration

# iteration - to take all the element from that datatype by using either for loop or while loop

# Non - iterable datatype   -   int , float , bool  , None

# iterable datatype         -   str , list  , tuple , dict  , range , iterator...

SAMPLE OUTPUT PROGRAM:
a = '1231ame'
list(a) # all elements in a list will become str elements ['1','2','3','1','a','m','e']

# append

# append will take only one element/argument
# to add the single element at the end of the list

a = ['1', '2', '3', '1', 'a', 'm', 'e']
print(a.append('magesh')) # None
a.append(45)
a.append('45')
a.append(['45',1,2,3,4])
# a.append(['45',1,2,3,4],4) # error
print(a)

OUTPUT:
None
['1', '2', '3', '1', 'a', 'm', 'e', 'magesh', 45, '45', ['45', 1, 2, 3, 4]]

##pop

# pop will take only one element/argument
# to remove the single element at the end of the list

a = ['1', '2', '3', '1', 'a', 'm', 'e']
print(a.pop()) # e
a.pop()
# a.pop(['45',1,2,3,4],4) # error
print(a)

a = ['1', '2', '3', '1', 'a', 'm', 'e']
a.pop(2) # 2 = index number
print(a)

OUTPUT:
e
['1', '2', '3', '1', 'a']
['1', '2', '1', 'a', 'm', 'e']

###count:

# similar to str refer day2 notes

a = ['1', '2', '1', 'a', 'm', 'e',1,2,1,2,2]

print(a.count('1'))
print(a.count(1))
print(a.count(2))   # 3
print(a.count('2')) # 1

OUTPIUT:
2
2
3
1

###extend

# extend will take a main list from tat all elements will be added to the soruce  element
# to add the  element at the end of the list

a = ['1', '2', '1', 'a', 'm', 'e']
a.extend([1,2,3,[1,2,3,4],8])
a

OUTPUT:
['1', '2', '1', 'a', 'm', 'e', 1, 2, 3, [1, 2, 3, 4], 8]

###insert

# to add the  element at the index number of the list

a = ['1', '2', '1', 'a', 'm', 'e']

syntax:
# a.insert( Index_number , element )

a.insert(4,'magesh')
a

OUTPUT:
['1', '2', '1', 'a', 'magesh', 'm', 'e']

###copy

a = [1,2,3,4]
b = a                 # a & b share common memory

a.append(56)
b.append('569')

print(a)
print(b)


a = [1,2,3,4]
b = a.copy()           # a & b have different memory

a.append(56)
b.append('569')

print(a)
print(b)

OUTPUT:
[1, 2, 3, 4, 56, '569']
[1, 2, 3, 4, 56, '569']
[1, 2, 3, 4, 56]
[1, 2, 3, 4, '569']

###join:

# syntax:
# 'substring'.join(list_variable)

# 1. substring will be placed in b/w all the elements of string
# 2. join can be used only if all the elements are str
# 3. output of join will be a str


a = ['1', '2', 2]
# print('-'.join(a)) # error

a = ['1', '2', '2']
print('-'.join(a)) 

# sort:

# use when all elements are int
# it will chnage the source

a = [1,21,31,4,32,1234,345]
print(a.sort()) # None
print(a)

OUTPUT:
None
[1, 4, 21, 31, 32, 345, 1234]

###sorted:

# use when all elements are int
# it will give the new output

a = [1,21,31,4,32,1234,345]
print('sorted output',sorted(a)) # NEW direct output
print('source',a) # unchanged

OUTPUT:
sorted output [1, 4, 21, 31, 32, 345, 1234]
source [1, 21, 31, 4, 32, 1234, 345]

###reverse:

# it will chnage the source

a = [1,21,31,4,32,1234,345]
print(a.reverse()) # None
print(a)

OUTPUT:
None
[345, 1234, 32, 4, 31, 21, 1]

# reversed:

# use when all elements are int
# it will give the new output
# output will be an iterator datatype   |   we have to convert it to list

# list()

a = [1,21,31,4,32,1234,345]
print(a[::-1]) # Reverse
print('sorted output',list(reversed(a))) # direct output
print('source',a) # unchanged

OUTPUT;
[345, 1234, 32, 4, 31, 21, 1]
sorted output [345, 1234, 32, 4, 31, 21, 1]
source [1, 21, 31, 4, 32, 1234, 345]

###Index:

# similar to str

a = [1,21,31,4,32,1234,345]
a.index(4)

# ITEM ASSIGNMENT:

a = [1,21,31,4,32,1234,345]----->ONLY WE DO IN THE LIST DATATYPE IN ITEM ASSIGNMENT

a[3] = "magesh"
a[5] = [1,2,3,4,5]

print(a)

OUTPUT:
[1, 21, 31, 'magesh', 32, [1, 2, 3, 4, 5], 345]

###TUPLE:

# TUPLE:

# tuple is a immutable datatype (i.e) we cannoct do item assignment

tuple() # it convert any iterable datatype into list

# normal indexing and slicing can be done similar to list & str

a = (1,2,3,4,[11,12,('magesh','rose'),13,123,43],4545)

print(a[4])
print(a[4][2])
print(a[4][2][1])

print(a[4][1])

a[4][2] = 'IT A LIST'

a[4][1] = 'Jack'
print(a)

OUTPUT:
[11, 12, ('magesh', 'rose'), 13, 123, 43]
('magesh', 'rose')
rose
12
(1, 2, 3, 4, [11, 'Jack', 'IT A LIST', 13, 123, 43], 4545)

###SET:
# set is a collections of un-ordered datatype (i.e) set dosent support indexing or slicing

# set elements is immutable (i.e) it will have only unique elements

set() # it convert any iterable datatype into list

SAMPLE OUTPROGRAM:
a = {1,112,67,342,3,4,5}

print(type(a))

print(a)
OUTPUT:<class 'set'>
{112, 1, 3, 67, 4, 5, 342}

###SET METHODS:
a = {'1',1, 2, 11,'   '}
a.add('magesh')
print(a)

OUTPUT:
{1, 2, 'magesh', '1', 11, '   '}

###STRINGS METHODS:
a = {1,2,3,4,5}
b = {4,5,6,7,8,9,10}
aa = {4,5,3}

c = a.union(b)
print(c)

c = a.intersection(b)
print(c)

c = a.difference(b) # only elements in a
print(c)

c = b.difference(a) # only elements in b
print(c)

c = b.symmetric_difference(a) # [union - intersection]   i.e opposite of intersection OR ONLY ELEMENTS OF (A + B)
print(c)

c = aa.issubset(a)
print(c)

c = a.issuperset(aa)
print(c)

c = b.issuperset(aa)
print(c)

###ISDISJOINT:
a = {1,2,3}
b = {4,5,6,7,8,9,10}

print(a.isdisjoint(b)) # if it has intersection output will be False or it will be True

# a.remove(11)        # if element isnot there it will throw error
print(a.discard(11))  # even if element is not there it will not throw error
OUTPUT:
True
None

###DICT;

----->It is the hetrogeneous dataype.
-----> # 1. dict wont support indexing
# 2. we will take value by using key
# 3. we cannoct take key by using value
# 4. keys should be unique
# 5. if the key is common means latest key-value pair will be considired
# 6. key should have only data-types like ->  str, int, float , bool , tuple
# 7. value can be of any datatype
# 8. a new key-value pair can be added to dict like list-> item assignment
# 9. if a key is already presented the value will get updated

##SYNTAX:
a = { "key1" : "value1" , "key2" : "value2" , "key3" : "value3" , '1' : ["value3","magesh"] , 1: {1:2,2:3,3:4} }

###syntax:
# a[key]

print(a)

print(a['key1'])
print(a['key2'])
print(a[1])

a['name'] = 'Magesh'

a[1] = 'Magesh'




print(a)

# print(a["value2"]) # key error

output:
{'key1': 'value1', 'key2': 'value2', 'key3': 'value3', '1': ['value3', 'magesh'], 1: {1: 2, 2: 3, 3: 4}}
value1
value2
{1: 2, 2: 3, 3: 4}
{'key1': 'value1', 'key2': 'value2', 'key3': 'value3', '1': ['value3', 'magesh'], 1: 'Magesh', 'name': 'Magesh'}
