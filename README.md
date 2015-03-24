My code example for using node-auth2-server found at https://github.com/thomseddon/node-oauth2-server

This was written purely to test an oauth client, if you want to use a proper model (not in memory like I did) - check out https://github.com/thomseddon/node-oauth2-server/tree/master/examples

# Install

Checkout from git, then from the source directory (assuming you have nodejs installed)

    npm install
    node .

Now test locally using example below.

# Example client usage

Request a token

    curl --request POST  http://localhost:3000/oauth/token --data "grant_type=password&client_id=thom&client_secret=nightworld&username=thomseddon&password=nightworld"  --header "Content-Type: application/x-www-form-urlencoded"

Then use the token with (replace the token with the one you got from the line above):

    curl -H "Authorization: Bearer b6ebe71330f379f7b0b2ebec3a9d145a2570648b" http://localhost:3000
