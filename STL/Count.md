The count() function returns the number of occurrences of an element in a given range. 
Returns the number of elements in the range [first, last) that compare equal to val.
<br>
If the val is not found at any occurrence then it returns 0(Integer value).
<h3>Syntax</h3>
<code>int count(Iterator first, Iterator last, T &val)</code>
<ul>
<li>first, last : Input iterators to the initial and final positions of the sequence of elements.</li>
<li>val : Value to match</li>
</ul>

<h3>Example:</h3>
<code>for (auto const &s: sentences) {</code><br>
    <code>int n = count(s.begin(), s.end(), ' ');</code><br>
    <code>res = max(res, n + 1);</code><br>
<code>}</code>