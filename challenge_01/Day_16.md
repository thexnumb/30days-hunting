# Day16 `07-Jan-2025`
- for today first I'll going to test for services on that Server IP that I found.
    - first job is port scan
        - this job is too riskly based on the ISP, or on the server provider so let's do some works to decrease that risk.
        - note that we can use this simple bash func that very helpful for us 
            ``` bash
            get_shodan_details () {
                    curl -s https://internetdb.shodan.io/$1 | jq -r
            }
            ```
            - note that in this function we get some information that maybe interesting.
                - like ports (opens), even there are vulnerabilities
                ```
                    {
                      "cpes": [
                        "██████████"
                      ],
                      "hostnames": [],
                      "ip": "█████████",
                      "ports": [
                        80
                      ],
                      "tags": [],
                      "vulns": []
                    }
                ```
        - for doing port scan we can use [Naabu](https://github.com/projectdiscovery/naabu)
            - interesting ports for scan (complete command): `echo IP_ADDRESS | naabu -p 80,8000,8080,8880,2052,2082,2086,2095,443,2053,2083,2087,2096,8443,10443 -silent`
            - founds are interesting but 99% all of them are **Internal ports**
    - search on CIDRs and before that search for other assets on this organization on the Certificate Issuer and the good news is that the provider is the company and we can goes forward.
    
Greats!
