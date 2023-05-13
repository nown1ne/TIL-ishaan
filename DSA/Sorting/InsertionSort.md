# Insertion Sort:

**Approach:**

1.  Select an element in each iteration from the unsorted array(using a loop).
2.  Place it in its corresponding position in the sorted part and shift the remaining elements accordingly (using an inner loop and swapping).
3.  The "inner while loop" basically shifts the elements using swapping.

## Code:
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
