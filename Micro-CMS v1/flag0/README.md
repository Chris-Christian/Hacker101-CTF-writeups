# Micro-CMS v1 - flag0

## Solution steps
- Click on the url which takes you to the `Testing` page and observe it's indexed as `1`:
  `https://xxxxxx.ctf.hacker101.com/page/1`
- Click on `Edit page` and observe that you can also edit the page's contents.
- The edit page is indexed as: `https://xxxxxxx.ctf.hacker101.com/page/edit/1`
- Now go to home and create a new page and observe it's directly indexed as `/page/10`.
- Try changing the index from the url from 1 to 10 and notice that `/page/6` is forbidden.
- Try to view the page with the edit page url by changing it's index to `6`:
  `https://xxxxxxx.ctf.hacker101.com/page/edit/6`
- Retrieve the flag.
