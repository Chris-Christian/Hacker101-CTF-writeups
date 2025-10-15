# Micro-CMS v1 - flag3

## Solution steps
- Click the URL that opens the **Markdown Test** page:
  `https://xxxxxx.ctf.hacker101.com/page/2`
- Click **Edit this page** and observe it contains an image element and a button element with attributes.
- Inject an inline event handler into the button, e.g.:
  `<button onclick=alert(1)>Some button</button>`
- Save and click the button.
- Observe that an alert pops but no flag in found.
- Inspect that button element using developer tools.
- Retrieve the flag.
