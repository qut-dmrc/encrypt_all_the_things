---
title: Encrypt all the things!!!
theme: css/theme/simple.css
---

![](http://blog.serverfault.com/files/2016/02/encrypt-all-the-things1.png)

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

```
From: Finn Coburn <finn.coburn@thepolice.com> To:
data-analysts@thepolice.com Date: 2016-12-10 10:58 Subject:
Fixing a leak at Minecorp

Good morning analysts,

Apologies for the email on the weekend. I am just off the
phone with the chief and I need you to work on something
asap.

It seems there is a whistleblower at Minecorp leaking to a
journalist at MineWatch. Here is the article that just came
out yesterday evening:

Anna Dupont: Whistleblower Reveals that Minecorp’s WA
Fracking Operation Uses Toxic Chemicals

May I remind you that the mines in Australia are all
critical infrastructure, and those leaked docs cannot get
into the wrong hands on the black market. Therefore, we need
to identify the person of interest to put him/her under
arrest.

So I need you to dig this guy up for me. As some of you are
new hires here, let me reiterate again what is expected from
you to do:

#1. Open up Kibana. On the left hand side bar, find the
#dropdown menu, and select the Google search query log
#(logstash-google_query_log-*). This brings up Google's
#records of what people have searched for. The article from
#above should come handy to find the right person. Remember
#you can click on fields (e.g. user_id) from the list. Don't
#forget to submit your results as you go.

#2. To get the email address of the whistleblower, switch to
#the email metadata logs (yay, we plugged smalllake.com.au
#in recently!). You might need to cross-check this dataset
#with the results from the previous step, and you might need
#to use quote marks when searching.

#3. You will need to dig into the phone subscriber data to
#get the name and full address. Don't forget to expand the
#time range to 5 years in Kibana.

#4. What is the last known location of the whistleblower? We
#may need to ring a judge in a different state for the
#warrant. Also, we could pull a couple of fresh photos of
#the target from the CCTV cams nearby. Try to get this from
#the mobile call logs.

#5. How many times did the journalist and this whistleblower
#talk to each other over the phone?

#6. Is there any other whistleblower who might be also
#leaking to MineWatch? Use our graph tool to do a link
#analysis on the telephone call logs. If you forgot how to
#do it, have a look at the Link Analysis section of the
#cheat sheet as a reminder.

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

# Example password reuse

getting hacked by angry gamergaters on one account, loose all others too

----

# Example IP address/VPN

researching in extremist bulletin boards/social networks
getting harrased in your neighbourhood afterwards

----



---

# Test
