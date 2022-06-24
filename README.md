# SCHEME
A python interpreter for the coding language SCHEME  
<h3 id="running-the-interpreter">Running the interpreter</h3>


<p>To start an interactive Scheme interpreter session, type:</p>

<pre><code>python3 scheme.py</code></pre>

<p>You can use your Scheme interpreter to evaluate the expressions in an input file
by passing the file name as a command-line argument to <code>scheme.py</code>:</p>

<pre><code>python3 scheme.py tests.scm</code></pre>  
<h2 id="interpreter-details">Interpreter details</h2>



<h3 id="scheme-features">Scheme features</h3>


<p><strong>Read-Eval-Print.</strong> The interpreter reads Scheme expressions, evaluates them,
and displays the results.</p>

<pre><code>scm&gt; 2
2
scm&gt; (+ 2 3)
5
scm&gt; ((lambda (x) (* x x)) 5)
25</code></pre>

<p>The starter code for your Scheme interpreter in <code>scheme.py</code> can successfully
evaluate the first expression above, since it consists of a single number. The
second (a call to a built-in procedure) and the third (a computation of 5
factorial) will not work just yet.</p>

<p><strong>Load.</strong> You can load a file by passing in a symbol for the file name.
For example, to load <code>tests.scm</code>, evaluate the following call expression.</p>

<pre><code>scm&gt; (load &#x27;tests)</code></pre>

<p><strong>Symbols.</strong> Various dialects of Scheme are more or less permissive
about identifiers (which serve as symbols and variable names).</p>

<p>Our rule is that:</p>

<blockquote><p>An identifier is a sequence of letters (a-z and A-Z), digits, and characters
in <code>!$%&amp;*/:&lt;=&gt;?@^_~&#x2d;+.</code> that do not form a valid integer or floating-point
numeral.</p></blockquote>

<p>Our version of Scheme is case-insensitive: two identifiers are considered
identical if they match except possibly in the capitalization of letters.
They are internally represented and printed in lower case:</p>

<pre><code>scm&gt; &#x27;Hello
hello</code></pre>
