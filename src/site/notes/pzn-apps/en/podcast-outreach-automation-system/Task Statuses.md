---
{"dg-publish":true,"permalink":"/pzn-apps/en/podcast-outreach-automation-system/task-statuses/"}
---

# Task Statuses
- **New**: just created, requires attention
- **Ready**: ready to be sent. 
	- if Task type is Outreach Email, and it's date is on or before Today, and its status is Ready, then an email is created and send via Make.com
- **Sending**: sending process is started, a new mail is created and sent to Make.com
- **Sent**: Make.com successfully sent the email
- **Received**: an incoming email is received and added to the base as a task
- **Replied**: a sent email was replied and there is now a task with the reply in this lead
- **Expired**: an email was not replied during the planned time and a follow-up task was created
- **Blocked**: another unreplied mail to the same recepient exists
- **Fail**: email could not be sent due to an error, error message is added to **Notes** field