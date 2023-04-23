Download Link: https://assignmentchef.com/product/solved-assignment-03-recursion-and-practice-with-exceptions-templates-and-the-stl
<br>
<h2><a id="user-content-requirements" class="anchor" href="https://github.com/timferido/assignment-03#requirements" aria-hidden="true"></a>Requirements</h2>

This project is to be done in groups.

You are allowed to write everything in one file this time, so long it is organized and the file is not too long. If the file gets too long, please split it into multiple <code>.h</code> and <code>.cpp</code> files, and have a <code>main.cpp</code> that <code>#include</code>s the <code>.h</code> files, and can be used to call the test functions prototyped in them. I recommend having one pair of <code>.h</code> and <code>.cpp</code> files for Parts 1–3, and another pair for Part 4 (and the challenge, if you choose to take it).

All the files you produce must be able to exist within a single project. You will submit these files via github as normal.

<h3><a id="user-content-part-1" class="anchor" href="https://github.com/timferido/assignment-03#part-1" aria-hidden="true"></a>Part 1</h3>

<ol start="0">

 <li>Read about exceptions (either <a href="http://www.cplusplus.com/doc/tutorial/exceptions/" rel="nofollow">here</a>, or you may find another source).</li>

 <li>Come up with the most interesting (readable) example of using them that you can. This should take an hour or less.</li>

</ol>

<h3><a id="user-content-part-2" class="anchor" href="https://github.com/timferido/assignment-03#part-2" aria-hidden="true"></a>Part 2</h3>

<ol start="0">

 <li>Read about templates (I suggest starting <a href="https://isocpp.org/wiki/faq/templates" rel="nofollow">here</a> and reading till you feel like you’ve read enough).</li>

 <li>Come up with the most interesting (readable) example of using them that you can. This should take an hour or less.</li>

</ol>

<h3><a id="user-content-part-3" class="anchor" href="https://github.com/timferido/assignment-03#part-3" aria-hidden="true"></a>Part 3</h3>

<ol start="0">

 <li>Think about a time when you really wanted a variable length array, or a list that was always sorted, or something similar.</li>

 <li>Read about <code>vector</code>s, <code>set</code>s, and one other STL container that looks interesting to you. <a href="http://en.cppreference.com/w/cpp/container" rel="nofollow">This</a> might be a good place to start, but you may also need to google around a bit.</li>

 <li>Come up with the most interesting (readable) example of using them that you can. This should take an hour or less.</li>

</ol>

<h3><a id="user-content-part-4" class="anchor" href="https://github.com/timferido/assignment-03#part-4" aria-hidden="true"></a>Part 4</h3>

Write definitions for as many of the following functions as you can in roughly 3 hours. Be sure to label the base case and recursive case in each function.

<ul>

 <li><code>int gcd(int a, int b);</code>Returns the greatest common divisor of two integers using Euclid’s algorithm. This function has the following properties:

  <ul>

   <li><code>gcd(a,0)</code> evaluates to <code>abs(a)</code></li>

   <li><code>gcd(a,b)</code> is equivalent to <code>gcd(b,a)</code></li>

   <li><code>gcd(a,b)</code> is equivalent to <code>gcd(abs(a),abs(b))</code></li>

   <li><code>gcd(a,b)</code> is equivalent to <code>gcd(a-b,b)</code> is equivalent to <code>gcd(a,b-a)</code></li>

  </ul>Pseudocode for this function might look like the following:

  <ul>

   <li>Normalize <code>a</code> and <code>b</code> by making them positive</li>

   <li>If <code>a</code> or <code>b</code> is <code>0</code>, return the one that is nonzero</li>

   <li>If <code>a &gt; b</code> return <code>gcd(a-b, b)</code></li>

   <li>Otherwise return <code>gcd(a, b-a)</code></li>

  </ul>where line (2) is the base case, and lines (3) and (4) are the recursive case.</li>

 <li><code>int fib(int n);</code>Returns the <code>n</code>th Fibonacci number. Recall that the Fibonacci sequence is defined as follows:

  <ul>

   <li><code>fib(1)</code> evaluates to <code>1</code></li>

   <li><code>fib(2)</code> evaluates to <code>1</code></li>

   <li><code>fib(n)</code> evaluates to <code>fib(n-1) + fib(n-2)</code></li>

  </ul></li>

 <li><code>int pow(int a, int b);</code>Returns <code>a</code> raised to the <code>b</code>th power (for positive <code>b</code>).</li>

 <li><code>int tri(int n);</code>Returns the <code>n</code>th triangular number. Triangular numbers are, informally<pre><code>1    .     .3   . .     .    . .6  . . .</code></pre>and so on. More formally, the <code>n</code>th triangular number, for <code>n &gt; 0</code>, is the sum of the integers between <code>1</code> and <code>n</code>, inclusive.Note that there is a closed form expression for finding the <code>n</code>th triangular number (and a famous story about Gauss coming up with it, as a child); but for this assignment, please find the answer algorithmically :-).</li>

</ul>

<h3><a id="user-content-part-5" class="anchor" href="https://github.com/timferido/assignment-03#part-5" aria-hidden="true"></a>Part 5</h3>

Rewrite the functions you wrote in Part 4 as iterative functions (append <code>_iter</code> to your name for the recursive version of the function).

<h3><a id="user-content-challenge" class="anchor" href="https://github.com/timferido/assignment-03#challenge" aria-hidden="true"></a>Challenge</h3>

<ul>

 <li><code>std::string int_to_roman(int n);</code>A recursive version of the <code>int_to_roman()</code> function from assignment-01</li>

 <li><code>std::string int_to_words(int n);</code>A recursive function taking in any integer, <code>n</code>, and returning a string containing the English representation of that number. For example, the following code:should produce the following output:<pre><code>0 == zero1 == one-1 == negative one123 == one hundred twenty three123123 == one hundred twenty three thousand one hundred twenty three123000123 == one hundred twenty three million one hundred twenty three123123000 == one hundred twenty three million one hundred twenty three thousand</code></pre>While writing this, remember the use of <code>const</code> arrays in the in-class solution to assignment-01. A similar technique may save you a lot of <code>if ... else</code> statements.Also, if you find it useful, you may modify the function signature slightly.As a general approach to solving this problem, I would recommend starting by writing a function that can correctly handle all the numbers from 1–999, then extending it to handle all possible numbers by splitting the original number into groups of 3 digits, recursively passing these smaller groups to itself, and appending the correct suffix (e.g. “thousand”) to each group.</li>

 <li><code>std::string magic_number(int n);</code>Ponder this:<pre><code>1 is 33 is 55 is 44 is the magic number!7 is 55 is 44 is the magic number!13 is 88 is 55 is 44 is the magic number!</code></pre>Why is 4 the magic number? Is 4 always the magic number?Once you figure it out, write a recursive function that generates the above example given the following:</li>

</ul>

<h2><a id="user-content-requests" class="anchor" href="https://github.com/timferido/assignment-03#requests" aria-hidden="true"></a>Requests</h2>

(None)

<h2><a id="user-content-assumptions" class="anchor" href="https://github.com/timferido/assignment-03#assumptions" aria-hidden="true"></a>Assumptions</h2>

(None)

<h2><a id="user-content-style" class="anchor" href="https://github.com/timferido/assignment-03#style" aria-hidden="true"></a>Style</h2>

<ul>

 <li>Place your solution in a <code>solution--YOURNAME</code> subdirectory (where <code>YOURNAME</code> is your GitHub username).</li>

 <li>Include your copyright and license information at the top of every file, followed by a brief description of the file’s contents, e.g.</li>

 <li>Use “include guards” in all <code>.h</code> files. Be sure to give the preprocessor variable a name corresponding to the file name. For example, in <code>point.h</code>:</li>

 <li><code>main()</code> must have its own <code>.cpp</code> file. I suggest calling it <code>main.cpp</code>.</li>

 <li>Classes must have both <code>.h</code> and <code>.cpp</code> files, with member functions defined in the <code>.cpp</code> files unless they are truly trivial. If it makes sense, you may put multiple classes into one pair of <code>.h</code> and <code>.cpp</code> files.</li>

 <li>Declare member functions and function arguments as <code>const</code> when appropriate (in general, whenever possible).</li>

 <li>Document and format your code well and consistently. Be sure to clearly document the source of any code, algorithm, information, etc. that you use or reference while completing your work.</li>

 <li>Wrap lines at 79 or 80 columns whenever possible.</li>

 <li>End your file with a blank line.</li>

 <li>Do <em>not</em> use <code>using namespace std;</code>. You may get around typing <code>std::</code> in front of things or with, e.g., <code>using std::cout;</code>.</li>

</ul>

5/5 - (1 vote)

<pre>  cout &lt;&lt; <span class="pl-c1">0</span> &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span> == <span class="pl-pds">"</span></span> &lt;&lt; int_to_words(<span class="pl-c1">0</span>) &lt;&lt; endl;  cout &lt;&lt; <span class="pl-c1">1</span> &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span> == <span class="pl-pds">"</span></span> &lt;&lt; int_to_words(<span class="pl-c1">1</span>) &lt;&lt; endl;  cout &lt;&lt; -<span class="pl-c1">1</span> &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span> == <span class="pl-pds">"</span></span> &lt;&lt; int_to_words(-<span class="pl-c1">1</span>) &lt;&lt; endl;  cout &lt;&lt; <span class="pl-c1">123</span> &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span> == <span class="pl-pds">"</span></span> &lt;&lt; int_to_words(<span class="pl-c1">123</span>) &lt;&lt; endl;  cout &lt;&lt; <span class="pl-c1">123123</span> &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span> == <span class="pl-pds">"</span></span> &lt;&lt; int_to_words(<span class="pl-c1">123123</span>) &lt;&lt; endl;  cout &lt;&lt; <span class="pl-c1">123000123</span> &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span> == <span class="pl-pds">"</span></span> &lt;&lt; int_to_words(<span class="pl-c1">123000123</span>) &lt;&lt; endl;  cout &lt;&lt; <span class="pl-c1">123123000</span> &lt;&lt; <span class="pl-s"><span class="pl-pds">"</span> == <span class="pl-pds">"</span></span> &lt;&lt; int_to_words(<span class="pl-c1">123123000</span>) &lt;&lt; endl;</pre>

<pre>cout &lt;&lt; magic_number(<span class="pl-c1">1</span>) &lt;&lt; endl;cout &lt;&lt; magic_number(<span class="pl-c1">7</span>) &lt;&lt; endl;cout &lt;&lt; magic_number(<span class="pl-c1">13</span>) &lt;&lt; endl;</pre>

<pre><span class="pl-c">/* ----------------------------------------------------------------------------</span><span class="pl-c"> * Copyright &amp;copy; 2016 Ben Blazak &lt;<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="98fafaf4f9e2f9f3d8feedf4f4fdeaecf7f6b6fdfced">[email protected]</a>&gt;</span><span class="pl-c"> * Released under the [MIT License] (http://opensource.org/licenses/MIT)</span><span class="pl-c"> * ------------------------------------------------------------------------- */</span><span class="pl-c">/**</span><span class="pl-c"> * A short program to print "Hello World!" to standard output.</span><span class="pl-c"> */</span></pre>