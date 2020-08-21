---


---

<h1 id="booker-mvp-api-summary-a-id0a">Booker MVP API Summary <a id="0"></a></h1>
<h2 id="table-of-contents">Table of Contents</h2>
<ol>
<li>
<p>POST <a href="#auth-signup">/auth/signup</a></p>
</li>
<li>
<p>POST <a href="#auth-login">/auth/login</a></p>
</li>
<li>
<p>POST <a href="#books-search">/books/search</a></p>
</li>
<li>
<p>POST <a href="#onboard">/onboard</a></p>
</li>
</ol>
<hr>
<hr>
<h2 id="post-authsignup-a-idauth-signupa">POST /auth/signup <a id="auth-signup"></a></h2>
<h3 id="request-payload---">– request payload –</h3>
<pre><code>
username: String

email: String

password: String

</code></pre>
<h3 id="valid-response-payload---">– valid response payload –</h3>
<pre><code>
token: String

</code></pre>
<h3 id="token-payload---">– token payload –</h3>
<pre><code>
username: String

</code></pre>
<h3 id="summary">Summary:</h3>
<ul>
<li>
<p>Encrypt the password</p>
</li>
<li>
<p>Create a new document in the <code>users</code> collection</p>
</li>
<li>
<p>Generate a JWT and return it to the client</p>
</li>
</ul>
<h3 id="error-handling">Error handling</h3>
<ul>
<li><em>needs documentation</em></li>
</ul>
<p><a href="#0">#top</a></p>
<hr>
<h2 id="post-authlogin-a-idauth-logina">POST /auth/login <a id="auth-login"></a></h2>
<h3 id="request-payload----1">– request payload –</h3>
<pre><code>
username: String

password: String

</code></pre>
<h3 id="response-payload---">– response payload –</h3>
<pre><code>
token: String

</code></pre>
<h3 id="token-payload----1">– token payload –</h3>
<pre><code>
username: String

</code></pre>
<h3 id="summary-1">Summary</h3>
<ul>
<li>
<p>Compare the passwords</p>
</li>
<li>
<p>Generate a JWT and return it to the client</p>
</li>
</ul>
<h3 id="error-handling-1">Error handling</h3>
<ul>
<li><em>needs documentation</em></li>
</ul>
<p><a href="#0">#top</a></p>
<hr>
<h2 id="post-bookssearch-a-idbooks-searcha">POST /books/search <a id="books-search"></a></h2>
<h3 id="request-payload----2">– request payload –</h3>
<pre><code>
inAuthor?: String

inTitle?: String

subject?: String

isbn?: String

</code></pre>
<h3 id="response-payload----1">– response payload –</h3>
<pre><code>
books: [

thumbnail: String

title: String

author: String

volumeId: String

]

</code></pre>
<h3 id="summary-2">Summary</h3>
<ul>
<li>
<p>Pass the inputs to Google Books <code>/volumes/q={search}</code></p>
</li>
<li>
<p>Return a list of recognized books</p>
</li>
<li>
<p>The request must contain at least one field</p>
</li>
<li>
<p>Each request happens 1/3 of a second after a user stops typing</p>
</li>
</ul>
<h3 id="error-handling-2">Error Handling</h3>
<ul>
<li><em>needs documentation</em></li>
</ul>
<p><a href="#0">#top</a></p>
<hr>
<h2 id="post-onboard-a-idonboarda">POST /onboard <a id="onboard"></a></h2>
<h3 id="request-payload----3">– request payload –</h3>
<pre><code>
token: String

books: [

volumeId: String

critique: String

]

</code></pre>
<h3 id="summary-3">Summary</h3>
<ul>
<li>
<p>Pass the <code>volumeId</code>s to Google Books <code>/volumes/volumeId</code></p>
</li>
<li>
<p>Create <code>book</code> documents in the <code>books</code> collection for each book entity</p>
</li>
<li>
<p>Associate the user’s critique with the book</p>
</li>
</ul>
<h3 id="error-handling-3">Error Handling</h3>
<ul>
<li><em>needs documentation</em></li>
</ul>
<p><a href="#0">#top</a></p>
<hr>
<h2 id="post-copy_this-a-idcopy-thisa">POST /copy_this <a id="copy-this"></a></h2>
<h3 id="request-payload----4">– request payload –</h3>
<pre><code>
</code></pre>
<h3 id="response-payload----2">– response payload –</h3>
<pre><code>
</code></pre>
<h3 id="summary-4">Summary</h3>
<ul>
<li><em>needs documentation</em></li>
</ul>
<h3 id="error-handling-4">Error Handling</h3>
<ul>
<li><em>needs documentation</em></li>
</ul>
<p><a href="#0">#top</a></p>

