# python-4
code--1

'''write a program to read a character untill * is entered .
count the number of uppercase,lowercase ,and numbers entered by user'''

ch=input("enter any character:")
n=u=l=0
if ch>='0' and ch<='9':
    n+=1
elif ch>='a' and ch<='z':
    l+=1
elif ch>='A' and ch<='Z':
    u+=1
while ch!='*':
    ch=input("Enter any character:")
    if ch>='0' and ch<='9':
        n+=1
    elif ch>='a' and ch<='z':
        l+=1
    elif ch>='A' and ch<='Z':
        u+=1
print("lower case characters:",l)
print("upper case characters:",u)
print("number characters:",n)

output:
"""
enter any character: V
Enter any character: L
Enter any character: b
Enter any character: r
Enter any character: 4
Enter any character: 8
Enter any character: 0
Enter any character: *
lower case characters: 2
upper case characters: 2
number characters: 3 """


##for loop 
code--2
#simple for loop (string)
str='Cheetah'
for i in str:
    print(i,end=" ")
out:: C h e e t a h

code--3
#list of string 
s=['cat','dog','fish']
for pet in s:
    print(pet)
output::
cat
dog
fish


#range
code--4
#for with-in range
n=int(input("enter the value of n"))
for i in range(1,n+1):
    print(i,end=' ')
for i in range(n,0,-2):
    print(i,end=' ')

c0de--5
''' code for multiplication Table of n, where n is entered by the user 
input:
 enter any number:2
 output:
 multiplication table of 2
 ********************
 2*0=0
 2*1=2
 .
 .
 2*10=20

 '''
n =int(input("enter any number:"))
e=int(input("enter any number"))
print("Multiplcation table of",n)
print("*********************")
for i in range(0,e+1,1):
    print(f"{n}*{i}={n*i}")


 another code for multiplication::::
 n=int(input("Enter any number:"))
print("Multiplication table of",n)
print("**************************")
for i in range(1,11):
    print(n,'X',i,'=',n*i)


code--6
#program to display the all leap years from 1900,2101
st=int(input("enter the starting year:"))
ed=int(input("Enter the ending year:"))
for i in range(st,ed+1):
    if i%4==0:
        print(i,end=' ')


output:::
enter the starting year: 1900
Enter the ending year: 2101
1900 1904 1908 1912 1916 1920 1924 1928 1932 1936 1940 1944 1948 1952 1956 1960 1964 1968 1972 1976 1980 1984 1988 1992 1996 2000 2004 2008 2012 2016 2020 2024 2028 2032 2036 2040 2044 2048 2052 2056 2060 2064 2068 2072 2076 2080 2084 2088 2092 2096 2100 

code--7
#sum of  1+1/2^2+1/3^2+........+1/n^2
n=int(input("Enter the value of n:"))
s=0
for i in range(1,n+1):
    a=1/(i**2)
    s=s+a
print(s)
 output::
 Enter the value of n: 5
1.4636111111111112

code--8
# sum of 1/2+2/3+......+n/n+1
n=int(input("Enter the value of n:"))
s=0
for i in range(1,n+1):
    a=i/(i+1)
    s=s+a
print(s)
output::
Enter the value of n: 2
1.1666666666666665



code--9
'''
generatring a calender manually
'''
sday=int(input("enter a start day of the month(1-7):"))
numday=int(input("enter the number of days"))
print(" Sun  Mon  Tue  Wed  Thur  Fri  Sat")
print("----------------------------------")
for i in range(sday-1):
    print(end="      ")
i=sday-1
for j in range(1,numday+1):
    if i>6:
        print()
        i=1
    else:
        i+=1
    print(str(j)+" ",end='  ')

output::

enter a start day of the month(1-7): 5
enter the number of days 31
Sun  Mon  Tue  Wed  Thur  Fri  Sat
----------------------------------
                     1    2   3   
 4    5    6    7    8    9    10   
 11   12   13   14   15   16   17   
 18   19   20   21   22   23   24   
 25   26   27   28   29   30   31   

 code--11
 #calender
 import calendar
year=int(input("Enter year:"))
month=int(input("Enter month:"))
cal=calendar.month(year,month)
print(cal)
 
 output::
Enter year: 2023
Enter month: 11
   November 2023
Mo Tu We Th Fr Sa Su
       1  2  3  4  5
 6  7  8  9 10 11 12
13 14 15 16 17 18 19
20 21 22 23 24 25 26
27 28 29 30


code--12
#calender start day for days
mdays=31
sday=1
print(" Su  Mo  Tu  We  Thu  Fr  Sa ")
for _ in range(sday):
    print("   ",end=' ')
for days in range(1, mdays+1):
    print(f"{days: >3}",end=' ')
    if(sday+days) %7==0:
        print()
output::
Su  Mo  Tu  We  Thu  Fr  Sa 
      1   2   3   4   5   6 
  7   8   9  10  11  12  13 
 14  15  16  17  18  19  20 
 21  22  23  24  25  26  27 
 28  29  30  31 
