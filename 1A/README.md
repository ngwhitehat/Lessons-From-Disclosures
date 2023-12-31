# 1A - FLAWS EXPOSING USERS' DATA FIXED

It was in the wake of the Whitehat.NG Campaign, we were building up the idea behind this movement and many things have started jumping to our heads on where to start. We reached out to people in need to know if they have received any emails of recent (specifically in the last five months), that seem to be unusual or may contain out-of-place information. A very large number of emails started trooping in and our team started conducting their analysis on them by drawing the T’s and dot the I’s. In the process, we found an interesting email from 1A which got forwarded by tens of people from our research dataset.

Analyzing the email, we found out that 1A reached out to many other people (Nigerians that registered) during the month of October and November 2019 in an email containing reference numbers and passwords in plaintext to accounts they created on 1A’s registration portal. To be sure that this is not a simple out-of-chance technical error on the email sent by 1A, we have to reach out to as many other people that registered with 1A during the period to be sure they received a similar email containing their password in plaintext hereby confirming our initial hypothesis.

![](https://raw.githubusercontent.com/ngwhitehat/Lessons-From-Disclosures/main/res/1A-now.png)

This initial hypothesis confirms that 1A stores registered users’ login information in plaintext on their database which is not a best practice as such information is meant to be stored in a distorted form for reasons that such database can get stolen or staff of 1A can decide to go rogue with data stores in such databases. If any of the stated reasons took place, the information in it becomes so useless as the distorted value will never serve the malicious actor’s purpose in the end or it may make things more difficult for them.

In moving forward on our research, our team took their time to passively gather and analyze other possible information we can get on the registration portal of 1A to see if there could be chances of the presence of other vulnerabilities which could be exposing users’ data that may be exploited by malicious actors.

We don’t want to imagine those possibilities malicious actors will have if they get their hands on the users’ email containing their reference number and password in plaintext, these flaws combined with other vulnerabilities that may be out there can lead to higher impact. So, we had to dig further to see if those holes are out there ourselves.

We found out that there was a link on 1A’s portal that gives unrestricted access to all sensitive documents that have been uploaded by users in the course of their registration. Wow, this is damning and confirms our second hypothesis of whether there are other loopholes that may have registered users’ sensitive information exposed to malicious actors.

Our second hypothesis confirms that secure code review didn’t take place before 1A’s application portal got pushed to production for the collection of data from Nigerians. Secure code review during and after the development of such an application would have helped identify such a link and it would have been patched before production.

At this point, the need to notify 1A of our findings becomes top priority for our team. We documented our findings including technical recommendations with a letter and sent it to 1A for them to review all affected areas. It took them a couple of days to fix all issues and get back to our team. We are glad we did help them turn this information into actionable intelligence. Share it with others so they can learn from it.

On the part of 1A, they have succeeded in collecting data from Nigerians but they have failed in ensuring it is protection as stated by the NDPA. Login credentials (passwords to be precise) of thousands of affected users that registered with 1A were sent back to the users in plaintext. With the help of the Whitehat.NG Team, we have helped change the story of 1A.

