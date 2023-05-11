# Reverse a number
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
