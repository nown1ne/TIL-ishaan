# Insertion Sort:

## **Iterative Approach:**

1.  Select an element in each iteration from the unsorted array(using a loop).
2.  Place it in its corresponding position in the sorted part and shift the remaining elements accordingly (using an inner loop and swapping).
3.  The "inner while loop" basically shifts the elements using swapping.

## Iterative Code:
```c++
void insertion_sort(int arr[], int n) {
    for (int i = 0; i <= n - 1; i++) {
        int j = i;
        while (j > 0 && arr[j - 1] > arr[j]) {
            int temp = arr[j - 1];
            arr[j - 1] = arr[j];
            arr[j] = temp;
            j--;
        }
    }

    cout << "After Using insertion sort: " << "\n";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << "\n";
}
```

- **Time complexity: O(N2)**
- **Space Complexity: O(1)**


## **Recursive Approach**: 

In the iterative method, we did the following:

-   Take an element from the unsorted array(using an outer loop).
-   Place it in its corresponding position in the sorted part(using an inner loop).
-   Shift the remaining elements accordingly.

Now, in the recursive approach, we will just select the element recursively instead of using any loop. This is the only change we will do the recursive insertion sort algorithm and the rest of the part will be completely the same as it was in the case of iterative insertion sort.

The approach will be the following:

1.  First, call the recursive function with the given array, the size of the array, and the index of the selected element(**let's say i**).
2.  Inside that recursive function, take the element at index i from the unsorted array.
3.  Then, place the element in its corresponding position in the sorted part(using swapping).
4.  After that, Shift the remaining elements accordingly.
5.  Finally, call the recursion increasing the index(i) by 1.
6.  The recursion will continue until the index reaches n(i.e. All the elements are covered).\
    **Base Case:** if(i == n) return;
    
 ## Recursive Code:
```c++
void insertion_sort(int arr[], int i, int n) {

    // Base Case: i == n.
    if (i == n) return;

    int j = i;
    while (j > 0 && arr[j - 1] > arr[j]) {
        int temp = arr[j - 1];
        arr[j - 1] = arr[j];
        arr[j] = temp;
        j--;
    }

    insertion_sort(arr, i + 1, n);
}
```

- **Time complexity: O(N2)**
- **Space Complexity: O(N)[auxiliary stack space]**
