---
layout: page
title: Power Cookie
exclude: true
---

## Summary
- **Category:** Web Exploitation
- **Difficulty:** Very Easy
- **Main Topics:** Cookies
- [**CTF webpage**](https://play.picoctf.org/practice/challenge/288?category=1&page=3)

## Power Cookie
> Can you get the flag? Go to this [website](http://saturn.picoctf.net:55287/) and see what you can discover.

The first step is to connect to the website that shows the following homepage.

![homepage]({{ '/pico/cookies/imgs/power.png' | relative_url }})

The HTML analysis shows that the website relies on the `guest.js` script
{% highlight js %}
function continueAsGuest()
{
  window.location.href = '/check.php';
  document.cookie = "isAdmin=0";
}
{% endhighlight %}
The **Continue as guest** button triggers the `continueAsGuest()` function and sets the cookie named
`isAdmin` to `0`. You can change the value of the cookie to `1` through the `Storage` tab of devtools 
in your browser and reload the webpage to get the flag!

**Flag:** `picoCTF{gr4d3_A_c00k13_5d2505be}`
