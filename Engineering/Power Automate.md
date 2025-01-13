---
title: Power Automate from Email to Onedrive
---

![A screenshot of a power automate flow!](./images/connector.png "power automate flow")

I often have the habit of writing my notes in outlook or in a random text box. Wherever I can find space or tiem.

There are many, many other ways of keeping notes and journals. but I wanted to keep them in a space of my own.

OneDrive!

The problem I had was that I wrote all my notes on my laptop, and have them synced to my personal one drive.

I don't always have my laptop on me, and sometimes an idea will happen where I'm out and about and I really need to save an idea so i'll either have to find a way to edit it in a third party editor like notion, or I'll have to write it out on paper or something else.

After a while I built up a collection of draft emails with loads of ideas and notes about all kinds of things. and this was starting to get messy and overwhelming.

so i decided to take action.

I knew that I could tackle the email problem either by writing a serverless function to connect to my email, or even deploy a vps and have some code running as a cron job.

But I wanted to try power automate since it's part of the Microsoft platform.

I laid out the following flow.

1. Upon new email to the outlook account, trigger the flow.

2. Perform data composition to extract the text the html formatted email

3. Write the file to my one drive using the subject as the file name.

There are some specifics about each of these steps such as the trigger only being actioned when the email subject contains specific text and is sent from one of my own email addresses. The one drive connector also requires an expression to extract the file name from the email.

Now I can happily send all those drafted notes to my outlook account and have them formatted nicely in my one drive as text.
