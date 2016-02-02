---
layout: post
title: Quick Tip - React.js onClick handler 
---
Here's a quick tip on getting an onClick handler to work properly with React.

Simply, the value for your onClick attribute should be a function, not a function call. Example code snippet below.

{% highlight js %}
<button type="submit" onClick={() => { this.props.removeTaskFunction(todo) }}>Submit</button>
{% endhighlight %}

Or for non-ES6:
{% highlight js %}
<button type="submit" onClick={function(){removeTaskFunction(todo)}}>Submit</button>
{% endhighlight %}
