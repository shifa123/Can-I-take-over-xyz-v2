
![Screenshot](canitakeoverallxyz.png)

## Disclaimer :warning:

**The authors of this document take no responsibility for correctness. This project is merely here to help guide security researchers towards determining whether something is vulnerable or not, but does not guarantee accuracy. This project heavily relies on contributions from the public; therefore, proving that something is vulnerable is the security researcher and bug bounty program's sole discretion. On top of that, it is worth noting that some bug bounty programs may accept dangling DNS record reports without requiring proof of compromise.**

## What is a subdomain takeover?

> Subdomain takeover vulnerabilities occur when a subdomain (subdomain.example.com) is pointing to a service (e.g. GitHub pages, Heroku, etc.) that has been removed or deleted. This allows an attacker to set up a page on the service that was being used and point their page to that subdomain. For example, if subdomain.example.com was pointing to a GitHub page and the user decided to delete their GitHub page, an attacker can now create a GitHub page, add a CNAME file containing subdomain.example.com, and claim subdomain.example.com.

You can read up more about subdomain takeovers here:

- <https://labs.detectify.com/2014/10/21/hostile-subdomain-takeover-using-herokugithubdesk-more/>
- <https://www.hackerone.com/blog/Guide-Subdomain-Takeovers>
- <https://0xpatrik.com/subdomain-takeover-ns/>

## Safely demonstrating a subdomain takeover

Based on personal experience, claiming the subdomain discreetly and serving a harmless file on a hidden page is usually enough to demonstrate the security vulnerability. Do not serve content on the index page. A good proof of concept could consist of an HTML comment served via a random path:

```
$ cat aelfjj1or81uegj9ea8z31zro.html
<!-- PoC by username -->
```

Please be advised that this depends on what bug bounty program you are targeting. When in doubt, please refer to the bug bounty program's security policy and/or request clarifications from the team behind the program.

## How to use this project

I recommend searching for the name of the service you are targeting in the issues tab. That way you can see the on-going discussion and more detailed steps on how to claim the subdomain you are after.

## How to contribute

You can submit new services here: https://github.com/EdOverflow/can-i-take-over-xyz/issues/new?template=new-entry.md.

A list of services that can be checked (although check for duplicates against this list first) can be found here: https://github.com/EdOverflow/can-i-take-over-xyz/issues/26.

# All entries
