---
layout: page
title: Digital Camouflage
exclude: true
---

## Summary
- **Category:** Forensics
- **Difficulty:** Medium
- **Main Topics:** Wireshark
- [**CTF webpage**](https://ctflearn.com/challenge/237)

## Challenge
> We need to gain access to some routers. Let's try and see if we can find the password in the captured network [data](https://mega.nz/#!XDBDRAQD!4jRcJvAhMkaVaZCOT3z3zkyHre2KHfmkbCN5lYpiEoY).<br><br>
Hint 1: It looks like someone logged in with their password earlier. Where would log in data be located in a network capture?<br><br>
Hint 2: If you think you found the flag, but it doesn't work, consider that the data may be encrypted.

- Download the `data.pcap` file
- Open the file with Wireshark
- Challenge description says *someone logged in with their password* 
- Filter the traffic by using `http.request.method == "POST"`
- The request body contains the base64 encoded password `UEFwZHNqUlRhZQ==`
- Decode it and get the flag

**Flag:** `PApdsjRTae`
