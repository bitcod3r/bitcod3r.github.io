---
layout: post
title: symfony1.4 + Ajax
date: '2014-11-04T10:00:00-05:00'
tags:
- symfony
- sf1.4
- ajax
- php
- frameworks
tumblr_url: https://bitcod3r.tumblr.com/post/101760313285/symfony1-4-ajax-symfox
---
After implementing so many old-school website based structures, I started using a different approach to pass across the [MVC paradigm](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller).

## Do we have to reload our application page every time?

It all depends on how we are going to implement UX. Okay, wait. [symfony](https://symfony.com/) simply does not take care too much attention to UX, because it is controller-based.&nbsp; Under that perspective, we have functionality in one hand versus usability in the other. Changing our vision towards actual tendencies, we have some new patterns to design web apps. A new concept incorporates [one-single page apps](http://singlepageappbook.com/goal.html "one single page apps")&nbsp;as a defacto way to deal with usability, without sacrificing asynchronous HTTP request demand.

A regular use case when the user interacts with an app altering data is not a good idea pulling the user out of the usual flow with a total page refresh. In that case, we can just take a one-page action to refresh only some UI components in the page.

<!-- more -->

Ok, let’s get rid of that premise with one simple example:

## View

{% highlight python %}
<div id="dinamic-div">

<?php include_partial('mi_partial',array('variable => $variable)) ?>

{% endhighlight %}

## Controller (+ajax)

{% highlight javascript %}
function(HTTPRequest $request) {
    $variable = $request->getParameter('variable');
    
    // execute here my code then...
    
    return render_partial('mi_partial',array('variable => $variable));
{% endhighlight %}

As you can see, there’s only one partial to be refreshed with new data. Eliminating the need to take the whole page to a new singularity state. It only depends on the component being affected.&nbsp;
