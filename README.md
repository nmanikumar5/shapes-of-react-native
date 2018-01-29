# shapes-of-react-native

<div class="content">
	
<p>After drawing a bit of inspiration from <a href="http://enjoycss.com/gallery/shapes">ENJOY CSS Shapes</a> We decided to see if I could remake some of these shapes with a subset of css.


<p>Of course we have to access <code>react-design</code> here so drawing shapes is pretty mush easy but my way is to see if I can just use normal <code>Views</code> and to get all the shapes in React</p>

<p> Added some of the shapes but got crazy! But most of the shapes are did :-)</p>


<p><img src="http://i.imgur.com/cWR7FKh.gif" title="What am doing with my life" ></p>

<!-- more -->


<!--<h2>Live Code <a href="https://rnplay.org/apps/58FEmw">https://rnplay.org/apps/58FEmw</a></h2>-->

<h1>Key Takeaways</h1>

<ul>
<li>I wish border-radius worked a little more like the web</li>
<li>Box Shadow would be nice to have as well.</li>
<li>Skew transform would be a nice to have.</li>
<li>Just use SVGs&hellip;</li>
</ul>


<h1>Shapes</h1>

<h3>Square</h3>

<p>Pretty simple&hellip;</p>

<p><img src="http://i.imgur.com/yNqQt2q.png" title="Yeah what were you expecting" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Square = React.createClass({
</span><span class='line'>    render: function() {
</span><span class='line'>        return (
</span><span class='line'>            &lt;View style={styles.square} /&gt;
</span><span class='line'>        )
</span><span class='line'>    }
</span><span class='line'>});
</span><span class='line'>
</span><span class='line'>square: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100,
</span><span class='line'>    backgroundColor: 'red'
</span><span class='line'>}
</span></code></pre></td></tr></table></div></figure>


<h3>Rectangle</h3>

<p>Nothing too crazy here either</p>

<p><img src="http://i.imgur.com/Eiw8qTZ.png" title="It is a longer square" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Rectangle = React.createClass({
</span><span class='line'>    render: function() {
</span><span class='line'>        return (
</span><span class='line'>            &lt;View style={styles.rectangle} /&gt;
</span><span class='line'>        )
</span><span class='line'>    }
</span><span class='line'>});
</span><span class='line'>
</span><span class='line'>rectangle: {
</span><span class='line'>    width: 100 * 2,
</span><span class='line'>    height: 100,
</span><span class='line'>    backgroundColor: 'red'
</span><span class='line'>}
</span></code></pre></td></tr></table></div></figure>


<h3>Circle</h3>

<p>One note to mention about border radius is that it doesn&rsquo;t work like the web. So if you go more than 50% you&rsquo;ll start forming a weird diamondy shape.</p>

<p><img src="http://i.imgur.com/Monc4Mx.png" title="The circle was invented in 1925" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Circle = React.createClass({
</span><span class='line'>    render: function() {
</span><span class='line'>        return (
</span><span class='line'>            &lt;View style={styles.circle} /&gt;
</span><span class='line'>        )
</span><span class='line'>    }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>circle: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100,
</span><span class='line'>    borderRadius: 100/2,
</span><span class='line'>    backgroundColor: 'red'
</span><span class='line'>}
</span></code></pre></td></tr></table></div></figure>


<!--
var HalfCircle = React.createClass({
render: function() {
return (
<view style="{[styles.halfCircle," this.props.style]}=""/>
)
}
})
halfCircle: {
height:25,
width:50,
backgroundColor:'red',
borderTopLeftRadius:27.5,
borderTopRightRadius:27.5,
}
-->

<h3>Oval</h3>

<p>Border radius wasn&rsquo;t working, lets just do a circle and scale it&hellip;</p>

<p><img src="http://i.imgur.com/pHxlyNn.png" title="Not a circle" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var Oval = React.createClass({
</span><span class='line'>    render: function() {
</span><span class='line'>        return (
</span><span class='line'>            &lt;View style={styles.oval} /&gt;
</span><span class='line'>        )
</span><span class='line'>    }
</span><span class='line'>});
</span><span class='line'>
</span><span class='line'>  oval: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100,
</span><span class='line'>    borderRadius: 50,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    transform: [
</span><span class='line'>      {scaleX: 2}
</span><span class='line'>    ]
</span><span class='line'>  },</span></code></pre></td></tr></table></div></figure>


<h3>Triangle Up</h3>

<p>CSS border triangles still work in React Native.</p>

<p><img src="http://i.imgur.com/cejjWpe.png" title="Pyramid in 2d" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Triangle = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={[styles.triangle, this.props.style]} /&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  triangle: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    backgroundColor: 'transparent',
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderBottomWidth: 100,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderBottomColor: 'red'
</span><span class='line'>  }
</span></code></pre></td></tr></table></div></figure>


<p>Here we get to cheat a bit. You could do this on the web too, but rather than adjust the borders we&rsquo;ll just rotate it.</p>

<h3>Triangle Down</h3>

<p><img src="http://i.imgur.com/gwJ9EdU.png" title="Rotate" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TriangleDown = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;Triangle style={styles.triangleDown}/&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>
</span><span class='line'>  triangleDown: {
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '180deg'}
</span><span class='line'>    ]
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Triangle Left</h3>

<p><img src="http://i.imgur.com/SlY2Bvf.png" title="Rotate" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TriangleLeft = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;Triangle style={styles.triangleLeft}/&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  triangleLeft: {
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '-90deg'}
</span><span class='line'>    ]
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Triangle Right</h3>

<p><img src="http://i.imgur.com/UTFvVL6.png" title="Konami Code" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var TriangleRight = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;Triangle style={styles.triangleRight}/&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  triangleRight: {
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '90deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span></code></pre></td></tr></table></div></figure>


<p>Again we&rsquo;ll cheat here and go for the rotation!</p>

<h3>Triangle Top Left</h3>

<p><img src="http://i.imgur.com/aToWUAu.png" title="Pythagorean theory" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TriangleCorner = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={[styles.triangleCorner, this.props.style]} /&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>});
</span><span class='line'>
</span><span class='line'>  triangleCorner: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    backgroundColor: 'transparent',
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderRightWidth: 100,
</span><span class='line'>    borderTopWidth: 100,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderTopColor: 'red'
</span><span class='line'>  },
</span></code></pre></td></tr></table></div></figure>


<h3>Triangle Top Right</h3>

<p><img src="http://i.imgur.com/Ei1GaY4.png" title="sohcahtoa" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TriangleCornerTopRight = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;TriangleCorner style={styles.triangleCornerTopRight}/&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>triangleCornerTopRight: {
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '90deg'}
</span><span class='line'>    ]
</span><span class='line'>}
</span></code></pre></td></tr></table></div></figure>


<h3>Triangle Bottom Left</h3>

<p><img src="http://i.imgur.com/tDtSN8B.png" title="ninety degree angle" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TriangleCornerBottomLeft = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;TriangleCorner style={styles.triangleCornerBottomLeft}/&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  triangleCornerBottomLeft: {
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '270deg'}
</span><span class='line'>    ]
</span><span class='line'>  },</span></code></pre></td></tr></table></div></figure>


<h3>Triangle Bottom Right</h3>

<p><img src="http://i.imgur.com/JbnkwkK.png" title="sick ramp bro" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TriangleCornerBottomRight = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;TriangleCorner style={styles.triangleCornerBottomRight}/&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  triangleCornerBottomRight: {
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '180deg'}
</span><span class='line'>    ]
</span><span class='line'>  }
</span></code></pre></td></tr></table></div></figure>


<h3>Curved Tail Arrow</h3>

<p>Well we don&rsquo;t have the ability to do pseudo elements but they were just hacks anyway so we&rsquo;ll just create a wrapping <code>View</code> with 2 elements and style them.
Now this is not exactly the same, and it&rsquo;s partially due to the way <code>border-radius</code> are managed in react-native vs the web but it&rsquo;s closeish.</p>

<p><img src="http://i.imgur.com/Y2IEMxh.png" title="Just use an image" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
<span class='line-number'>47</span>
<span class='line-number'>48</span>
<span class='line-number'>49</span>
<span class='line-number'>50</span>
<span class='line-number'>51</span>
<span class='line-number'>52</span>
<span class='line-number'>53</span>
<span class='line-number'>54</span>
<span class='line-number'>55</span>
<span class='line-number'>56</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var CurvedTailArrow = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.curvedTailArrow}&gt;
</span><span class='line'>        &lt;View style={styles.curvedTailArrowTail} /&gt;
</span><span class='line'>        &lt;View style={styles.curvedTailArrowTriangle} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  curvedTailArrow: {
</span><span class='line'>    backgroundColor: 'transparent',
</span><span class='line'>    overflow: 'visible',
</span><span class='line'>    width: 30,
</span><span class='line'>    height: 25
</span><span class='line'>  },
</span><span class='line'>  curvedTailArrowTriangle: {
</span><span class='line'>    backgroundColor: 'transparent',
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopWidth: 9,
</span><span class='line'>    borderTopColor: 'transparent',
</span><span class='line'>    borderRightWidth: 9,
</span><span class='line'>    borderRightColor: 'red',
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '10deg'}
</span><span class='line'>    ],
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    bottom: 9,
</span><span class='line'>    right: 3,
</span><span class='line'>    overflow: 'visible'
</span><span class='line'>  },
</span><span class='line'>  curvedTailArrowTail: {
</span><span class='line'>    backgroundColor: 'transparent',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    borderBottomColor: 'transparent',
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderBottomWidth: 0,
</span><span class='line'>    borderLeftWidth: 0,
</span><span class='line'>    borderRightWidth: 0,
</span><span class='line'>    borderTopWidth: 3,
</span><span class='line'>    borderTopColor: 'red',
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderTopLeftRadius: 12,
</span><span class='line'>    top: 1,
</span><span class='line'>    left: 0,
</span><span class='line'>    width: 20,
</span><span class='line'>    height: 20,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '45deg'}
</span><span class='line'>    ]
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Trapezoid</h3>

<p>The difference with this one is we had to double our width. Why? I don&rsquo;t know.</p>

<p><img src="http://i.imgur.com/Mu3NLyN.png" title="Trapezoid" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Trapezoid = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.trapezoid} /&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  trapezoid: {
</span><span class='line'>    width: 200,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderBottomWidth: 100,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderStyle: 'solid'
</span><span class='line'>  } </span></code></pre></td></tr></table></div></figure>


<h3>Parallelogram</h3>

<p>If only we had skew. :(
Luckily we have the triangles we created earlier.</p>

<p><img src="http://i.imgur.com/AtXb6rq.png" title="Dont try this at home" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var Parallelogram = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.parallelogram}&gt;
</span><span class='line'>        &lt;TriangleUp style={styles.parallelogramRight} /&gt;
</span><span class='line'>        &lt;View style={styles.parallelogramInner} /&gt;
</span><span class='line'>        &lt;TriangleDown style={styles.parallelogramLeft} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>
</span><span class='line'>  parallelogram: {
</span><span class='line'>    width: 150,
</span><span class='line'>    height: 100
</span><span class='line'>  },
</span><span class='line'>  parallelogramInner: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    left: 0,
</span><span class='line'>    top: 0,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    width: 150,
</span><span class='line'>    height: 100,
</span><span class='line'>  },
</span><span class='line'>  parallelogramRight: {
</span><span class='line'>    top: 0,
</span><span class='line'>    right: -50,
</span><span class='line'>    position: 'absolute'
</span><span class='line'>  },
</span><span class='line'>  parallelogramLeft: {
</span><span class='line'>    top: 0,
</span><span class='line'>    left: -50,
</span><span class='line'>    position: 'absolute'
</span><span class='line'>  }
</span></code></pre></td></tr></table></div></figure>


<h3>Star (6-points)</h3>

<p>These Triangles sure are coming in handy.</p>

<p><img src="http://i.imgur.com/XEPeWjV.png" title="This is really ugly, someone should make it look better" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var StarSix = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.starsix}&gt;
</span><span class='line'>        &lt;TriangleUp style={styles.starSixUp} /&gt;
</span><span class='line'>        &lt;TriangleDown style={styles.starSixDown} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  starsix: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100
</span><span class='line'>  },
</span><span class='line'>  starSixUp: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 0,
</span><span class='line'>    left: 0
</span><span class='line'>  },
</span><span class='line'>  starSixDown: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 25,
</span><span class='line'>    left: 0
</span><span class='line'>  }
</span></code></pre></td></tr></table></div></figure>


<h3>Star (5-points)</h3>

<p>Yaye <code>TriangleUp</code> is killing it. This one is REALLY hacky with the placement, could use some fine tuning.</p>

<p><img src="http://i.imgur.com/hUvOTUx.png" title="Basically a starfish" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
<span class='line-number'>47</span>
<span class='line-number'>48</span>
<span class='line-number'>49</span>
<span class='line-number'>50</span>
<span class='line-number'>51</span>
<span class='line-number'>52</span>
<span class='line-number'>53</span>
<span class='line-number'>54</span>
<span class='line-number'>55</span>
<span class='line-number'>56</span>
<span class='line-number'>57</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var StarFive = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.starfive}&gt;
</span><span class='line'>        &lt;TriangleUp style={styles.starfiveTop} /&gt;
</span><span class='line'>        &lt;View style={styles.starfiveBefore} /&gt;
</span><span class='line'>        &lt;View style={styles.starfiveAfter} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>
</span><span class='line'>  starfive: {
</span><span class='line'>    width: 150,
</span><span class='line'>    height: 150,
</span><span class='line'>  },
</span><span class='line'>  starfiveTop: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: -45,
</span><span class='line'>    left: 37
</span><span class='line'>  },
</span><span class='line'>  starfiveBefore: {
</span><span class='line'>    backgroundColor: 'transparent',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    left: 0,
</span><span class='line'>    top: 0,
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderRightWidth: 100,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderBottomWidth: 70,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderLeftWidth: 100,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    transform: [
</span><span class='line'>      { rotate: '35deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  starfiveAfter: {
</span><span class='line'>    backgroundColor: 'transparent',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 0,
</span><span class='line'>    left: -25,
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderRightWidth: 100,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderBottomWidth: 70,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderLeftWidth: 100,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    transform: [
</span><span class='line'>      { rotate: '-35deg'}
</span><span class='line'>    ]
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Pentagon</h3>

<p>No <code>TriangleUp</code> here but we could have used a Corner Triangle with rotate.</p>

<p><img src="http://i.imgur.com/LEDmb24.png" title="I hate geometry" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Pentagon = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.pentagon}&gt;
</span><span class='line'>        &lt;View style={styles.pentagonInner} /&gt;
</span><span class='line'>        &lt;View style={styles.pentagonBefore} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  pentagon: {
</span><span class='line'>    backgroundColor: 'transparent'
</span><span class='line'>  },
</span><span class='line'>  pentagonInner: {
</span><span class='line'>    width: 90,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderBottomWidth: 0,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 18,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 18,
</span><span class='line'>    borderTopColor: 'red',
</span><span class='line'>    borderTopWidth: 50
</span><span class='line'>  },
</span><span class='line'>  pentagonBefore: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    height: 0,
</span><span class='line'>    width: 0,
</span><span class='line'>    top: -35,
</span><span class='line'>    left: 0,
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderBottomWidth: 35,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 45,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 45,
</span><span class='line'>    borderTopWidth: 0,
</span><span class='line'>    borderTopColor: 'transparent',
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Hexagon</h3>

<p>2 Triangles and a square. Everything is just shapes.</p>

<p><img src="http://i.imgur.com/djNMGNg.png" title="Honeycomb" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
<span class='line-number'>47</span>
<span class='line-number'>48</span>
<span class='line-number'>49</span>
<span class='line-number'>50</span>
<span class='line-number'>51</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var Hexagon = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.hexagon}&gt;
</span><span class='line'>        &lt;View style={styles.hexagonInner} /&gt;
</span><span class='line'>        &lt;View style={styles.hexagonBefore} /&gt;
</span><span class='line'>        &lt;View style={styles.hexagonAfter} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  hexagon: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 55
</span><span class='line'>  },
</span><span class='line'>  hexagonInner: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 55,
</span><span class='line'>    backgroundColor: 'red'
</span><span class='line'>  },
</span><span class='line'>  hexagonAfter: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    bottom: -25,
</span><span class='line'>    left: 0,
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderTopWidth: 25,
</span><span class='line'>    borderTopColor: 'red'
</span><span class='line'>  },
</span><span class='line'>  hexagonBefore: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: -25,
</span><span class='line'>    left: 0,
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderBottomWidth: 25,
</span><span class='line'>    borderBottomColor: 'red'
</span><span class='line'>
</span><span class='line'>  }
</span></code></pre></td></tr></table></div></figure>


<h3>Octagon</h3>

<p>I attempted copied the css on this one but it required setting a background color, so I did 4 bars and just rotated them. Slightly more markup but this is just for fun.</p>

<p><img src="http://i.imgur.com/i5drMtB.png" title="Stop!" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Octagon = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.octagon}&gt;
</span><span class='line'>        &lt;View style={[styles.octagonUp, styles.octagonBar]} /&gt;
</span><span class='line'>        &lt;View style={[styles.octagonFlat, styles.octagonBar]} /&gt;
</span><span class='line'>        &lt;View style={[styles.octagonLeft, styles.octagonBar]} /&gt;
</span><span class='line'>        &lt;View style={[styles.octagonRight, styles.octagonBar]} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>
</span><span class='line'>
</span><span class='line'>  octagon: {},
</span><span class='line'>  octagonBar: {
</span><span class='line'>    width: 42,  
</span><span class='line'>    height: 100,
</span><span class='line'>    backgroundColor: 'red'
</span><span class='line'>  },
</span><span class='line'>  octagonUp: {},
</span><span class='line'>  octagonFlat: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 0,
</span><span class='line'>    left: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '90deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  octagonLeft: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 0,
</span><span class='line'>    left: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '-45deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  octagonRight: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 0,
</span><span class='line'>    left: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '45deg'}
</span><span class='line'>    ]
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Heart</h3>

<p>This one is easy since well I already had it done for my previous tutorial.</p>

<p><img src="http://i.imgur.com/uBAv2eJ.png" title="in the name of love" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Heart = React.createClass({
</span><span class='line'>    render: function() {
</span><span class='line'>        return (
</span><span class='line'>            &lt;View {...this.props} style={[styles.heart, this.props.style]}&gt;
</span><span class='line'>                &lt;View style={styles.leftHeart} /&gt;
</span><span class='line'>                &lt;View style={styles.rightHeart} /&gt;
</span><span class='line'>            &lt;/View&gt;
</span><span class='line'>        )
</span><span class='line'>    }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  heart: {
</span><span class='line'>    width: 50,
</span><span class='line'>    height: 50
</span><span class='line'>  },
</span><span class='line'>  heartShape: {
</span><span class='line'>    width: 30,
</span><span class='line'>    height: 45,
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 0,
</span><span class='line'>    borderTopLeftRadius: 15,
</span><span class='line'>    borderTopRightRadius: 15,
</span><span class='line'>    backgroundColor: '#6427d1',
</span><span class='line'>  },
</span><span class='line'>  leftHeart: {
</span><span class='line'>    transform: [
</span><span class='line'>        {rotate: '-45deg'}
</span><span class='line'>    ],
</span><span class='line'>    left: 5
</span><span class='line'>  },
</span><span class='line'>  rightHeart: {
</span><span class='line'>    transform: [
</span><span class='line'>        {rotate: '45deg'}
</span><span class='line'>    ],
</span><span class='line'>    right: 5
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Infinity</h3>

<p>Width and border radius all work oddly together. So baby infinity? Scale it up if you want it bigger.</p>

<p><img src="http://i.imgur.com/7Ykpa06.png" title="This could be animated and you would have no idea" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
<span class='line-number'>47</span>
<span class='line-number'>48</span>
<span class='line-number'>49</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Infinity = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.infinity}&gt;
</span><span class='line'>        &lt;View style={styles.infinityBefore} /&gt;
</span><span class='line'>        &lt;View style={styles.infinityAfter} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  infinity: {
</span><span class='line'>    width: 80,
</span><span class='line'>    height: 100,
</span><span class='line'>  },
</span><span class='line'>  infinityBefore: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 0,
</span><span class='line'>    left: 0,
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderWidth: 20,
</span><span class='line'>    borderColor: 'red',
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderTopLeftRadius: 50,
</span><span class='line'>    borderTopRightRadius: 50,
</span><span class='line'>    borderBottomRightRadius: 50,
</span><span class='line'>    borderBottomLeftRadius: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '-135deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  infinityAfter: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 0,
</span><span class='line'>    right: 0,
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderWidth: 20,
</span><span class='line'>    borderColor: 'red',
</span><span class='line'>    borderStyle: 'solid',
</span><span class='line'>    borderTopLeftRadius: 50,
</span><span class='line'>    borderTopRightRadius: 0,
</span><span class='line'>    borderBottomRightRadius: 50,
</span><span class='line'>    borderBottomLeftRadius: 50,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '-135deg'}
</span><span class='line'>    ]
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Diamond Square</h3>

<p>This was more than just a rotated square. Am I missing something?</p>

<p><img src="http://i.imgur.com/gAL9dfq.png" title="Not a blood diamond" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var Diamond = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.diamond} /&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  diamond:{
</span><span class='line'>    width: 50,
</span><span class='line'>    height: 50,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '45deg'}
</span><span class='line'>    ]    
</span><span class='line'>  }
</span></code></pre></td></tr></table></div></figure>


<h3>Diamond Shield</h3>

<p>Just 2 triangles, thought this one was going to be harder.</p>

<p><img src="http://i.imgur.com/4S6FDMo.png" title="also just a kite" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var DiamondShield = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.diamondShield}&gt;
</span><span class='line'>        &lt;View style={styles.diamondShieldTop} /&gt;
</span><span class='line'>        &lt;View style={styles.diamondShieldBottom} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  diamondShield: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100
</span><span class='line'>  },
</span><span class='line'>  diamondShieldTop: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopWidth: 50,
</span><span class='line'>    borderTopColor: 'transparent',
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderBottomWidth: 20,
</span><span class='line'>  },
</span><span class='line'>  diamondShieldBottom: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopWidth: 70,
</span><span class='line'>    borderTopColor: 'red',
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderBottomColor: 'transparent',
</span><span class='line'>    borderBottomWidth: 50,
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Diamond Narrow</h3>

<p>Another 2 triangles that could have been the same and rotated. This way works too.</p>

<p><img src="http://i.imgur.com/cRwI61S.png" title="Diamond on a diet" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var DiamondNarrow = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.diamondNarrow}&gt;
</span><span class='line'>        &lt;View style={styles.diamondNarrowTop} /&gt;
</span><span class='line'>        &lt;View style={styles.diamondNarrowBottom} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  diamondNarrow: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100
</span><span class='line'>  },
</span><span class='line'>  diamondNarrowTop: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopWidth: 50,
</span><span class='line'>    borderTopColor: 'transparent',
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderBottomWidth: 70,  
</span><span class='line'>  },
</span><span class='line'>  diamondNarrowBottom: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopWidth: 70,
</span><span class='line'>    borderTopColor: 'red',
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderBottomColor: 'transparent',
</span><span class='line'>    borderBottomWidth: 50, 
</span><span class='line'>  }
</span></code></pre></td></tr></table></div></figure>


<h3>Cut Diamond</h3>

<p>The top could have been used for the octagon, I chose a different way though.</p>

<p><img src="http://i.imgur.com/yZNHZP0.png" title="Now that is a diamond" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>
</span><span class='line'>var CutDiamond = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.cutDiamond}&gt;
</span><span class='line'>        &lt;View style={styles.cutDiamondTop} /&gt;
</span><span class='line'>        &lt;View style={styles.cutDiamondBottom} /&gt;
</span><span class='line'>      &lt;/View&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  cutDiamond: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100,
</span><span class='line'>  },
</span><span class='line'>  cutDiamondTop: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopWidth: 0,
</span><span class='line'>    borderTopColor: 'transparent',
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 25,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 25,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderBottomWidth: 25, 
</span><span class='line'>  },
</span><span class='line'>  cutDiamondBottom: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopWidth: 70,
</span><span class='line'>    borderTopColor: 'red',
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderBottomColor: 'transparent',
</span><span class='line'>    borderBottomWidth: 0, 
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Egg</h3>

<p>Circular things are hard to do in RN. This is eggish.</p>

<p><img src="http://i.imgur.com/0v5tH4x.png" title="Her?" ></p>

<p><img src="http://i.imgur.com/27Rbo3x.gif" title="Egg?" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Egg = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.egg} /&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  egg: {
</span><span class='line'>    width: 126,
</span><span class='line'>    height: 180,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    borderTopLeftRadius: 108,
</span><span class='line'>    borderTopRightRadius: 108,
</span><span class='line'>    borderBottomLeftRadius: 95,
</span><span class='line'>    borderBottomRightRadius: 95
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Pac-Man</h3>

<p>This one is so simple but always so fun.</p>

<p><img src="http://i.imgur.com/TZHjuxw.png" title="Pixels was a teribel movie" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var PacMan = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.pacman}/&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  pacman: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopWidth: 60,
</span><span class='line'>    borderTopColor: 'red',
</span><span class='line'>    borderLeftColor: 'red',
</span><span class='line'>    borderLeftWidth: 60,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRightWidth: 60,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderBottomWidth: 60, 
</span><span class='line'>    borderTopLeftRadius: 60,
</span><span class='line'>    borderTopRightRadius: 60,
</span><span class='line'>    borderBottomRightRadius: 60,
</span><span class='line'>    borderBottomLeftRadius: 60
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Talk Bubble</h3>

<p>This one is also simple, triangle and a rounded square.</p>

<p><img src="http://i.imgur.com/1LIwGEQ.png" title="Perfect for your billion dollar slack clone" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TalkBubble = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.talkBubble}&gt;
</span><span class='line'>        &lt;View style={styles.talkBubbleSquare} /&gt;
</span><span class='line'>        &lt;View style={styles.talkBubbleTriangle} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  talkBubble: {
</span><span class='line'>    backgroundColor: 'transparent'
</span><span class='line'>  },
</span><span class='line'>  talkBubbleSquare: {
</span><span class='line'>    width: 120,
</span><span class='line'>    height: 80,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    borderRadius: 10
</span><span class='line'>  },
</span><span class='line'>  talkBubbleTriangle: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    left: -26,
</span><span class='line'>    top: 26,
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderTopColor: 'transparent',
</span><span class='line'>    borderTopWidth: 13,
</span><span class='line'>    borderRightWidth: 26,
</span><span class='line'>    borderRightColor: 'red',
</span><span class='line'>    borderBottomWidth: 13,
</span><span class='line'>    borderBottomColor: 'transparent'
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>12 Point Burst</h3>

<p>I will admit this one confused be a little bit, then I realized it&rsquo;s just a couple of rotated squares.</p>

<p><img src="http://i.imgur.com/FHx0WVH.png" title="NOW 90% OFF!!" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TwelvePointBurst = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.twelvePointBurst}&gt;
</span><span class='line'>        &lt;View style={styles.twelvePointBurstMain} /&gt;
</span><span class='line'>        &lt;View style={styles.twelvePointBurst30} /&gt;
</span><span class='line'>        &lt;View style={styles.twelvePointBurst60} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>
</span><span class='line'> twelvePointBurst: {},
</span><span class='line'>  twelvePointBurstMain: {
</span><span class='line'>    width: 80,
</span><span class='line'>    height: 80,
</span><span class='line'>    backgroundColor: 'red'
</span><span class='line'>  },
</span><span class='line'>  twelvePointBurst30: {
</span><span class='line'>    width: 80, 
</span><span class='line'>    height: 80,
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    top: 0,
</span><span class='line'>    right: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '30deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  twelvePointBurst60: {
</span><span class='line'>    width: 80, 
</span><span class='line'>    height: 80,
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    top: 0,
</span><span class='line'>    right: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '60deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span></code></pre></td></tr></table></div></figure>


<h3>8 Point Burst</h3>

<p>Just like the 12, but one less square and different rotations. Only thing here is because the pseudo element was positionined relative to the first 20 degree rotation and ours isn&rsquo;t we&rsquo;ll just bump it up to 155.</p>

<p><img src="http://i.imgur.com/IITGOMB.png" title="Sun" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var EightPointBurst = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.eightPointBurst}&gt;
</span><span class='line'>        &lt;View style={styles.eightPointBurst20} /&gt;
</span><span class='line'>        &lt;View style={styles.eightPointBurst155} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  eightPointBurst: {},
</span><span class='line'>  eightPointBurst20: {
</span><span class='line'>    width: 80, 
</span><span class='line'>    height: 80,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '20deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  eightPointBurst155: {
</span><span class='line'>    width: 80, 
</span><span class='line'>    height: 80,
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    top: 0,
</span><span class='line'>    left: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '155deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span></code></pre></td></tr></table></div></figure>


<h3>Yin Yang</h3>

<p>This one I don&rsquo;t like because you can&rsquo;t accomplish it without setting a background. Ohwell.
Also weird border issue causing outlines.</p>

<p><img src="http://i.imgur.com/z9cUqaz.png" title="Yin and Yang and see through background borders" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var YinYang = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.yinyang}&gt;
</span><span class='line'>        &lt;View style={styles.yinyangMain} /&gt;
</span><span class='line'>        &lt;View style={styles.yinyangBefore} /&gt;
</span><span class='line'>        &lt;View style={styles.yinyangAfter} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  yinyang: {
</span><span class='line'>
</span><span class='line'>  },
</span><span class='line'>  yinyangMain: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100,
</span><span class='line'>    borderColor: 'red',
</span><span class='line'>    borderTopWidth: 2,
</span><span class='line'>    borderLeftWidth: 2,
</span><span class='line'>    borderBottomWidth: 50,
</span><span class='line'>    borderRightWidth: 2,
</span><span class='line'>    borderRadius: 50
</span><span class='line'>  },
</span><span class='line'>  yinyangBefore: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 24,
</span><span class='line'>    left: 0,
</span><span class='line'>    borderColor: 'red',
</span><span class='line'>    borderWidth: 24,
</span><span class='line'>    borderRadius: 30,
</span><span class='line'>  },
</span><span class='line'>  yinyangAfter: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 24,
</span><span class='line'>    right: 2,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    borderColor: 'white',
</span><span class='line'>    borderWidth: 25,
</span><span class='line'>    borderRadius: 30,
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Badge Ribbon</h3>

<p>Remember, always add <code>backgroundColor: 'transparent'</code> when you are overlapping things.</p>

<p><img src="http://i.imgur.com/3V4K2B3.png" title="Well I did get first place" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
<span class='line-number'>47</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var BadgeRibbon = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.badgeRibbon}&gt;
</span><span class='line'>        &lt;View style={styles.badgeRibbonCircle} /&gt;
</span><span class='line'>        &lt;View style={styles.badgeRibbonNeg140} /&gt;
</span><span class='line'>        &lt;View style={styles.badgeRibbon140} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>  badgeRibbonCircle: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    borderRadius: 50
</span><span class='line'>  },
</span><span class='line'>  badgeRibbon140: {
</span><span class='line'>    backgroundColor:'transparent',
</span><span class='line'>    borderBottomWidth: 70,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderLeftWidth: 40,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightWidth: 40,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 70,
</span><span class='line'>    right: -10,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '140deg'}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  badgeRibbonNeg140: {
</span><span class='line'>    backgroundColor:'transparent',
</span><span class='line'>    borderBottomWidth: 70,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderLeftWidth: 40,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightWidth: 40,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: 70,
</span><span class='line'>    left: -10,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '-140deg'}
</span><span class='line'>    ]
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Space Invader</h3>

<p> <code>WUTTTTTTTTTTT</code></p>

<h3>TV Screen</h3>

<p>Stupid border radius making this one hard. We&rsquo;ll just use a bunch of ovals.</p>

<p><img src="http://i.imgur.com/ffJdfqM.png" title="CRT" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
<span class='line-number'>47</span>
<span class='line-number'>48</span>
<span class='line-number'>49</span>
<span class='line-number'>50</span>
<span class='line-number'>51</span>
<span class='line-number'>52</span>
<span class='line-number'>53</span>
<span class='line-number'>54</span>
<span class='line-number'>55</span>
<span class='line-number'>56</span>
<span class='line-number'>57</span>
<span class='line-number'>58</span>
<span class='line-number'>59</span>
<span class='line-number'>60</span>
<span class='line-number'>61</span>
<span class='line-number'>62</span>
<span class='line-number'>63</span>
<span class='line-number'>64</span>
<span class='line-number'>65</span>
<span class='line-number'>66</span>
<span class='line-number'>67</span>
<span class='line-number'>68</span>
<span class='line-number'>69</span>
<span class='line-number'>70</span>
<span class='line-number'>71</span>
<span class='line-number'>72</span>
<span class='line-number'>73</span>
<span class='line-number'>74</span>
<span class='line-number'>75</span>
<span class='line-number'>76</span>
<span class='line-number'>77</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var TvScreen = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.tvscreen}&gt;
</span><span class='line'>        &lt;View style={styles.tvscreenMain} /&gt;
</span><span class='line'>        &lt;View style={styles.tvscreenTop} /&gt;
</span><span class='line'>        &lt;View style={styles.tvscreenBottom} /&gt;
</span><span class='line'>        &lt;View style={styles.tvscreenLeft} /&gt;
</span><span class='line'>        &lt;View style={styles.tvscreenRight} /&gt;
</span><span class='line'>
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  tvscreen: {},
</span><span class='line'>  tvscreenMain: {
</span><span class='line'>    width: 150,
</span><span class='line'>    height: 75,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    borderTopLeftRadius: 15,
</span><span class='line'>    borderTopRightRadius: 15,
</span><span class='line'>    borderBottomRightRadius: 15,
</span><span class='line'>    borderBottomLeftRadius: 15,
</span><span class='line'>  },
</span><span class='line'>  tvscreenTop: {
</span><span class='line'>    width: 73,
</span><span class='line'>    height: 70,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: -26,
</span><span class='line'>    left: 39,
</span><span class='line'>    borderRadius: 35,
</span><span class='line'>    transform: [
</span><span class='line'>      {scaleX: 2},
</span><span class='line'>      {scaleY: .5}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  tvscreenBottom: {
</span><span class='line'>    width: 73,
</span><span class='line'>    height: 70,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    bottom: -26,
</span><span class='line'>    left: 39,
</span><span class='line'>    borderRadius: 35,
</span><span class='line'>    transform: [
</span><span class='line'>      {scaleX: 2},
</span><span class='line'>      {scaleY: .5}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  tvscreenLeft: {
</span><span class='line'>    width: 20,
</span><span class='line'>    height: 38,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    left: -7,
</span><span class='line'>    top: 18,
</span><span class='line'>    borderRadius: 35,
</span><span class='line'>    transform: [
</span><span class='line'>      {scaleX: .5},
</span><span class='line'>      {scaleY: 2},
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  tvscreenRight: {
</span><span class='line'>    width: 20,
</span><span class='line'>    height: 38,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    right: -7,
</span><span class='line'>    top: 18,
</span><span class='line'>    borderRadius: 35,
</span><span class='line'>    transform: [
</span><span class='line'>      {scaleX: .5},
</span><span class='line'>      {scaleY: 2},
</span><span class='line'>    ]
</span><span class='line'>  },</span></code></pre></td></tr></table></div></figure>


<h3>Chevron</h3>

<p>Once again we don&rsquo;t have skew, but we&rsquo;ll use triangles. Also magical negative scale to flip stuff around!</p>

<p><img src="http://i.imgur.com/HEfbLbS.png" title="get techron with chevron" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
<span class='line-number'>47</span>
<span class='line-number'>48</span>
<span class='line-number'>49</span>
<span class='line-number'>50</span>
<span class='line-number'>51</span>
<span class='line-number'>52</span>
<span class='line-number'>53</span>
<span class='line-number'>54</span>
<span class='line-number'>55</span>
<span class='line-number'>56</span>
<span class='line-number'>57</span>
<span class='line-number'>58</span>
<span class='line-number'>59</span>
<span class='line-number'>60</span>
<span class='line-number'>61</span>
<span class='line-number'>62</span>
<span class='line-number'>63</span>
<span class='line-number'>64</span>
<span class='line-number'>65</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var Chevron = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.chevron}&gt;
</span><span class='line'>        &lt;View style={styles.chevronMain} /&gt;
</span><span class='line'>        &lt;View style={[styles.chevronTriangle, styles.chevronTopLeft]} /&gt;
</span><span class='line'>        &lt;View style={[styles.chevronTriangle, styles.chevronTopRight]} /&gt;
</span><span class='line'>        &lt;View style={[styles.chevronTriangle, styles.chevronBottomLeft]} /&gt;
</span><span class='line'>        &lt;View style={[styles.chevronTriangle, styles.chevronBottomRight]} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>
</span><span class='line'>  chevron: {
</span><span class='line'>    width: 150,
</span><span class='line'>    height: 50
</span><span class='line'>  },
</span><span class='line'>  chevronMain: {
</span><span class='line'>    width: 150,
</span><span class='line'>    height: 50,
</span><span class='line'>    backgroundColor: 'red'
</span><span class='line'>  },
</span><span class='line'>  chevronTriangle: {
</span><span class='line'>    backgroundColor: 'transparent',
</span><span class='line'>    borderTopWidth: 20,
</span><span class='line'>    borderRightWidth: 0,
</span><span class='line'>    borderBottomWidth: 0,
</span><span class='line'>    borderLeftWidth: 75,
</span><span class='line'>    borderTopColor: 'transparent',
</span><span class='line'>    borderBottomColor: 'transparent',
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderLeftColor: 'red',
</span><span class='line'>  },
</span><span class='line'>  chevronTopLeft: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: -20,
</span><span class='line'>    left: 0
</span><span class='line'>  },
</span><span class='line'>  chevronTopRight: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    top: -20,
</span><span class='line'>    right: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {scaleX: -1}
</span><span class='line'>    ]
</span><span class='line'>  },
</span><span class='line'>  chevronBottomLeft: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    bottom: -20,
</span><span class='line'>    left: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {scale: -1 }
</span><span class='line'>    ]
</span><span class='line'>  },     
</span><span class='line'>  chevronBottomRight: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    bottom: -20,
</span><span class='line'>    right: 0,
</span><span class='line'>    transform: [
</span><span class='line'>      {scaleY: -1}
</span><span class='line'>    ]
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Magnifying Glass</h3>

<p>Border around a circle with a stick. Nothing to it.</p>

<p><img src="http://i.imgur.com/1aCNZLk.png" title="Blow bubbles" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var MagnifyingGlass = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.magnifyingGlass}&gt;
</span><span class='line'>        &lt;View style={styles.magnifyingGlassCircle} /&gt;
</span><span class='line'>        &lt;View style={styles.magnifyingGlassStick} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  magnifyingGlass: {
</span><span class='line'>
</span><span class='line'>  },
</span><span class='line'>  magnifyingGlassCircle: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 100,
</span><span class='line'>    borderRadius: 50,
</span><span class='line'>    borderWidth: 15,
</span><span class='line'>    borderColor: 'red'
</span><span class='line'>  },
</span><span class='line'>  magnifyingGlassStick: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    right: -20,
</span><span class='line'>    bottom: -10,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    width: 50,
</span><span class='line'>    height: 10,
</span><span class='line'>    transform: [
</span><span class='line'>      {rotate: '45deg'}
</span><span class='line'>    ]</span></code></pre></td></tr></table></div></figure>


<h3>Facebook Icon</h3>

<p>This one seems appropriate but couldn&rsquo;t get it to work well. I attempted it and failed.</p>

<p><img src="http://i.imgur.com/Y9lyxN7.png" title="React Native brought to you by" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
<span class='line-number'>32</span>
<span class='line-number'>33</span>
<span class='line-number'>34</span>
<span class='line-number'>35</span>
<span class='line-number'>36</span>
<span class='line-number'>37</span>
<span class='line-number'>38</span>
<span class='line-number'>39</span>
<span class='line-number'>40</span>
<span class='line-number'>41</span>
<span class='line-number'>42</span>
<span class='line-number'>43</span>
<span class='line-number'>44</span>
<span class='line-number'>45</span>
<span class='line-number'>46</span>
<span class='line-number'>47</span>
<span class='line-number'>48</span>
<span class='line-number'>49</span>
<span class='line-number'>50</span>
<span class='line-number'>51</span>
<span class='line-number'>52</span>
<span class='line-number'>53</span>
<span class='line-number'>54</span>
<span class='line-number'>55</span>
<span class='line-number'>56</span>
<span class='line-number'>57</span>
<span class='line-number'>58</span>
<span class='line-number'>59</span>
<span class='line-number'>60</span>
<span class='line-number'>61</span>
<span class='line-number'>62</span>
<span class='line-number'>63</span>
<span class='line-number'>64</span>
<span class='line-number'>65</span>
<span class='line-number'>66</span>
<span class='line-number'>67</span>
<span class='line-number'>68</span>
<span class='line-number'>69</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Facebook = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.facebook}&gt;
</span><span class='line'>        &lt;View style={styles.facebookMain}&gt;          
</span><span class='line'>          &lt;View style={styles.facebookCurve} /&gt;
</span><span class='line'>          &lt;View style={styles.facebookBefore} /&gt;
</span><span class='line'>          &lt;View style={styles.facebookAfter} /&gt;
</span><span class='line'>          &lt;View style={styles.facebookRedCover} /&gt;
</span><span class='line'>        &lt;/View&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  facebook: {
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 110,
</span><span class='line'>  },
</span><span class='line'>  facebookMain: {
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    width: 100,
</span><span class='line'>    height: 110,
</span><span class='line'>    borderRadius: 5,
</span><span class='line'>    borderColor: 'red',
</span><span class='line'>    borderTopWidth: 15,
</span><span class='line'>    borderLeftWidth: 15,
</span><span class='line'>    borderRightWidth: 15,
</span><span class='line'>    borderBottomWidth: 0,
</span><span class='line'>    overflow: 'hidden'
</span><span class='line'>
</span><span class='line'>  },
</span><span class='line'>  facebookRedCover: {
</span><span class='line'>    width: 10,
</span><span class='line'>    height: 20,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    right: 0,
</span><span class='line'>    top: 5
</span><span class='line'>  },
</span><span class='line'>  facebookCurve: {
</span><span class='line'>    width: 50,
</span><span class='line'>    borderWidth: 20,
</span><span class='line'>    borderTopWidth: 20,
</span><span class='line'>    borderTopColor: 'white',
</span><span class='line'>    borderBottomColor: 'transparent',
</span><span class='line'>    borderLeftColor: 'white',
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderRadius: 20,
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    right: -8,
</span><span class='line'>    top: 5
</span><span class='line'>  },
</span><span class='line'>  facebookBefore: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    backgroundColor: 'white',
</span><span class='line'>    width: 20,
</span><span class='line'>    height: 70,
</span><span class='line'>    bottom: 0,
</span><span class='line'>    right: 22,
</span><span class='line'>  },
</span><span class='line'>  facebookAfter: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    width: 55,
</span><span class='line'>    top: 50,
</span><span class='line'>    height: 20,
</span><span class='line'>    backgroundColor: 'white',
</span><span class='line'>    right: 5
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<p></p>

<h3>Moon</h3>

<p>Box shadow&hellip;</p>

<h3>Flag</h3>

<p>The one on css-tricks inferred a background, we&rsquo;ll just flip it around and say the center is transparent and the outer triangles are red.</p>

<p><img src="http://i.imgur.com/7AMJ3sj.png" title="Have they ever seen a flag?" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>
</span><span class='line'>var Flag = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.flag}&gt;
</span><span class='line'>        &lt;View style={styles.flagTop} /&gt;
</span><span class='line'>        &lt;View style={styles.flagBottom} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  flag: {},
</span><span class='line'>  flagTop: {
</span><span class='line'>    width: 110,
</span><span class='line'>    height: 56,
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>  },
</span><span class='line'>  flagBottom: {
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    left: 0,
</span><span class='line'>    bottom: 0,
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderBottomWidth: 13,
</span><span class='line'>    borderBottomColor: 'transparent',
</span><span class='line'>    borderLeftWidth: 55,
</span><span class='line'>    borderLeftColor: 'red',
</span><span class='line'>    borderRightWidth: 55,
</span><span class='line'>    borderRightColor: 'red'
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Cone</h3>

<p>Had to modify the css on this one a bit to get the same look, 70 => 55.</p>

<p><img src="http://i.imgur.com/04f26Kl.png" title="needs more icecream" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Cone = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.cone} /&gt;
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  cone: {
</span><span class='line'>    width: 0,
</span><span class='line'>    height: 0,
</span><span class='line'>    borderLeftWidth: 55,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightWidth: 55,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    borderTopWidth: 100,
</span><span class='line'>    borderTopColor: 'red',
</span><span class='line'>    borderRadius: 55
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Cross</h3>

<p>More of a plus then a cross.</p>


<p><img src="http://i.imgur.com/0IerLuP.png" title="across from where?" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Cross = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.cross}&gt;
</span><span class='line'>        &lt;View style={styles.crossUp} /&gt;
</span><span class='line'>        &lt;View style={styles.crossFlat} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>
</span><span class='line'>  cross: {
</span><span class='line'>
</span><span class='line'>  },
</span><span class='line'>  crossUp: {
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    height: 100,
</span><span class='line'>    width: 20
</span><span class='line'>  },
</span><span class='line'>  crossFlat: {
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    height: 20,
</span><span class='line'>    width: 100,
</span><span class='line'>    position: 'absolute',
</span><span class='line'>    left: -40,
</span><span class='line'>    top: 40
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h3>Base</h3>

<p>Base&hellip; Home .. Home Base, whichever all the same.</p>

<p><img src="http://i.imgur.com/LGQEIvS.png" title="that's all folks" ></p>

<figure class='code'><div class="highlight"><table><tr><td class="gutter"><pre class="line-numbers"><span class='line-number'>1</span>
<span class='line-number'>2</span>
<span class='line-number'>3</span>
<span class='line-number'>4</span>
<span class='line-number'>5</span>
<span class='line-number'>6</span>
<span class='line-number'>7</span>
<span class='line-number'>8</span>
<span class='line-number'>9</span>
<span class='line-number'>10</span>
<span class='line-number'>11</span>
<span class='line-number'>12</span>
<span class='line-number'>13</span>
<span class='line-number'>14</span>
<span class='line-number'>15</span>
<span class='line-number'>16</span>
<span class='line-number'>17</span>
<span class='line-number'>18</span>
<span class='line-number'>19</span>
<span class='line-number'>20</span>
<span class='line-number'>21</span>
<span class='line-number'>22</span>
<span class='line-number'>23</span>
<span class='line-number'>24</span>
<span class='line-number'>25</span>
<span class='line-number'>26</span>
<span class='line-number'>27</span>
<span class='line-number'>28</span>
<span class='line-number'>29</span>
<span class='line-number'>30</span>
<span class='line-number'>31</span>
</pre></td><td class='code'><pre><code class=''><span class='line'>var Base = React.createClass({
</span><span class='line'>  render: function() {
</span><span class='line'>    return (
</span><span class='line'>      &lt;View style={styles.base}&gt;
</span><span class='line'>        &lt;View style={styles.baseTop} /&gt;
</span><span class='line'>        &lt;View style={styles.baseBottom} /&gt;
</span><span class='line'>      &lt;/View&gt;   
</span><span class='line'>    )
</span><span class='line'>  }
</span><span class='line'>})
</span><span class='line'>  base: {
</span><span class='line'>
</span><span class='line'>  },
</span><span class='line'>  baseTop: {
</span><span class='line'>    borderBottomWidth: 35,
</span><span class='line'>    borderBottomColor: 'red',
</span><span class='line'>    borderLeftWidth: 50,
</span><span class='line'>    borderLeftColor: 'transparent',
</span><span class='line'>    borderRightWidth: 50,
</span><span class='line'>    borderRightColor: 'transparent',
</span><span class='line'>    height: 0,
</span><span class='line'>    width: 0,
</span><span class='line'>    left: 0,
</span><span class='line'>    top: -35,
</span><span class='line'>    position: 'absolute',
</span><span class='line'>  },
</span><span class='line'>  baseBottom: {
</span><span class='line'>    backgroundColor: 'red',
</span><span class='line'>    height: 55,
</span><span class='line'>    width: 100
</span><span class='line'>  }</span></code></pre></td></tr></table></div></figure>


<h1>Final</h1>

<p>Wow what a fun waste of time. Modeling React Native after the web spec is of course a great idea, I just wish it conformed a little nicer on border radius.</p>

<p>Also I hate geometry now.</p>

<h2>Live Code <a href="https://rnplay.org/apps/58FEmw">https://rnplay.org/apps/58FEmw</a></h2>

<p>I&rsquo;m not posting the full code here because it&rsquo;s just too long.</p>

<p><img src="http://i.imgur.com/cWR7FKh.gif" title="Stay in school kids" ></p>
Tagged under
 <a href="http://browniefed.com/blog/the-shapes-of-react-native/">Reference</a> 
		

</div>
        
