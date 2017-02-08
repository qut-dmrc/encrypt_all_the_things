---
title: Encrypt all the things!!!
theme: css/theme/simple.css
---

<img src="http://blog.serverfault.com/files/2016/02/encrypt-all-the-things1.png" width=40%/>

**... but don't forget your keys.**

*(Digital Privacy & Security for Researchers)*

QUT DMRC Summer School 2017

Brenda Moon & Felix Victor Münch

<font size=0.5>image: http://blog.serverfault.com/files/2016/02/encrypt-all-the-things1.png
(based on original by http://hyperboleandahalf.blogspot.com.au/)
</font>

---

# Why are we here?

Note:
* Over the next 2 hours we are going to explore common security and privacy concerns for researchers & some solutions to them.
* To get started thinking about security & privacy let's run through a few examples.
* use of coloured stickynotes - red one: help, green one: finished activity.
* asking questions

----

## Metadata retention

*The Assignment*

You, a data analyst for the Australian police, are on the train heading home when your phone starts buzzing. You got a text from your boss, who is asking you to take a look at your work emails. You reluctantly open your mailbox only to find the following email:

Note:
* Snitchhunt is a game designed by Gabor Szathmari of CryptoParty Sydney to demonstrate how metadata can be used to track our movements.

----

```txt
From: Finn Coburn <finn.coburn@thepolice.com> To:
data-analysts@thepolice.com Date: 2016-12-10 10:58 Subject:
Fixing a leak at Minecorp

Good morning analysts,

[...]

It seems there is a whistleblower at Minecorp leaking to a
journalist at MineWatch.

[...]

May I remind you that the mines in Australia are all
critical infrastructure, [...]. Therefore, we need
to identify the person of interest to put him/her under
arrest.
```

----

```txt
So I need you to dig this guy up for me. [...]

All logs you will need for the investigation should be
available on Kibana. You will need to solve the preceding
tasks before moving on to the next.

Do not forget to have a look on the Kibana cheat sheet that
Sharon put together last week for us.

Keep me updated and let me know if you get stuck. I need the
info to be submitted here by no later than 2:30 pm.

FINN COBURN CHIEF DATA OFFICER COMPUTER CRIME SQUAD Tel:
16131 www.thepolice.com
```

https://snitchhunt.org/challenge

Note:
* This is a privacy and security risk faced by everyone, not just researchers.
* Would any of you like to suggest a definition of metadata?
* One way of considering metadata is as activity records - records of what you have done and when, but not the content of what you have done.

----

<img src='https://dl.dropboxusercontent.com/s/xfeqp79r5lv1wxq/2017-01-31%20at%203.23%20pm.png' width="70%">

(http://www.abc.net.au/triplej/programs/hack/how-team-of-pre-teens-found-whisteblower-using-metadata/8113668)

Note:
* You might imagine this to be very difficult, but working with realistic data and tools a team of pre-teens identified the whistleblower in less than 2 hours
* The original website has been taken down but Rosie Williams (@info_aus) has made a new online version and a link to that is included in resources at the end of this presentation
* HANDOVER

----

# worst case scenarios

----

## weak password reuse

your Twitter accounts is hacked by angry gamergaters, and suddenly your devices are wiped

----

### Activity

Visit https://haveibeenpwned.com/ and look up your most used email address, to see whether your data has been published after a successful cyber attack or data breach.

Note:
* Define pwned - 'Owned'
* demo first on our own account.
* now go ahead and check your email

----

## revealing IP address

researching in extremist bulletin boards/social networks
getting harassed in your neighbourhood afterwards

----

## unencrypted communication

communication with protesters in an authoritarian surveillance state via iMessage but message gets sent via SMS service

----

## unencrypted devices

interview with journalist in country oppressing the press with 'off-the-record' content on unencrypted Android phone gets confiscated at the airport before leaving the country.

Note:
* even if something similar might have happened, all examples are made up
* also: Felix's stolen hard drive
* 15 minutes in!

----

# Why are you here?

What do you want to get out of this session?
What privacy or security issues might effect your research?
Discuss in groups (5 minutes)

Note:
* break into groups
* discuss what privacy or security issues might effect your research & summarise on butchers paper
* each group report back

---

# Passwords
one ring to rule you all

----

## Main risks

When you've been pwned:

* common password (qwerty, 12345, monkey, love, ...) <!-- .element: class="fragment" -->
* easy to guess (qwerty12345, your name, your birthday, your partners birthday, your postcode, ) <!-- .element: class="fragment" -->
* reuse of passwords <!-- .element: class="fragment" -->
* storing password in an unsafe place (i.e. unencrypted and accessible from outside) <!-- .element: class="fragment" -->
* forgetting your password <!-- .element: class="fragment" -->

Note: 25 minutes in!

----

## Solution #1:

### Use a password manager

Note:
QUESTIONS:
* Who is using a password manager?
* Which one?

----

## What is a password manager?

* allows you to access all your passwords with a master password and/or keyfile ("secret file", e.g. on a USB stick) <!-- .element: class="fragment" -->
* stores passwords in an encrypted file (i.e. not readable without a key) <!-- .element: class="fragment" -->
* can often generate secure passwords for you <!-- .element: class="fragment" -->

Therefore your passwords will be strong, will not be reused, and you don't have to worry about memorising them anymore. <!-- .element: class="fragment" -->

----

## We recommend

* KeePass, KeePassX, KeeWeb
    * Open source +
    * interoperable +
    * high reputation +
    * free +
    * not so convenient -
* 1Password
    * high reputation +
    * very convenient +
    * costs money -
    * closed source -

Note:
* links to all these are provided on the resources page at end of presentation
* HANDOVER

----

## Solution #2:

### Use 2-factor authentication

----

## What is 2-factor authentication?

* similar to one time passwords for online banking<!-- .element: class="fragment" -->
* something you know (your password) and something you have (your device)<!-- .element: class="fragment" -->
* having device is verified by either<!-- .element: class="fragment" -->
  * sending second code to you by SMS or<!-- .element: class="fragment" -->
  * generating it in an App on your device<!-- .element: class="fragment" -->
* this second element changes each time<!-- .element: class="fragment" -->

Note:
* most secure forms of this are bound to a device you carry with you, e.g. an app on your phone, or even more secure on a dedicated device
* best practice internet services have it, if service you are using doesn't it might be a warning sign

----

## SMS is not a secure channel!

![Due to today's incident, it's possible some SMS messages were incorrectly delivered. All messages will be held while we resolve the issue.](TelstraSMSProblemsTweet.png)

Note:
* Last week Telstra (Australian telecom provider) outage caused by fire in Sydney exchange resulted in many SMS's being delivered to wrong phones

----

## SMS problems

* misdelivery
* unauthorised phone number porting
* not available during phone outages
* not encrypted - can be intercepted with scanner

Note:
* There have been examples in news lately of people repeatedly having their numbers ported just using their name and DOB as authorisation
* Same Telstra outage last week stopped people receiving SMS for 2FA

----

## We recommend

Use an app for 2 factor authentication:

* [FreeOTP](https://freeotp.github.io/)
* [Google Authenticator (Android/iPhone/BlackBerry)](https://support.google.com/accounts/answer/1066447?hl=en)
* [Amazon AWS MFA (Android)](https://www.amazon.com/gp/product/B0061MU68M)
* [Authenticator (Windows Phone 7)](https://www.microsoft.com/en-us/store/p/authenticator/9wzdncrfj3rj)

Note:
* links to these are provided in the resources section

----

# Group activity!

Find out whether one of your most used services provides 2-factor-authentication

Note:
* break into groups (5 minutes? - shorter?)
* green sticky note when finished
* check if services you use support 2fa
* make list on butchers paper of ones that do / don't
* each group report back (put up butchers paper on walls)

---

# Communication

----

## Main risks

While transmitting sensitive information: the men in the middle

* your email/messaging provider or anybody who has hacked them or pretends to be them <!-- .element: class="fragment" -->
* authorities who subpoena any of your communication providers <!-- .element: class="fragment" -->
* others in open/untrusted WiFi <!-- .element: class="fragment" -->

<img src="img/wifi-ios.png" class="fragment" width="40%">

Note:
* Email is like a postcard, even the post office can read it
* HANDOVER

----

## Solution #1:

### https

----

## What is https?

* browser checks whether website has a valid certificate ('ID card')
* encrypts traffic between browser and website

----

## We recommend

* check the address bar in your browser
![](https://dl.dropboxusercontent.com/s/64u41gygdnzk0k8/2017-02-05%20at%201.41%20pm.png)

* https://www.eff.org/https-everywhere


Examples for bad certificates: https://badssl.com/

Note: HTTPS Everywhere is a Firefox, Chrome, and Opera extension that encrypts your communications with many major websites
----

## Solution #2:

### PGP encryption

"Pretty Good Privacy"

----

## What is PGP encryption?

* Encryption protects your information so that no one except the intended recipient can read it.

* PGP adds two extra features by using a Public key:
  * it allows you to encrypt information for a recipient without contacting them first - using their Public key
  * you can verify that information signed by them is from them

----

## We recommend

* [keybase](https://keybase.io/)
* [GPGTools](https://gpgtools.org/)
* [Enigmail for Thunderbird](https://www.enigmail.net/index.php/en/)
* email clients with GPG support

----

# Group activity!

Get an account on [keybase.io](https://keybase.io) and encrypt a message to somebody else in this workshop. Send it to their email address. Decrypt a message that someone sends you.

I'll demonstrate the steps required so you can follow along, and there are screenshots showing the process in the slides file in dropbox.

----

![](https://dl.dropboxusercontent.com/s/e2vg3x415glbnh9/2017-02-07%20at%2011.08%20am.png)

----

![](https://dl.dropboxusercontent.com/s/mvrvjzyqp1uf71a/2017-02-07%20at%2011.17%20am.png)

----

![](https://dl.dropboxusercontent.com/s/5y598qvy1oa9ygf/2017-02-07%20at%2011.23%20am.png)

----

![](https://dl.dropboxusercontent.com/s/prfjqs88civ456n/2017-02-07%20at%2011.25%20am.png)

----

![](https://dl.dropboxusercontent.com/s/vvlzxh1mvqtwpdj/2017-02-07%20at%2011.27%20am.png)

----

![](https://dl.dropboxusercontent.com/s/kmknfxop96hf2lr/2017-02-07%20at%2011.30%20am%20%281%29.png)

----

![](https://dl.dropboxusercontent.com/s/tjh16s4657prk8n/2017-02-07%20at%2011.36%20am.png)

----

![](https://dl.dropboxusercontent.com/s/1b42dt1x2s43q7y/2017-02-07%20at%2011.39%20am.png)

----

![](https://dl.dropboxusercontent.com/s/pgn4sgj9iy1248k/2017-02-07%20at%2011.43%20am.png)

----

![](https://dl.dropboxusercontent.com/s/spgf964aqxkt0lg/2017-02-07%20at%2011.47%20am.png)

----

![](https://dl.dropboxusercontent.com/s/oux1ofn7ji2ocl7/2017-02-07%20at%2011.50%20am%20%281%29.png)

----

![](https://dl.dropboxusercontent.com/s/csjpyeerxciss61/2017-02-07%20at%2011.52%20am.png)

----

![](https://dl.dropboxusercontent.com/s/rc7e96xidr4anwe/2017-02-07%20at%2011.55%20am.png)

----

![](https://dl.dropboxusercontent.com/s/4or33xht5wp2j6c/2017-02-07%20at%2011.57%20am%20%281%29.png)

----

## Whoot! So how did that work?

Let's call the public key a 'padlock'.

----

Red has a secret message for Green

<img src="PGP/PGP1.png" width=70%>

----

Red encrypts message with Green's public padlock

<img src="PGP/PGP2.png" width=70%>

----

Sent message is unreadable without Green's secret key

<img src="PGP/PGP3.png" width=70%>

----

Green decrypts the message with their secret key

<img src="PGP/PGP4.png" width=70%>

----

Done :)

<img src="PGP/PGP5.png" width=70%>

----

## Using PGP to sign things

As well as encrypting messages and files, PGP can be used to sign things:
* PGP signature verifies content and sender of item
* can be used to certify unencrypted emails or files
* will fail if message or file is changed

----

## Using PGP to verify identities

PGP can also be used to verify peoples public keys - by signing a public key you are saying you are confident that the key belongs to the person it says it belongs to.

On keybase this is done by Following people - consider following some of the other people in this workshop while you know that the account is really them.

----

## And how does signing work?

That's where the metaphor stops working. Ask later :)

----

## Solution #3:

### Secure messenger / Private messaging

----

## What is a secure messenger?

* encrypts message end-to-end per default (i.e. messages are only readable by sender and recipient, not by the message service provider)
* explicitly does not store activity records (metadata)
* is open source
* optional: has self-destructing messages (i.e. messages are deleted on both ends after a pre-defined timespan)

----

## We recommend

[Signal](https://whispersystems.org/)

----

# Safely using secure messaging and encryption

* make sure you confirm that the account you are dealing with (Public key or Signal account) is who you expect to be at the other end
  * verify using separate channel
  * for chat, make sure encryption is working before exchanging any critical informaiton
* your Keybase account is good for improving security, but you should create fresh PGP keypairs for very secure communications

Note: Get expert advice, may also need to setup more secure computer

---

# Researcher privacy

----

## Main risks

when researching on the internet:

* activity record (metadata) retention (by state/institution/ad networks)
    * by IP address (like a 'phone number' for your computer)
    * by browser cookies (like customer cards in shops, just for your browser)
* revealing of personal details to website owners
* other forms of browser finger printing

Note:
* your IP address may reveal your location, and stays the same at least during a single session, and possibly all the time. This means it can be used to track your visits across multiple websites
* browser cookies are stored on your computer and used to customise your experience of a website, but can also be used to track your use of a website and even between websites.
* if you login to a website you have provide your account details to that website and to your IP address
* new ways of identifying website visits are always being explored, for example using which fonts your browser reports as a finger print to identify your browser.

----

# Activity!

visit https://browserleaks.com

Note:
* QUESTION: Any surprises?

----

## Solution #1:

### Virtual Private Network
### VPN 'tunnel'

----

## What is a VPN?

* prevents eavesdropping, e.g. in an open WiFi
* hides your IP address (i.e. location, internet provider, other visited websites) from servers you communicate with
* can make you appear to be in another country and circumvent DNS or geo-blocking
* does NOT replace https

----

## We recommend

Choose a VPN service which:

* claims not to store activity records (hard to verify)
* uses OpenVPN
* has servers in safe jurisdictions
* not insert advertising into your browsing stream

Remember that if it's too cheap you might be paying in other ways.

[NordVPN](https://nordvpn.com/) and [Private Internet Access](https://www.privateinternetaccess.com/) both have a long term high reputation

----

## Solution #2:

### Tor Browser

----

## What is Tor Browser?

* provides secure browser that doesn't leave traces (e.g. it does not store cookies)
* onion-network (encrypted tunnel through encrypted tunnel through encrypted tunnel ...)
* does not prevent you from disclosing your identity e.g. by logging into Facebook

----

## We recommend

Use for TorBrowser high risk research, not for everyday use.

Note: for high risk research get expert advice!

----

# Group activity!

Install Tor Browser and visit https://browserleaks.com again.

Tor Browser: https://www.torproject.org/projects/torbrowser.html.en

Note:
* Explain about using signatures to verify downloads?
* What did you find was different in browserleaks report?
* HAND OVER

---

# Data storage

----

## Main risks

when storing data:

* unauthorised access to data, e.g. in the cloud
* unwanted access to devices, e.g. at airports
* data loss
* lost access

----

## Solution

----

# backup, backup, backup

3 independent copies

Note: research storage - QUT provides properly tape backed up storage for research data (rstore).

----

AND

----

![](http://blog.serverfault.com/files/2016/02/encrypt-all-the-things1.png)

**... but don't forget your keys.**
*(hint: use a password manager)*

----

## We recommend

* full device/disk/USB stick … encryption (mostly provided by OS)
* for files in the cloud:
    * [Cryptomator](https://cryptomator.org/)
    * [keybase](https://keybase.io/)
    * disk image encryption by your operating system

MAKE SURE YOU NEVER LOOSE YOUR KEYS OR PASSPHRASES!!! Or all will be lost.

Note:
* Most encryption services offer multiple ways of storing your keys or passphrases - take advantage of them, but make sure you store the keys or passphrases securely.
* HAND OVER

---

# How to choose a tool?

----

## Things to consider

1. Open Source?<!-- .element: class="fragment" -->
2. Reputation?<!-- .element: class="fragment" -->
3. Independent security audit?<!-- .element: class="fragment" -->
4. Will you actually use it?<!-- .element: class="fragment" -->

---

# Where to from here?

At end of the presentation there is a list of all the software we've mentioned today and a list of useful websites for more information.

Depending on the level of risk to you or your research participants you may need to seek advice from a security/privacy expert before you begin your research.

Note:
* Risks/Solutions are changing over time, so important to get current advice before you start your research.

---

# Group activity!

Discuss in your groups how what we have covered today applies to your research.

---

Questions?

---

# Resources

----

## Password manager

* 1Password https://1password.com/
* KeePass http://keepass.info/
* KeePassX https://www.keepassx.org/
* KeeWeb https://keeweb.info/

----

## 2-factor-authentication

* Amazon AWS MFA (Android) https://www.amazon.com/gp/product/B0061MU68M
* Authenticator (Windows Phone 7) https://www.microsoft.com/en-us/store/p/authenticator/9wzdncrfj3rj
* FreeOTP https://freeotp.github.io/
* Google Authenticator (Android/iPhone/BlackBerry) https://support.google.com/accounts/answer/1066447?hl=en

----

## Privacy

* Browser leaks https://browserleaks.com
* HTTPS Everywhere https://www.eff.org/https-everywhere
* NordVPN https://nordvpn.com/
* Private Internet Access https://www.privateinternetaccess.com/
* Tor Browser: https://www.torproject.org/projects/torbrowser.html.en

----

## file/device/communication encryption

* Cryptomator https://cryptomator.org/
* Enigmail for Thunderbird https://www.enigmail.net/index.php/en/
* GPGTools https://gpgtools.org/
* keybase https://keybase.io/
* Signal https://whispersystems.org/

----

## websites

* CryptoParty https://www.cryptoparty.in/
* Electronic Freedom Foundation (EFF)
  * Privacy https://www.eff.org/issues/privacy
  * Surveillance Self-Defense https://ssd.eff.org/
    This has overviews, tutorials, and detailed guides for specific situations.
* Snitch Hunt Game http://whistleblower.network/snitch/index.php
* Snitch Hunt news article http://www.abc.net.au/triplej/programs/hack/how-team-of-pre-teens-found-whisteblower-using-metadata/8113668
* Examples of Bad SSL certificates https://badssl.com/

---

# Glossary of terms

* browser cookies: like customer cards for your browser to store information about you that can be read by the website when you return
* encryption: making data practically unreadable without another piece of data (see keyfile) and/or password that's usually kept secret
* end-to-end encryption: encryption from a senders device to a recipient device without intermediaries being able to decrypt

----

# Glossary of terms

* https: HTTP over SSL https://en.wikipedia.org/wiki/HTTPS
* IP address: number to identify your computer/router to another computer, mostly a server serving you a website
* keyfile: think of it as a password, but in a file.
* metadata: activity records (https://twitter.com/Snowden/status/661305566967562240) or more detailed: https://ssd.eff.org/en/glossary/metadata
* ssl or tsl: Secure Sockets Layer / Transport Layer Security https://en.wikipedia.org/wiki/Transport_Layer_Security

---

![](https://abs.twimg.com/icons/apple-touch-icon-192x192.png)

@brendam
@flxvctr

QUT DMRC Summer School 2017
