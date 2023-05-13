# Check if a number is prime or not
**Problem Statement:** Given a number, check whether it is prime or not

## Approach :
Running the for loop till the square root of the number
```c++
bool isPrime(int N) {
  for (int i = 2; i < sqrt(N); i++) {
    if (N % i == 0) {
      return false;
    }
  }
  return true;
}
```
- Space Optimisation: O(√n)
- Time Optimization: O(1)
