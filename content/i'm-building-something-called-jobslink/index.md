---
title: "I’m building something called JobSlink"
description: "Before the what is, let me explain why I came up with this idea."
date: "2018-06-23T21:17:14.868Z"
categories: []
published: true
canonical_link: https://medium.com/@AlfieDarko/im-building-something-called-jobslink-a4c27c3bb5de
redirect_from:
  - /im-building-something-called-jobslink-a4c27c3bb5de
---

---

One time at [ClickCleanit LTD](http://www.clickcleanit.com) (my little side hustle), we had lost a customer & the potential of a fruitful long-term business partner because of a mixup with the details we had received & had given to contractors. Since it was over the phone, there was no solid record of what was actually said. **Important information like that shouldn’t be left to perception or memory**. It needs to be recorded.

**I love solving problems.** Its the big reason I got into programming. Life had just presented me with a problem & a potential opportunity. We really needed all job detail communications recorded digitally. It needs to be seamless, easily. Really really.

My aim was to create a system where I could enter jobs details online and send them via SMS to contractors. Contractors can then accept or decline them via text. They can also mark jobs as complete via SMS. _This leaves very little to interpretation as everything is set in_ **_stone_**_._

### **But there is email?**

Simply because alot of people we work with don’t use email as their primary means of communication, they like phone calls and text messages. Almost all our staff prefer phone calls rather than emails. Even though emails are instant, they don’t feel as immediate as a call or text message. People run out of data, some people dont even use the internet as much as we do. I still feel that SMS is the best format right now for reciving messages. When you get a text, you check it within a few seconds & that is true for more people that it is with emails.

![“Bank account full of $eed funding after I tell them that I’m disrupting some kind of verb”](./asset-1.jpeg)

After playing with the idea, I thought much about how it could be expanded in order to auto assign jobs to contractors based on their past stats and information. For example, it would be great if we could send job assignments based on who has the highest job acceptance rate, or who gets the job done the quickest. Even whoever is closest to the job! My idea has led me to attempt to develop as a side-project & perhaps maybe down the line, I could push it forward as some kind of product.

**Since I like shiny things**, this also gives me the opportunity to experiment and practice with new technologies!

![](./asset-2.jpeg)

On the backend, I will be implementing Node, Express, MongoDB & GraphQL.

### Why GraphQL?

I like shiny things. Also I really like the simplicity of it as a query language. After working with SQL queries and seeing how verbose it is to do certain things, GraphQL looked a beauty. I liked how expressive it was when trying to request information

On the other hand, this could easily be implemented with a REST API but that wouldn’t put me outside of my comfort zone. I want to jump in at the deep end with something. At Makers Academy, we were introduced to new tech every single week & old habits die hard. Learning about new things while brushing up on old things is a good thing.

On the front end, I will be using React since I want instant update views in the event of SMS job confirmations and completions. I want to explore using this framework too so it’s a good opportunity to experiment with this.

I will also be using Twilio to handle the SMS messages. That is something I got to use on the first weekend challenge at Makers Academy and it was something that I thought would be so useful later down the line if applied to other things.

---

Things may change, develop further or I may find that some things don’t work as well as I thought they would and that is OK. Documenting the process and sharing my findings via Medium gives me a chance to reflect, evaluate on my processes & most importantly, learn from the process!
