# Day1 `25-Mar-2025`
- Hello there, after near by 1.5 months, Now I'm going to continue my hunting challenge, I know that the dicipline is too hard but I've trying :)
- Note that I've been working for 6 days but I've delete them and start again for more focus
- So let's start!
- focus on specific domain
- gathered all the subdomains
- use `dnsx` for find up or live subdomains then do service discovery for find best place to work
- in meanwhile we can do dorking
  - arrive to an endpoint that possible to injection trying the sqlmap for that with `python3 sqlmap.py -r r.txt --risk 3 --batch` command -> we got blocked!
  - arrive to another endpoint that is a simple web app that maybe interesting so let's check the wayback machine
  - trying to directory fuzz with `ffuf` so arrived to some interesting paths
- so nothing specific found, but the recon is interesting
- I've been arrive to an IP address so best practice??
  - nmap is good
- another endpoit point to a cms that interesting, so trying to directory fuzz and then arrive to the login page, and a legit url that interesting to do fuzz based on it `https://domain.tld/index.php`
  - but nothing interesting
- again another endpoint that is interesting
- For tomorrow with more focus work on this specific url that can do too many works!

Hope this time we don't have any break!
