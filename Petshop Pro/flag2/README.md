# Petshop Pro - flag2

## Solution steps
- After logging in using the method described in flag1's solution click on `edit` option beside `add to cart`.
- Inject an XSS payload into the `name` field, for example:
  `<img src=x onerror="alert(1)">`
- Save the changes and add that item to cart.
- Open the cart and retrieve the flag.

**Note:** You can also get this flag without logging in by navigating to `https://xxxxx.ctf.hacker101.com/edit?id=1` and injecting the payload as described above.
