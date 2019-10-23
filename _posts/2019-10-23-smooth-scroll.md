---
layout: post
title:  "Smooth scroll"
date:   2019-10-23 17:00:50 -0300
categories: blog
excerpt_separator: <!--more-->
keywords:
  - smooth scroll
---

Hi there!

Do you want to give your site that cool smooth scroll when someone clicks a link?

<!--more-->

So, lets say you have an awesome page with different sections. You have several ways for allowing the user to get to them. Here are some examples:

  1. Good ol' scrolling,
  2. Click on a link and make the user insta-jump to the desired section,
  3. Click on a link and make the user go to the desired section with a cool smooth auto-scroll.

Here we go with the CSS way to get that smooth auto-scroll:

## The CSS

{% highlight css %}
{% raw %}
html {
  scroll-behavior: smooth;
}
{% endraw %}
{% endhighlight %}

Replacing `smooth` with `auto` gives you the default insta-jump behavior.

## Consider users with motion sickness

Vestibular disorders arise when the parts of the inner ear and brain that process the sensory information involved with controlling balance and eye movement get damaged.

Users with this disorders may suffer from motion sickness, which can make the experience of browsing the web quite unpleasent for them.

As stated in [MDN](https://developer.mozilla.org/es/docs/Web/CSS/scroll-behavior), you should use a CSS `prefers-reduced-motion` media query to disable smooth scrolling to account for users that have set their browsers to `reduced motion`:

{% highlight css %}
{% raw %}
html {
  scroll-behavior: smooth;
}

@media (prefers-reduced-motion: reduce) {
    html {
        scroll-behavior: auto;
    }
}
{% endraw %}
{% endhighlight %}

## Compatibility

This CSS property is supported in Chrome, Firefox and Opera. As of the date of publication of this blog post, it is not supported  in Safari, Edge nor Internet Explorer.

Cheers, have a good one!