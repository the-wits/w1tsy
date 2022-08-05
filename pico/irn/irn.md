---
layout: page
title: Irish-Name-Repo
exclude: true
---

## Summary
- **Category:** Web Exploitation
- **Difficulty:** Easy
- **Main Topics:** SQL Injection
- [**CTF webpage**](https://play.picoctf.org/practice/challenge/80?category=1&page=3)

## Irish-Name-Repo 1
> Connect to the [website](http://jupiter.challenges.picoctf.org:39720). Do you think you can log us in? Try to see if you can login!

- Click on menu icon on the upper-left corner
- Click on Admin Login button
- Try a SQLi attack by using the `admin --` payload to get the flag

**Flag:** `picoCTF{s0m3_SQL_c218b685}`

## Irish-Name-Repo 2

> Connect to the [website](http://jupiter.challenges.picoctf.org:52849). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login!

- Click on menu icon on the upper-left corner
- Click on Admin Login button
- Try a SQLi attack by using the `admin' --` payload to get the flag

**Flag:** `picoCTF{m0R3_SQL_plz_fa983901}`

## Irish-Name-Repo 3

> Connect to the [website](http://jupiter.challenges.picoctf.org:29132). Try to see if you can login as admin!

- Click on menu icon on the upper-left corner
- Click on Admin Login button
- Now there is only a password input field
- SQLi attack by using the `admin' --` payload and debug mode
- Passwords are encoded with ROT13
- The payload `OR 1=1 --` became `BE 1=1 --` with ROT13 and you get the flag

**Flag:** `picoCTF{3v3n_m0r3_SQL_06a9db19}`
