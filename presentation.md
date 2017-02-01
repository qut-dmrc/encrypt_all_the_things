---
title: Encrypt all the things!!!
theme: css/theme/simple.css
---

![](http://blog.serverfault.com/files/2016/02/encrypt-all-the-things1.png)

**... but don't forget your keys.**

*(Digital Privacy & Security for Researchers)*

DMRC Summer School 2017

Brenda Moon & Felix Victor Münch

---

# Why are we here?

----

## Metadata retention

*The Assignment*

You are on the train heading home when your phone starts buzzing. You got a text from your boss, who is asking you to take a look at your work emails. You reluctantly open your mailbox only to find the following email:

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

----

<img src='https://dl.dropboxusercontent.com/s/xfeqp79r5lv1wxq/2017-01-31%20at%203.23%20pm.png' width="70%">

(http://www.abc.net.au/triplej/programs/hack/how-team-of-pre-teens-found-whisteblower-using-metadata/8113668)

----

# worst case scenarios

----

## weak password reuse

getting Twitter hacked by angry gamergaters, and suddenly your devices are wiped

----

Visit https://haveibeenpwned.com/ and look up your most used email address.

----

## revealing IP address/VPN

researching in extremist bulletin boards/social networks
getting harrased in your neighbourhood afterwards

----

## unencrypted communication

Iranian protester communicates via iMessage but message gets sent via SMS service

----

## unencrypted devices

interview with journalist in Turkey with 'off-the-record' content on unencrypted Android phone gets confiscated at the airport before leaving the country.

Note:
* even if something similar might have happened, all examples are made up
* 15 minutes in!

---

# Group activity!

----

# Why are you here?

What do you want to get out of this session. Discuss in groups (5 minutes)

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
QUESTION: Who is using a password manager?
Which one?

----

## What does it and how?

* stores passwords in an encrypted, i.e. secure file
* allows you to access all your passwords with a master password and/or keyfile
* can often generate secure passwords for you

Therefore your passwords will be **strong**,  will **not be reused**, and you don't have to worry about **memorising** them anymore.

----

## We recommend

* KeePass, KeePassX, KeeWeb
    * Open source +
    * interoperable +
    * free +
    * not so convenient -
* 1Password
    * high reputation +
    * very convenient +
    * costs money -
    * closed source -

----

## Solution #2:

### Use 2-factor-authentication

----

## What does it and how?

----

## We recommend

Rather use an app than SMS

----

# Group activity!

Find out whether one of your most used services provides 2-factor-authentication

---

# Communication

----

## Main risks

While transmitting sensitive information: the men in the middle

* others in open/untrusted WiFi <!-- .element: class="fragment" -->
* your email/messaging provider or anybody who has hacked or pretends to be them <!-- .element: class="fragment" -->
* authorities who subpoena any of your communication providers <!-- .element: class="fragment" -->

----

## Solution #1:

### PGP encryption

----

## What does it and how?

* puts a padlock on anything you want
* padlock is a 'public key'
* 'secret key' can open the padlock

----

## We recommend

* keybase
* GPGTools
* Enigmail for Thunderbird
* lots of mail clients have GPG support

----

# Group activity!

Get your keybase account with the invitation code we've sent you and encrypt a message to somebody else in this workshop. Send it to their email address.

----

## Solution #2:

### Secure messenger

----

## What does it and how?

* encrypts message end-to-end per default
* does **explicitly** not store activity records (metadata)
* is open source
* optional: has self-destructing messages

----

## We recommend

Signal

---

# Researcher privacy

----

## Main risks

when researching on the internet:

* activity record (metadata) retention (by state/institution/ad networks)
    * by IP
    * by cookies
* revealing of personal details to website owners

----

## Solution #1:

### https

----

## What does it and how?

* browser checks whether website has a valid certificate ('ID card')
* encrypts traffic between browser and website

----

## We recommend

* check the address bar in your browser
* https://www.eff.org/https-everywhere

----

# Group activity!

visit https://browserleaks.com

----

## Solution #2:

### VPN 'tunnel'

----

## What does it and how?

* prevents eavesdropping, e.g. in an open WiFi
* BUT: does not verify certificates ('ID cards')
* hides your IP address (i.e. location, internet provider, other visited websites) from servers you communicate with
* can make you appear to be in another country and circumvent DNS or geo-blocking

----

## We recommend

* should claim not to store activity records
* should use OpenVPN
* should have servers in safe jurisdictions
* if it's too cheap you might pay otherwise

NordVPN and Private Internet Access have a long term high reputation

----

## Solution #2:

### Tor Browser

----

## What does it and how?

* provides secure, not easily identifiable browser that doesn't leave traces
* onion-network (encrypted tunnel through encrypted tunnel through encrypted tunnel ...)
* does not prevent you from disclosing your identity e.g. by logging into Facebook

----

## We recommend

Use for high risk research, not for everyday use.

----

# Group activity!

Install Tor Browser and visit https://browserleaks.com again.

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
    * Cryptomator
    * keybase
    * disk image encryption by your operating system

MAKE SURE YOU NEVER WILL LOOSE YOUR KEYS OR PASSPHRASES!!! Or all will be lost.

----

# Group activity!

Encrypt a file with keybase for you/for somebody else.

---

# How to choose a tool?

----

1. Open Source?
2. independent security audit/reputation?
3. will you actually use it?

---

Questions?

---

![](https://abs.twimg.com/icons/apple-touch-icon-192x192.png)

@brendam
@flxvctr
