The accumulate function adds up every element of a vector when used from beginning to end.
I used this along with iterating through each element of the vector of customers.
<h3>Syntax:</h3>
<code>accumulate(first, last, sum, myfun);</code>
<p>Parameters:</p>
<ul>
<li>first, last: first and last elements of range whose elements are to be added</li>
<li>sum:  initial value of the sum</li>
<li>myfun: a function for performing any specific task.</li>
</ul>
<h3>Example:</h3>
<code> for(auto customer: accounts){</code><br>
            <code>int wealth =accumulate(customer.begin(),customer.end(),0);</code><br>    
            <code>if(wealth>wealthiest) wealthiest = wealth;}</code><br>
