# Day18 `13-Jan-2025`
- for today we are going to refresh and review and act like normal user keep note of each part of the application
- note that in my opinion the application mapping is so important becuase addition to help organize your mind help to have a clean view of the application.
- in meanwhile walking through the application arrive to and API endpoint that is POST a value that is the view count of a article so we can delete the cookie of that request so we can increase the view of the article without even the site know that we are the same user and it's a Business Logic.
- so keep going.
- something interesting got my attention. postmessages
    - take a look at it.
    - there is nothing interesting
- arrive to a API endpoint that get report ID and give you a json response that contains two field: html and data
    - at the first we trying simple IDOR and yes we can see others.
    - some creepy programming is in here but for now leave it away.
- only way for register is the OTP code and only accept specific country so enter a legit number to see the behavior and boom. it's fantastic that we have 1 minute time and we can enter unlimited verification code in there and the interest thing is that it's only 4 digits.
    - I've made a mistake that is the limit for 5 try to enter OTP code
- find another domain of this application that have a registration field that get number from any country but that need the admin approval
- find another api endpoint that return jobs ofers
    - best job to do in here is fuzzing.
        - in this api we have a route that is valid and we can use it to check that we still alive or kill by the sever.
        - `ffuf -w wordlist.txt -u https://domain.tld/api/career/FUZZ -mc all -c -fl 8,14,33 -H "User-Agent: Legit user agent" -H "Cookie: ████████████████" -t 10`
- arrive to another API endpoint that get the path and give the phone number, in other product of this application that needs to use captcha but in here no. let's see what can I do.
- there is no point so we skip it.
- after some exploring arrive to an API endpoint that get the part of path and return the phone number of that with no captcha or even authentication for see the number of that product. so there is a vulnerability.

Think that it's enough for today and for the rest of the day trying to learing and training more and more :) See ya...
