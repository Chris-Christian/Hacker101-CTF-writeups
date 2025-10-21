# Petshop Pro - flag0

## Solution steps
- Open Burp suite and set-up proxy.
- Add any item to the cart and open cart: https://xxxxxx.ctf.hacker101.com/cart
- Click the `checkout` button.
- From Http history send the `POST /checkout` request to the repeater.
- In Repeater, modify the URL-encoded `cart` parameter so the item's `price` is `$0`:
  `cart=%5B%5B0%2C+%7B%22name%22%3A+%22Kitten%22%2C+%22desc%22%3A+%228%5C%22x10%5C%22+color+glossy+photograph+of+a+kitten.%22%2C+%22logo%22%3A+%22kitten.jpg%22%2C+%22price%22%3A+0%7D%5D%5D`
- Send the modified request and observe the item price is now `$0`.
- Retrieve the flag from the response.
