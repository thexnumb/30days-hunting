# Day24 `20-Jan-2025`
- Hello everyone, without any time intrupt let's go to the work.
- Yesterday we run `dirsearch` on some specific domains of the application that leads us to some points like `License.txt` this maybe leads us to the current version of the wordpress and then we can search for `CVE` for it if there is any.
- nothing found, then get back to the main job
- as the recon I've done one domain of this application is too tiny but there is like `dev.domain.tld` or `staging.domain.tld`
    - so the best approach in here is to do `dns-bruteforce`
    - for `dns-bruteforce` best approach that I can do to not use my own server is to use the [trickest](https://trickest.io/)
        - command: `shuffledns -w in/dnsgen-1/output.txt -d granularinsurance.com -r in/http-input-3/.resolvers -list in/http-input-4/static_final.txt -wt 5 -o out/shuffledns-1/output.txt`
- in meanwhile we doing manual task on other endpoint
- arrive to an endpoint that have kind of waf that show forbidden when request for a file like `hello.php` so in this case first search to see can we have another extension or not
    - not found anything
- in the `/wp-json` I've found interesting things that wait for me until tomorrow. :+
