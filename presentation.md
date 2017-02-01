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

# worst case scenario revealing IP address/VPN

researching in extremist bulletin boards/social networks
getting harrased in your neighbourhood afterwards

----

# worst case scenario for unencrypted communication

Iranian protester communicates via iMessage but message gets sent via SMS service

----

# worst case scenario for unencrypted devices

interview with journalist in Turkey with 'off-the-record' content on unencrypted Android phone gets confiscated at the airport before leaving the country.

----

# worst case scenario weak password reuse

getting Twitter hacked by angry gamergaters, and suddenly your devices are wiped

Note:
* even if something similar might have happened, all examples are made up
* 15 minutes in!

---

# Group activity!

----

Visit https://haveibeenpwned.com/ and look up your most used email address.

----

# Why are you here?

discuss in groups (5 minutes)

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

----

## What does it and how?

----

## We recommend

----

# Group activity!

Install a password manager and change one of your passwords

----

## Solution #2:

### Use 2-factor-authentication

----

## What does it and how?

----

## We recommend

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

### https

----

## What does it and how?

----

## We recommend

----

## Solution #2:

### PGP encryption

----

## What does it and how?

----

## We recommend

----

# Group activity!

Get your keybase account with the invitation code we've sent you and encrypt a message to somebody else in this workshop. Send it to their email address.

----

## Solution #3:

### Secure messenger

----

## What does it and how?

----

## We recommend

----

## Solution #4:

### VPN 'tunnel'

----

## What does it and how?

----

## We recommend

---

# Researcher privacy

----

## Main risks

when researching on the internet:

* metadata retention (by state/institution/ad networks)
    * by IP
    * by cookies
* revealing of personal details to website owners

----

## Solution #1:

### VPN + dedicated browser

----

## What does it and how?

----

## We recommend

----

## Solution #2:

### Tor Browser

----

## What does it and how?

----

## We recommend

----

# Group activity!

Install Tor Browser and visit something dodgy, e.g. Breitbart News.

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

## What does it and how?

----

## We recommend

----

# Group activity!

Install Cryptomator and copy a file to an encrypted vault. Don't forget to save your password in your password manager!

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
