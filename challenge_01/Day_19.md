# Day19 `14-Jan-2025`
- for today continue to mess with the application and work with it. as I've said always knowing application is the best to find more application.
- again find another API endpoint and the best work in here to doing fuzz and hope found something interesting.
- no result so I've think should start the wide recon again.
- note that in todays wide recon is so hard to help us to directly find vulnerability but it help us increase attack surface
- before wide recon, the first step that I've start is to open debugger and trying to track behaviors of the application for each action.
- maybe this is kind of recon but this is more hackery thing to run and do some specific jobs that all the scripts in the world can do that.
- after some lozy browsing on the JS files then arrive the an Endpoint that make me to think that maybe this should be vulnerable to injection, so run SQLmap on it and do other works.
- after a while on exploring finally arrive to an endpoint that is like a function that based on input do action and the input is sanitize via regex or something like this that start with specific word and the rest can be anything
