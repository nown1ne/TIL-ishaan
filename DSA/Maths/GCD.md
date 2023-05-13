# GCD/HCF (Greatest common Denominator)
**Problem Statement:** Find gcd of two numbers.

**Intuition:** Gcd is the greatest number which is divided by both a and b.If a number is divided by both a and b, it is should be divided by (a-b) and b as well.

## Approach (Euclidean’s theorem.):
-   Recursively call gcd(b,a%b) function till the base condition is hit.
-   b==0 is the base condition.When base condition is hit return a,as gcd(a,0) is equal to a.

```c++
int gcd(int a, int b) {
	if (b == 0) {
		return a;
	}
	return gcd(b, a % b);
}
```
- Time Complexity: O(logɸmin(a,b)), where ɸ is 1.61.

- Space Complexity: O(1).

