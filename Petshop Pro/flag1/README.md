# Petshop Pro - flag1

## Solution steps
- Bruteforce the directories of `https://xxxxx.ctf.hacker101.com` using `gobuster`:
  `gobuster dir -u https://xxxxx.ctf.hacker101.com -w /path/to/wordlist.txt`
- I personally used [DirBuster-2007_directory-list-2.3-big.txt](https://github.com/danielmiessler/SecLists/blob/master/Discovery/Web-Content/DirBuster-2007_directory-list-2.3-big.txt) for this task.
- I successfully discovered the administrative login page at `/login`.
- Navigate to `https://xxxxx.ctf.hacker101.com/login`.
- After attempting common SQL injection payloads I found out the application had protection against basic injections.
- Try bruteforcing the username and password using `ffuf`:
  `ffuf -u https://xxxxxxx.ctf.hacker101.com/login -w Desktop/username.txt -X POST -d "username=FUZZ&password=admin" -H "Content-Type: application/x-www-form-urlencoded" -mr "Invalid password"`
- The above command keeps the password static and brute-forces the `username` parameter until we see the response "Invalid password", which indicates the username is correct.
- After getting username, keep it static and bruteforce password using different wordlist:
  `ffuf -u https://xxxxxxx.ctf.hacker101.com/login -w Desktop/password.txt -X POST -d "username=demousername&password=FUZZ" -H "Content-Type: application/x-www-form-urlencoded" -fr "Invalid password"`
- Login using the credentials and retrieve the flag.
---
> I tried several wordlists but didn’t find the username, so I couldn’t retrieve the flag; the steps above describe the intended approach.
