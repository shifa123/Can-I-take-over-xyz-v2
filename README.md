
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
$ cat index.html
<!-- PoC by Hacker -->
```

Please be advised that this depends on what bug bounty program you are targeting. When in doubt, please refer to the bug bounty program's security policy and/or request clarifications from the team behind the program.

## How to use this project

I recommend searching for the name of the service you are targeting in the issues tab. That way you can see the on-going discussion and more detailed steps on how to claim the subdomain you are after.

## How to contribute

You can submit new services here: https://github.com/shifa123/ALLsubdomaintakeovers/issues/new?template=new-entry.md


# All entries

Engine                                        | Status         | Old Fingerprint                                                             | New Fingerprint                                                 | Documentation
--------------------------------------------- | -------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------
Acquia | Not vulnerable | `Web Site Not Found` |`If you are an Acquia Cloud customer and expect to see your site at this address` ``|[Issue #103](https://github.com/EdOverflow/can-i-take-over-xyz/issues/103)
Aftership | Vulnerable | |`Oops.</h2><p class="text-muted text-tight">The page you're looking for doesn't exist.`
Agile CRM | Vulnerable | `Sorry, this page is no longer available.` |`Sorry, this page is no longer available`
Aha | Vulnerable | |`There is no portal here ... sending you back to Aha!`
Airee.ru                             | Vulnerable     | | `Ошибка 402. Сервис  Айри.рф  не  оплачен` |
Anima | Vulnerable |`If this is your website and you've just created it, try refreshing in a minute` |`If this is your website and you've just created it, try refreshing in a minute`
Akamai                                        | Not vulnerable | | Not Vulnerable
AWS/S3                             | Vulnerable     | `The specified bucket does not exist`                                   | `The specified bucket does not exist`
Bigcartel                       | Vulnerable     | | `<h1>Oops! We couldn&#8217;t find that page.</h1>`
Bitbucket                       | Vulnerable     | `Repository not found`                                                  | `The page you have requested does not exist`
Brightcove                       | Vulnerable     | | `<p class="bc-gallery-error-code">Error Code: 404</p>`
Campaign Monitor         | Vulnerable     |               `Trying to access your account?` |               `<strong>Trying to access your account?</strong>` 
Canny         | Vulnerable     |               `Trying to access your account?` |               `Company Not Found` 
Cargo         | Vulnerable     |               |     `If you're moving your domain away from Cargo you must make this configuration through your registrar's DNS control panel.` 
Cargo Collective        | Vulnerable     |               `404 Not Found` |               `<div class="notfound">` 
Cloudfront       | Not vulnerable     |               `ViewerCertificateException` |               
 Desk       | Vulnerable     |               `Please try again or try Desk.com free for 14 days.` |               `this help center no longer exists` 
  Digital Ocean       | Vulnerable     |               `Domain uses DO name serves with no records in DO.` |             
   Discourse       | Vulnerable     |           
   Fastly       | Edge case     |               `Fastly error: unknown domain:` |               `Fastly error: unknown domain:`
   Feedpress       | Not vulnerable     |               `The feed has not been found.` |     `The feed has not been found.`          
 Firebase       | Not Vulnerable     |                | 
  Fly.io       | Vulnerable     |               `404 Not Found` |               
   Freshdesk       | Not vulnerable     |                |                         
   Gemfury       | Vulnerable     |               `404: This page could not be found.` |          `404: This page could not be found.`     
   Ghost       | vulnerable     |               `The thing you were looking for is no longer here, or never was` |     `The thing you were looking for is no longer here` 
   Github       | vulnerable     |               `There isn't a Github Pages site here.` |     `There isn't a GitHub Pages site here.`          
 Gitlab       | Not Vulnerable     |                | 
  Google Cloud Storage      | Vulnerable     |               `NoSuchBucket The specified bucket does not exist.` |       |
   HatenaBlog       | Vulnerable     |               `404 Blog is not found` |          `404 Blog is not found`     
   Help Juice       | vulnerable     |               `We could not find what you're looking for.` |     `We could not find what you're looking for.`  |
Help Scout       | Vulnerable     |               `No settings were found for this company:` |          `No settings were found for this company:`     
   Heroku       | Edge case     |               `No such app` |     `There's nothing here, yet.` 
  Instapage       | Non Vulnerable     |                |              
   Intercom       | vulnerable     |               `Uh oh. That page doesn't exist.` |     `This page is reserved for artistic dogs.` 
   JetBrains       | Vulnerable     |               `is not a registered InCloud YouTrack` |          `is not a registered InCloud YouTrack.`     
   Key CDN       | Not vulnerable     |                |     
   Kinsta       | Vulnerable     |               `No Site For Domain` |          `No Site For Domain`     
   LaunchRock       | vulnerable     |               `It looks like you may have taken a wrong turn somewhere. Don't worry...it happens to all of us.` |     `It looks like you may have taken a wrong turn somewhere. Don't worry...it happens to all of us.` 
   Mashery       | Edge Case     |               `Unrecognized domain` |          `Unrecognized domain <strong>`     
   Microsoft Azure       | vulnerable     |                |     
   Netlify       | Edge Case     |                |    `Not Found`           
   Ngrok       | vulnerable     |               `Tunnel *.ngrok.io not found` |     `ngrok.io not found` 
   Pantheon       | Vulnerable     |               `404 error unknown site!` |          `The gods are wise, but do not know of the site which you seek.`     
   Pingdom       | vulnerable     |               `This public report page has not been activated by the user` |     `Public Report Not Activated` | 
   Readme.io       | Vulnerable     |               `Project doesnt exist... yet!` |          `Project doesnt exist... yet!`     
   Sendgrid       |Not vulnerable     |                |    
   Shopify       | Vulnerable     |               `Sorry, this shop is currently unavailable.` |          `Only one step left!`     
   SmartJobBoard       | vulnerable     |               `This job board website is either expired or its domain name is invalid.` |     `Job Board Is Unavailable` 
   Squarespace       | Not Vulnerable     |                |              
   Statuspage       | Not vulnerable     |                |     
   Strikingly       | Vulnerable     |               `page not found` |          `But if you're looking to build your own website`     
   Surge.sh       | vulnerable     |               `project not found` |     `project not found` | 
   Tumblr       | Edge Case     |               `Whatever you were looking for doesn't currently exist at this address` |          `There's nothing here.`     
   Tilda       |  Edge Case     |              `Please renew your subscription` |     `<title>Please renew your subscription</title>` | 
 Uberflip       | Vulnerable     |               `Non-hub domain, The URL you've accessed does not provide a hub.` |          `Non-hub domain, The URL you've accessed does not provide a hub.`     |
  Unbounce       | Edge Case     |               `The requested URL was not found on this server.` |     `The requested URL was not found on this server.` 
  Uptimerobot       | Vulnerable     |               `page not found` |          `page not found`     
   UserVoice       | vulnerable     |               `This UserVoice subdomain is currently available!` |     `This UserVoice subdomain is currently available!` 
   Webflow       | Edge Case     |               `The page you are looking for doesn't exist or has been moved.` |          `<p class="description">The page you are looking for doesn't exist or has been moved.</p>`     
   Wordpress       | vulnerable     |               `Do you want to register *.wordpress.com?` |     `Do you want to register` 
   Worksites       | Vulnerable     |               `Hello! Sorry, but the website you&rsquo;re looking for doesn&rsquo;t exist.` |          `Company Not Found | you&rsquo;re looking for doesn&rsquo;t exist`     |
   WP Engine       | Not vulnerable     |                |  
   Zendesk       | Not vulnerable     |    `Help Center Closed`            |      
    
    
   
          
