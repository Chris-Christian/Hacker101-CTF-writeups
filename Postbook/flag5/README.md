# Postbook - flag5

## Solution steps
- Open developer tools and navigate to the `Application` tab.
- Navigate to cookies and observe there's a cookie named `id` with value=`c81e728d9d4c2f636f067f89cc14862c`.
- The value looks like a hash.
- Go to [crackstation.net](https://crackstation.net/) to crack the hash.
- Paste the hash and crack it.
- Notice that the result is `2`.
- Go to [cyberchef](https://gchq.github.io/CyberChef/), search for `md5` and drag and drop it in the recipe.
- Write `1` in the input and copy the output.
- Paste the hash into the value of the cookie named `id` using developer tools.
- Refresh the page and notice you have successfully logged in as `admin`.
- Retrieve the flag.
