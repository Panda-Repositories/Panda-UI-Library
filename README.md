<h1>Panda UI Library Documentation</h1>
<h3><em>By Panda Technologies</em></h3>
<p><a href="http://commonmark.org"><img src="https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg" alt="made-with-Markdown"></a></p>
<p><img src="https://img.shields.io/badge/Made%20With-Lua-blue" alt="Lua"></p>
<p><img src="https://img.shields.io/discord/761754005906653245" alt="Discord"></p>
<p><a href="https://github.com/SkieAdmin/Panda-Respiratory/graphs/commit-activity"><img src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" alt="Maintenance"></a></p>
<hr>
<h3>Load the UI Library</h3>
<pre class="hljs language-lua"><code><span class="hljs-keyword">local</span> library = <span class="hljs-built_in">loadstring</span>(game:HttpGet(<span class="hljs-string">&quot;https://raw.githubusercontent.com/SkieAdmin/Panda-Respiratory/main/Script/Libraries/Core&quot;</span>))()
</code></pre>
<hr>
<h3>Add windows</h3>
<pre class="hljs language-lua"><code><span class="hljs-keyword">local</span> window = library:Window(<span class="hljs-string">&quot;Window&quot;</span>)
</code></pre>
<hr>
<h3>Add button</h3>
<pre class="hljs language-lua"><code><span class="hljs-comment">--example, callback</span>

window:Button(<span class="hljs-string">&quot;Button name&quot;</span>, <span class="hljs-function"><span class="hljs-keyword">function</span><span class="hljs-params">()</span></span>
   <span class="hljs-built_in">print</span>(<span class="hljs-string">&quot;pressed button&quot;</span>)
<span class="hljs-keyword">end</span>)
</code></pre>
<hr>
<h3>Add toggle</h3>
<pre class="hljs language-lua"><code><span class="hljs-comment">--Name of the toggle, default state of the toggle, callback</span>

window:Toggle(<span class="hljs-string">&quot;Example toggle&quot;</span>, <span class="hljs-literal">true</span>, <span class="hljs-function"><span class="hljs-keyword">function</span><span class="hljs-params">(bool)</span></span>
    <span class="hljs-built_in">print</span>(bool) <span class="hljs-comment">-- bool is true or false depending on the state of the toggle</span>
<span class="hljs-keyword">end</span>)
</code></pre>
<h3>Add color picker</h3>
<hr>
<pre class="hljs language-lua"><code><span class="hljs-comment">--Name, default color (set to true to make the default rainbow), callback</span>

window:ColorPicker(<span class="hljs-string">&quot;Color Picker&quot;</span>, Color3.fromRGB(<span class="hljs-number">255</span>, <span class="hljs-number">255</span>, <span class="hljs-number">255</span>), <span class="hljs-function"><span class="hljs-keyword">function</span><span class="hljs-params">(color)</span></span>
   <span class="hljs-built_in">print</span>(color)
<span class="hljs-keyword">end</span>)
</code></pre>
<hr>
<h3>Add slider</h3>
<pre class="hljs language-lua"><code><span class="hljs-comment">--Name of slider, minimum value, maximum value, default value, callback</span>

window:Slider(<span class="hljs-string">&quot;Example Slider&quot;</span>,<span class="hljs-number">0</span>,<span class="hljs-number">100</span>,<span class="hljs-number">20</span>, <span class="hljs-function"><span class="hljs-keyword">function</span><span class="hljs-params">(value)</span></span>
   <span class="hljs-built_in">print</span>(value)
<span class="hljs-keyword">end</span>)
</code></pre>
<hr>
<h3>Add label</h3>
<pre class="hljs language-lua"><code><span class="hljs-comment">-- Text, color: setting color to true will give it a rainbow effect!</span>

window:Label(<span class="hljs-string">&quot;Credits to SkieHacker and Intrer#0421&quot;</span>, Color3.fromRGB(<span class="hljs-number">127</span>, <span class="hljs-number">143</span>, <span class="hljs-number">166</span>))
</code></pre>
<hr>
<h3>Add input box</h3>
<pre class="hljs language-lua"><code><span class="hljs-comment">-- Name, callback</span>

window:Box(<span class="hljs-string">&quot;Walkspeed&quot;</span>, <span class="hljs-function"><span class="hljs-keyword">function</span><span class="hljs-params">(text, focuslost)</span></span>
   <span class="hljs-keyword">if</span> focuslost <span class="hljs-keyword">then</span>
   <span class="hljs-built_in">print</span>(text)
   <span class="hljs-keyword">end</span>
<span class="hljs-keyword">end</span>)
<span class="hljs-comment">-- The callback will be called with two arguments, the text that the player inputted and whether the player has stopped writing</span>
</code></pre>
<hr>
<h3>Add dropdown</h3>
<pre class="hljs language-lua"><code><span class="hljs-comment">-- Name, table with names of the button that you want, callback that will be called with the name of the button that was pressed</span>

<span class="hljs-keyword">local</span> dropdown = window:Dropdown(<span class="hljs-string">&quot;Example dropdown&quot;</span>, {<span class="hljs-string">&quot;Button 1&quot;</span>, <span class="hljs-string">&quot;Button 2&quot;</span>, <span class="hljs-string">&quot;Third button&quot;</span>}, <span class="hljs-function"><span class="hljs-keyword">function</span><span class="hljs-params">(name)</span></span>
   <span class="hljs-built_in">print</span>(name)
<span class="hljs-keyword">end</span>)
</code></pre>
<h4>Add buttons to dropdown</h4>
<pre class="hljs language-lua"><code><span class="hljs-comment">-- Name</span>

dropdown:Button(<span class="hljs-string">&quot;New button&quot;</span>)
</code></pre>
<h4>Remove buttons from dropdown</h4>
<pre class="hljs language-lua"><code><span class="hljs-comment">-- Name</span>

dropdown:Remove(<span class="hljs-string">&quot;Button&quot;</span>)
</code></pre>
<hr>
<h3>Add keybind to UI</h3>
<pre class="hljs language-lua"><code><span class="hljs-comment">-- Key</span>

library:Keybind(<span class="hljs-string">&quot;P&quot;</span>)
</code></pre>
<hr>
<h3>Destroy UI</h3>
<pre class="hljs language-lua"><code>library:Destroy()
</code></pre>
