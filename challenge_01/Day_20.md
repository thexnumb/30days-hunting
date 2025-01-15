# Day20 `15-Jan-2025`
- for today I'm going to work on the results of the wide recon that contains of:
    - Subdomain enumuration, service discovery, directory discovery
- so let's go.
- in the found urls, I found the favicon of the one of the applications of the program so we can find other and more assets
- about the favicon script to do this, it's simple, use `mmh3` python library for hash and `codec` for encode.
- in here there is no new asset that being helpful for us so go the the rest of the urls.
- checking almost 600 urls and most of them are useless just in some case found some JS files that may help us.
- in this step let's review what we have done till now
    - completely wide recon for tree main domain, use `web archive` to see if there is hidden or far away file or endpoint.
    - act like normal user on three main domains
    - look for functionalities
    - the biggest failure is that can't login with email that should be an specific country,
    - there are many api endpoints that do lots of job for the application but nothing interesting appears.
- repeat the loop for cover any overlook and misses.
- after bunch of trying arrive to a open ssh port on the server of the application, now best way is to trying to check weak credentials or other things.

before finished today, ==it's good to say that if you are in any level with any state just keep going, try and hard work day by day, even not hard work or even not too much try just do it day by day it's a miracle.==

I've think it's enough for today but the first job for do tomorrow is this SSH server!
