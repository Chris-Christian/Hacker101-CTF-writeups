# Postbook - flag3

## Solution steps
- Open Burp suite and set-up proxy.
- Turn the intercept `ON`.
- Open any post and send the request to the `intruder`.
- Add payload markers around the id parameter: `id=§1§`
- Change the payload type from `Simple list` to `Numbers`.
- From number range select type as `sequential` and range from `1` to `1000` with step `1`.
- Start the attack.
- Observe the length of the output and notice it has `1500` length for non-existing posts and different lengths for existing posts.
- Notice at `id=945` the length changes.
- View the response of that request.
- Retrieve the flag.
