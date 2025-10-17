# Postbook - flag6

## Solution steps
- Hover over the `delete` element which let's you delete a post.
- Right click and copy it's link address: `https://xxxxxx.ctf.hacker101.com/index.php?page=delete.php&id=c81e728d9d4c2f636f067f89cc14862c`
- Notice it contains an `id` parameter which looks like a hash.
- Copy the id.
- Open [crackstation.net](https://crackstation.net/) in your browser, paste the hash and crack it.
- Notice it's a `md5` hash and our result is `2`.
- Open [cyberchef](https://gchq.github.io/CyberChef/#recipe=MD5()) in your browser, search for `md5` then drag and drop it in the recipe.
- Write `3` in the input and copy the hash.
- Replace it with the previous hash in the link: `https://xxxxxx.ctf.hacker101.com/index.php?page=delete.php&id=eccbc87e4b5ce2fe28308fd9f2a7baf3`
- Open this link in your browser and notice you successfully deleted a post which was authored by another user.
- Retrieve the flag.
