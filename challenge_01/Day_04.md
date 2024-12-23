# Day4 `23-Dec-2024`
- do wide recon on ring company
    - subdomain discovery
        - via crt.sh
            - bash function `crt_sh () {
    while IFS= read -r domain; do
        curl -s "https://crt.sh/?q=$domain&output=json" | jq -r '.[] | .common_name, .name_value' | sort -u
    done
}`
            - with this command `cat domains | while read domain in domains; do crtsh $domain | sort -u >> $domain.crtsh; done`
        - via [subfinder](https://github.com/projectdiscovery/subfinder)
            - with this command `for domain in $(cat domains.txt); do subfinder -d $domain -all -silent | sort -u >> $domain.subfinder;done`
    - do name resolution
        - via dnsx
            - `cat domain.tld.* | dnsx -silent | sort -u >> domain.tld.dnsx`
    - do service discovery
        - via httpx
            - with this command `cat domain.tld.* | httpx -silent -follow-host-redirects -title -status-code -cdn -tech-detect -H "User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:108.0) Gecko/20100101 Firefox/108.0"`
        - work on interesting results

today I've been sick but trying to stick to the plan.
