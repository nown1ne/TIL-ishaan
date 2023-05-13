# Bubble Sort:

**Approach:**

The algorithm steps are as follows:

1.  First, we will select the range of the unsorted array. For that, we will run a loop(say i) that will signify the last index of the selected range. The loop will run backward from index n-1 to 0(where n = size of the array). The value i = n-1 means the range is from 0 to n-1, and similarly, i = n-2 means the range is from 0 to n-2, and so on.
2.  Within the loop, we will run another loop(say j, runs from 0 to i-1 though the range is from 0 to i) to push the maximum element to the last index of the selected range, by repeatedly swapping adjacent elements.\
    Basically, we will swap adjacent elements(**if arr[j] > arr[j+1]**) until the maximum element of the range reaches the end.
3.  Thus, after each iteration, the last part of the array will become sorted. Like: after the first iteration, the array up to the last index will be sorted, and after the second iteration, the array up to the second last index will be sorted, and so on.
4.  After (n-1) iteration, the whole array will be sorted.

**Note: ***Here, after each iteration, the array becomes sorted up to the last index of the range. That is why the last index of the range decreases by 1 after each iteration. This decrement is achieved by the outer loop and the last index is represented by variable ****i**** in the following code. And the inner loop(****i.e. j****) helps to push the maximum element of range [0....i] to the last index(i.e. index i)

## DRY RUN:
**Iteration 1**
![pasted image 0-2](https://github.com/IshaanAdarsh/TIL/assets/100434702/f0fc57d1-8d1d-4b31-b0ea-f75d626eeee3)

**Iteration 2**
![pasted image 0](https://github.com/IshaanAdarsh/TIL/assets/100434702/10ac7483-9f79-41ea-ad95-b69d7cd73066)

## Code:
```c++
void bubble_sort(int arr[], int n) {
    // bubble sort
    for (int i = n - 1; i >= 0; i--) {
        for (int j = 0; j <= i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j + 1];
                arr[j + 1] = arr[j];
                arr[j] = temp;
            }
        }
    }

    cout << "After Using bubble sort: " << "\n";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << "\n";
}
```

- **Time complexity: O(N2)**
- **Space Complexity: O(1)**
