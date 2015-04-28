---
layout: page
title: About
permalink: /about/
---

Some information about this project!

### Information

[IFTTT](ifttt.com) is great. It supports many [channels](https://ifttt.com/channels) to create so called recipes, but may fall short if you are looking to implement more complex tasks. This can become complicated to impossible. However, they support a channel for github as well as rss feeds, which could make things interesting.

### Example
I might be interested in getting an iOS notification during the end of my work day to wrap up and leave the office. However, I may want this to be dependent on (a) the time I arrive in the morning and (b) the next best public transport options. 
Theoretically, I could simply display a notification at the same time (let's say 6pm) every night. Unfortunatly, I will completely ignore this, as I prefer to leave just on time to get my public transport connection. Alright, we could set the timer to 6:12pm, but this may not be the same every day and won't take irregularities into account. It also isn't very helpful if I can not leave, yet, and would like to get another reminder in 30 minutes.

I assume you get my point - there should be some smarter logic in the background figuring out when I should be reminded, so that I will actually act upon the notification.

This is usually not possible with [IFTTT](ifttt.com) as you can only have a single "trigger" event and not a very complex "resulting action". Alright, we need a script to do that for us, but we can't execute scripts within IFTTT, or can we? (No, we can not as far as I know)

### Scripted RSS
The initial idea therefore is to write an application or script on your computer that figures out what is supposed to be done when and simply push a commit onto your RSS feed, which can then trigger an iOS notification.

It would be great, if IFTTT would already provide such a "background-task" for your computer, but they don't.

### Limitations
Of course this is making the gui-based IFTTT approach to automated tasks obsolete and therefore this is not intended for non-technical people, but would you really use IFTTT if you couldn't?

### Contact me

[iftttrss.github.io](http://iftttrss.github.io)
