My code example for using node-auth2-server found at https://github.com/thomseddon/node-oauth2-server

This was written purely to test an oauth client, if you want to use a proper model (not in memory like I did) - check out https://github.com/thomseddon/node-oauth2-server/tree/master/examples

# Example usage

Request a token

    curl --request POST  http://localhost:3000/oauth/token --data "grant_type=password&client_id=thom&client_secret=nightworld&username=thomseddon&password=nightworld"  --header "Content-Type: application/x-www-form-urlencoded"

Then use the token with:

    curl -H "Authorization: Bearer b6ebe71330f379f7b0b2ebec3a9d145a2570648b" http://localhost:3000
