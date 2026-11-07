AWS publishes all of its IP address ranges at this URL in json format:

https://ip-ranges.amazonaws.com/ip-ranges.json

The main purpose why we would want to look this up is because large organization might want to configure their internal networking devices to allow the ranges on the allowlist. 

Since the endpoint is a json endpoint, we can programmatically access that file and pull data using "curl" (to download the results) then pass it to "jq" for parshing json to have it return the exact ranges that we need. 