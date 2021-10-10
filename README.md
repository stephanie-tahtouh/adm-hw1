# adm-hw1[Submissions_HackerRank.pdf](https://github.com/stephanie-tahtouh/adm-hw1/files/7318301/Submissions_HackerRank.pdf)


from __future__ import print_function
#Transpose and Flatten
import numpy
mat=[]
n, m = map(int, input().split())
for i in range(n):
    mat.append(list(map(int, input().split())))
    matrix=numpy.array(mat)
print (numpy.transpose(matrix))
print (matrix.flatten())

#Shape and Reshape
import numpy
a=list(map(int,input().split()))
array=numpy.array(a)
print (numpy.reshape(array,(3,3)))

# Arrays
def arrays(arr):
    arr.reverse()
    return numpy.array(arr,float)
    
#Calendar Module
s=input().split()
m=int(s[0])
d=int(s[1])
y=int(s[2])
import calendar
print ( (calendar.day_name[calendar.weekday(year=y,month=m,day=d)]).upper())

#Map and Lambda Function
cube = lambda x: x**3

def fibonacci(n):
    if n==0:
        return[]
    elif n==1:
        return [0]
    else:
        fib=[0,1]
        for i in range(2,n):
            fib.append(fib[i-1]+fib[i-2])
        return fib
#Exceptions
T=int(input())
for i in range(T):
    a,b=input().split()
    try:
        print (int(a)//int(b))
    except ZeroDivisionError as e:
        print ("Error Code:",e)
    except ValueError as e:
        print("Error Code:",e)
#collections.Counter()
from collections import Counter
x=int(input())
d=Counter(map(int, input().split()))
money=[]
n=int(input())
for i in range(n):
    s,p=map(int,input().split())
    if s in d.keys() and d[s]!=0:
        money.append(p)
        d.subtract(Counter([s]))
        d
print(sum(money))

#No Idea!
nm=input()
n,m=nm.split()
N=int(n)
M=int(m)
array= [int(item) for item in input().split()]
a=input().split()
A=set(map(int,a))
b=input().split()
B=set(map(int,b))
c=0
for i in range(len(array)):
    if array[i] in A:
        c+=1
    if array[i] in B:
        c-=1
print(c)

#Set Mutations
a=int(input())
A=set(map(int, input().split()))
N=int(input())
c=[]
n=set()
for i in range(N):
    c.append(input().split())
    n=set(map(int, input().split()))
    if c[i][0]=='intersection_update':
        A.intersection_update(n)
    if c[i][0]=='update':
        A.update(n)
    if c[i][0]=='intersection_update':
        A.intersection_update(n)
    if c[i][0]=='symmetric_difference_update':
        A.symmetric_difference_update(n)
    if c[i][0]=='difference_update':
        A.difference_update(n)
print(sum(A))
    
    
#Set .symmetric_difference() Operation
n=int(input())
e= set(map(int, input().split()))
b=int(input())
f= set(map(int, input().split()))
print(len(e.symmetric_difference(f)))

#Set .difference() Operation
n=int(input())
e= set(map(int, input().split()))
b=int(input())
f= set(map(int, input().split()))
print(len(e.difference(f)))

# Set .intersection() Operation
n=int(input())
e= set(map(int, input().split()))
b=int(input())
f= set(map(int, input().split()))
print(len(e.intersection(f)))

#Set .union() Operation
n=int(input())
e= set(map(int, input().split()))
b=int(input())
f= set(map(int, input().split()))
print(len(e.union(f)))

#Set .discard(), .remove() & .pop()
n = int(input())
s = set(map(int, input().split()))
N = int(input())
c=[]
for i in range(N):
    c.append(input())
    if c[i]=='pop':
        s.pop()
    if c[i][:6]=='remove':
        s.remove(int(c[i][7]))
    if c[i][:7]=='discard':
        s.discard(int(c[i][8]))
print(sum(s))

#Set .add()
n=int(input())
s=set()
for i in range(n):
    s.add(str(input()))
print(len(s))

#Symmetric Difference
# Enter your code here. Read input from STDIN. Print output to STDOUT
n=int(input())
a=input().split()
m=int(input())
b=input().split()
newa=set(a)
newb=set(b)
s=sorted(list((newa.difference(newb)).union(newb.difference(newa))),key=int)
print ('\n'.join(s))

#Introduction to Sets
def average(array):
    return round(sum(set(array))/len(set(array))*1.000,3)

#Capitalize!
def solve(s):
    a=s.split(' ')
    b=[]
    for i in range(len(a)):
        a[i]=a[i].capitalize()
    c=str(" ".join(a))
    return c
#Nested Lists
if __name__ == '__main__':
    n=int(input())
    l=[]
    for _ in range(n):
        name = input()
        score = float(input())
        l.append([score,name])
    l.sort()
    list=[]
    for i in range(1,len(l)):
        if l[i][0]!=l[0][0]:
            list.append(l[i])
    a=[]
    a.append(list[0][1])
    for i in range(1,len(list)):
        if list[i][0]==list[0][0]:
            a.append(list[i][1])
    a.sort()
    for i in a:
        print(i)
#Finding the percentage
    if __name__ == '__main__':
        n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
    avg=0
    s=0
    for j in student_marks[query_name]:
        s+=j
        avg=s/(len(student_marks[query_name]))
    print(format(avg,".2f"))
#Designer Door Mat
import textwrap
s=input()
a=[s[i] for i in range(s.index(" "))]
n=int("".join(a))
m=n*3
string='.|.'
for i in range(n//2):
    print (textwrap.fill(string.center(m,'-'),m))
    string+='.|..|.'
print (textwrap.fill('WELCOME'.center(m,'-'),m))
for j in range(6,len(string),6):
    print (textwrap.fill(string[:-j].center(m,'-'),m))



#Text Wrap
def wrap(string, max_width):
    return textwrap.fill(string,max_width)
#Text Alignment
#Replace all ______ with rjust, ljust or center. 

thickness = int(input()) #This must be an odd number
c = 'H'

#Top Cone
for i in range(thickness):
    print((c*i).rjust(thickness-1)+c+(c*i).ljust(thickness-1))

#Top Pillars
for i in range(thickness+1):
    print((c*thickness).center(thickness*2)+(c*thickness).center(thickness*6))

#Middle Belt
for i in range((thickness+1)//2):
    print((c*thickness*5).center(thickness*6))    

#Bottom Pillars
for i in range(thickness+1):
    print((c*thickness).center(thickness*2)+(c*thickness).center(thickness*6))    

#Bottom Cone
for i in range(thickness):
    print(((c*(thickness-i-1)).rjust(thickness)+c+(c*(thickness-i-1)).ljust(thickness)).rjust(thickness*6))



#String Validators
    if __name__ == '__main__':
        s = input()
    def alnum(s):
        for i in range(len(s)):
            if s[i].isalnum():
                return True
        return False
    def alpha(s):
        for i in range(len(s)):
            if s[i].isalpha():
                return True
        return False
    def digit(s):
        for i in range(len(s)):
            if s[i].isdigit():
                return True
        return False
    def lower(s):
        for i in range(len(s)):
            if s[i].islower():
                return True
        return False
    def upper(s):
        for i in range(len(s)):
            if s[i].isupper():
                return True
        return False
    print(alnum(s))
    print(alpha(s))
    print(digit(s))
    print(lower(s))
    print(upper(s))

#Find a string
def count_substring(string, sub_string):
    c=0
    for i in range(len(string)):
        if string[i:i+len(sub_string)]==sub_string:
            c+=1
    
    return c
#Mutations
def mutate_string(string, position, character):
    l = list(string)
    l[position] = character
    string = ''.join(l)
    return string

#What's Your Name?

def print_full_name(first, last):
    print("Hello "+first+" "+last+"! You just delved into python.")

#String Split and Join
def split_and_join(line):
    line = line.split(" ")
    line="-".join(line)
    return(line)

#sWAP cASE
def swap_case(s):
    return s.swapcase()

#Tuples
if __name__ == '__main__':
    n = int(raw_input())
    integer_list = map(int, raw_input().split())
    t=(int(n) for n in integer_list)
    tu= tuple(t)
    print (hash(tu))
    
    
#Lists
if __name__ == '__main__':
    N = int(input())
    list=[]
    command={}
    for i in range(N):
        command[i]=input()
        if command[i][:3]=="ins":
            list.insert(int(command[i][7]),int(command[i][9:len(command[i])+1]))
        elif command[i][:3]=="pri":
            print(list)
        elif command[i][:3]=="rem":
            list.remove(int(command[i][7]))
        elif command[i][:3]=="app":
            list.append(int(command[i][7:len(command[i])+1]))
        elif command[i][:3]=="sor":
            list.sort()
        elif command[i][:3]=="pop":
            list.pop(len(list)-1)
        else:
            list.reverse()


#Find the Runner-Up Score!
if __name__ == '__main__':
    n = int(raw_input())
    arr = map(int, raw_input().split())
l=[int(i) for i in arr if i!=" "]
m=max(l)
l.remove(max(l))
l=[ i for i in l if i!=m]
print(max(l))

#List Comprehensions
if __name__ == '__main__':
    x = int(raw_input())
    y = int(raw_input())
    z = int(raw_input())
    n = int(raw_input())

permutations=[]
for i in range(0,x+1):
    for j in range(0,y+1):
        for k in range(0,z+1):
            permutations.append([i,j,k])
result=[a for a in permutations if a[0]+a[1]+a[2]!=n]
print(result)

#Print Function


if __name__ == '__main__':
    n = int(raw_input())
for i in range(1,n+1):
    print(i, end='')
    
#Write a function
def is_leap(year):
    leap = False
    if year%400==0:
        leap=True
    elif year%100==0:
        leap=False
    elif year%4==0:
        leap=True
    # Write your logic here
    
    return leap



#Loops
if __name__ == '__main__':
    n = int(raw_input())
less_than_n=[s for s in range(0,n,1)]
for i in range(0,len(less_than_n)):
    print(less_than_n[i]**2)

#Python: Division


if __name__ == '__main__':
    a = int(raw_input())
    b = int(raw_input())

print(a//b)
print(a/b)

#Arithmetic Operators
if __name__ == '__main__':
    a = int(raw_input())
    b = int(raw_input())
print(a+b)
print(a-b)
print(a*b)

#Python If-Else
#!/bin/python

import math
import os
import random
import re
import sys



if __name__ == '__main__':
    n = int(raw_input().strip())
if n%2!=0:
    print("Weird")
elif n%2==0 and n>=2 and n<=5:
    print("Not Weird")
elif n%2==0 and n>=6 and n<=20:
    print("Weird")
elif n%2==0 and n>20:
    print("Not Weird")

#Say "Hello, World!" With Python
print ("Hello, World!")
