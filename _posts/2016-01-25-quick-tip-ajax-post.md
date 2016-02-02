---
layout: post
title: Quick Tip - AJAX POST contentType 
---
Here's a quick tip to get an AJAX POST to work properly. It is something simple, yet remarkably not easy to determine via the api docs or even Stack Overflow.  

The contentType is the key:value pair that makes POST work. Example code snippet below. 

{% highlight js %}
    $.ajax({
      type: "POST",
      url: '/testurl',
      data: JSON.stringify(data),
      success: function() {console.log('hooray')},
      contentType: 'application/json'   // IMPORTANT!!!
    });
{% endhighlight %}
