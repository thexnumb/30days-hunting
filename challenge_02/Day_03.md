# Day3 `27-Mar-2025`
- As you know from the earlier day, we arrived at a domain that is so interesting, because that domain not listed on the policy but we know that and approved that the domains is belong to the program.
  - why we do this? it's simple less arrival to this domain more vulnerabilities can found!
  - so this domains is tooooooo lazy and not work property
  - after some time spending on the recon process we arrive to a URL that exposed all the list bucket of AWS S3 bucket, that we can do?
    1. Public Access Misconfiguration
      1. original domain is `https://redacted.domain.com/`
      2. trying to test `https://redacted.domain.com.s3.amazonaws.com/` and it work
      3. Know if we can download files, then it's a vulnerability that lead sensitive data exposed
   
Send the report, I think it's enough for today!
