# Count digits in a number
**Problem Statement:** Given an integer N , write program to count number of digits in N.


## Approach 1 (Divide and Count):
```reason
int count_digits( int n )
{
   int x = n; int count =0;
   while( x !=0 ) 
   {
       x = x / 10;
       count++;
   }
   return count;
}
```
- Space Optimisation: O(n)
- Time Optimization: O(1)

## Approach 2 (Using String STL):
Convert the integer into a string then find the length of the string.
```reason
int count_digits( int n )
{
  string x = to_string(n);
  return x.length(); 
}
```
- Space Optimisation: O(1)
- Time Optimization: O(1)

## Approach 3 (Using Logarithm Function): 
The number of digits in an integer = the upper bound of log10(n).
```reason
int count_digits( int n )
{
  int digits = floor(log10(n) + 1);
  return digits;
}
```
- Space Optimisation: O(1)
- Time Optimization: O(1)
