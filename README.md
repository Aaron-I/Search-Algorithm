# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
# i)Use a linear search method to match the item in a list.
# Developed by:AARON I
# RegisterNumber: 23002289
```
def linearSearch():
   array = eval(input())
   k = eval(input()) 
   n=len(array)
   array.sort()
   x=0
   for i in array:
      if i==k:
         index=x
         print(array)
         print("Element found at index: ",index)
         break
      x+=1
   else:
      print(array)
      print("Element not found")
linearSearch()
```
# ii) Find the element in a list using Binary Search(Iterative Method).
# Developed by:AARON I
# RegisterNumber: 23002289
```
array=eval(input())
k=eval(input())
low=0
high=len(array)-1
array.sort()
print(array)
while low<=high:
    mid=low+(high-low)//2
    if array[mid]==k:
        print("Element found at index: ",mid)
        break
    elif array[mid]>k:
        high=mid-1
    else:
        low=mid+1
else:
    print("Element not found")
```
# iii)Find the element in a list using Binary Search (recursive Method).
# Developed by: AARON I
# RegisterNumber: 23002289
```
def binarySearch(array,k,low,high): 
    mid=low+(high-low)//2
    if low<=high:
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
            return binarySearch(array,k,low,high)
        else: 
            high=mid-1
            return binarySearch(array,k,low,high)
    else:
        return -1
array=eval(input())
array.sort()
print(array)
k=eval(input())
n=len(array)
x=binarySearch(array,k,0,n-1)
if x<0:
    print("Element not found")
else:
    print("Element found at index: ",x)
```
##Output:
![output](/Screenshot%202023-07-26%20205114.png)
![output](/Screenshot%202023-07-26%20205337.png)
![output](/Screenshot%202023-07-26%20205552.png)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
