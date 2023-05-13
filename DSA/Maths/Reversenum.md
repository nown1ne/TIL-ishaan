# Reverse a number

**Problem Statement:** Given an integer N , write program to Reverse a Number.
```reason
int num = N;
int reverse = 0;
    while(N!=0)
    {
        int digit = N%10;
        reverse = reverse*10+digit;
        N = N/10;
    }
```

### Space Optimisation: O(n)
### Time Optimization: O(1)

## Questions Extension -> Check if palindrome
```c++
if(num == reversenum) return true;
else return false;
```
