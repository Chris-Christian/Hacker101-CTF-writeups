# Micro-CMS v1 - flag1

## Solution steps
- Click on the URL that takes you to the Testing page:
  `https://xxxxxx.ctf.hacker101.com/page/1`
- Attempt SQL injection on the page URL (note the trailing `'`):
  `https://xxxxxx.ctf.hacker101.com/page/1'`
- Nothing found.
- Return to the **Testing** page and click **Edit this page**.
- Attempt SQL injection on the edit endpoint (again note the trailing `'`):
  `https://xxxxxxxxx.ctf.hacker101.com/page/edit/1'`
- Retrieve the flag.
