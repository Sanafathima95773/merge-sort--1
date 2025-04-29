# Ex MERGE SORT

# Date: 
## Aim:
To implement the Merge Sort algorithm to sort a list of numbers entered by the user.
## Algorithm (Step-by-Step)
Step 1:
Take input n from the user — the number of elements to be sorted.

Step 2:
Read n integers from the user and store them in a list inp_arr.

Step 3:
Define a recursive function merge_sort(inp_arr) to perform merge sort:

If the list has more than one element:

Find the middle index.

Divide the list into two halves: L and R.

Recursively call merge_sort(L) and merge_sort(R).

Step 4:
Merge the two sorted halves:

Use three pointers i, j, k for L, R, and inp_arr.

Compare and insert elements in sorted order into inp_arr.

Step 5:
After merging, print the original array and the sorted array.
## Code:
```
def merge_sort(inp_arr):
    if len(inp_arr)>1:
        mid = 0 + len(inp_arr) // 2
        L = inp_arr[:mid]
        R = inp_arr[mid:]
        merge_sort(L)
        merge_sort(R)
        i = j = k =0
        while i <len(L) and j <len(R):
            if L[i] < R[j]:
                inp_arr[k] = L[i]
                i +=1
            else:
                inp_arr[k] = R[j]
                j +=1
            k +=1
        while i <len(L):
            inp_arr[k] = L[i]
            i += 1
            k +=1
        while j < len(R):
            inp_arr[k] = R[j]
            j +=1
            k +=1
    
n = int(input())
inp_arr = []
for i in range(n):
    inp_arr +=[int(input()),]
print("Given array is")
for i in range(n):
    print(inp_arr[i],end=" ")
print("\nSorted array is")
merge_sort(inp_arr)
for i in range(n):
    print(inp_arr[i],end=" ")
```
## Output
![image](https://github.com/user-attachments/assets/55bdc16c-909d-408f-a4d3-603ae5a18218)

## Result:
The code is executed successfully

