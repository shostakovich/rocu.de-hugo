---
title: A short primer on Pair Programming
date: 2013-05-26
emoji: ⌨️
---

When I started to pair-programm I had absolutely no idea what I was doing. I sat next to another programmer and we started. Occasionally it worked, but more often it was a frustrating experience.

Maybe you are new to pair programming and want to give it a try, or you have trouble getting started. Then this blog post is for you.

I show you how we pair at Gutefrage.net. Some of this advice is really obvious — but much of the other stuff we figured out the hard way through pairing over and over again.

![https://images.unsplash.com/photo-1530442788742-8a6beb2efb65?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb](https://images.unsplash.com/photo-1530442788742-8a6beb2efb65?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb)

### *Preparations for your first pairing session*

Probably your workspace is not suited for 2 people working on it for an extended amount of time. So, before you even begin: Be a good host: *Adjust your environment for pairing.*

### *Physical preparation of your workspace*

Move away the piles of paper, the dishes, and your backpack under the table. Clean your table. Don’t let the navigator feel like he is just a visitor.

Now move 2 chairs in front of the table. If you do not pair all the time, it is also ok to keep a few spare chairs scattered through the office.

### *Prepare your hardware*

Now take a good look at your screen(s). Can you see them from both perspectives? Is the contrast high enough?

Especially with notebook screens, it can happen that the person sitting next to you will have such a bad contrast that it might be hard for your pair to see what you are doing. If this is the case, get a monitor that both of you can watch.

Place a second mouse/keyboard combo on your desk. It’s nice for the navigator to point to code or be able to write a chunk of pseudocode, and it costs nearly nothing.

### *Prepare your computer*

Adjust your font size to 16px or 18px. I know this seems ridiculously big, but it will be much nicer for the navigator to look at it. (And also for you, of course)

Now close all your programs. E-Mail clients, IRC, Instant Messenger are of-limits during pairing in my opinion. You will have time for checking this stuff in between the pairing session.

Prepare an editor/IDE that both of you can use. Get an environment ready that works, check out the project, run the tests.

### *Talk to your partner*

You should know each other’s schedule. I find it frustrating if my pair has to leave in 15 minutes. Better to know in advance.

### *Grab Essential tools*

Now the navigator should grab a **notepad** and a **pencil**. Also prepare a **timer**.

A kitchen timer works fine, alternatively search for “[Pomodoro Timer](https://rocu.de/2013/05/26/%3Chttps://www.google.com/search?q=pomodoro+timer)” on Google.

## *Immediately before every session*

Grab a coffee, go to the restroom, and prepare yourself to focus for the next 25 minutes. Close open loops that might distract you during this time.

## *The first pairing session*

At the beginning of each session, the navigator sets the timer to 25 minutes.

Then talk about what you want to do on a high level. Both of you should have a good idea about the scope of the task ahead and what steps are involved.

If the task consists of multiple steps, the navigator should write down a list off these steps.

### *Write a test first*

Pick the best step to start with and write the first test. Try to get the test right, so you both understand what needs to be done.

TDD is especially effective with pairing, it communicates what you want to do, and it will focus both of you on the next step.

### *Driver*

Now the driver’s responsibility is to implement the code. Explain what you are doing along the way. Do not concentrate that much on the big picture, but try to get the task at hand done. Trust your navigator to keep the larger picture in sight.

Whenever there are alternatives ways to do it, and you are not sure — ask your navigator what to do.

Let the navigator guide you through the list of tasks. Ask him how to proceed if you are unsure.

### *Navigator*

Ensure that you work on the tasks on the list.

If you discover additional tasks — it often does make sense to postpone them and focus back on the problem at hand. It’s your responsibility that both of you don’t forget them — so write them down.

Keep engaged with the driver and try to understand what the driver does.

When you notice that the Driver get’s stuck, unstuck him. Even if you don’t know the answer to the problem at hand — ask him a question.

Point out typos or problems if the driver does not see them himself. Is the code understandable? Are the variable names ok? Is the class getting to bloated? Do an on-the-fly code review. Mention problems. But do not micromanage, of course. — Just like in a normal code review.

Pull the driver out of the implementation if you have the feeling that you should change the angle. Discuss it with him.

### *Talk, talk, talk!*

![https://images.unsplash.com/photo-1590650516494-0c8e4a4dd67e?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb](https://images.unsplash.com/photo-1590650516494-0c8e4a4dd67e?ixlib=rb-1.2.1&q=85&fm=jpg&crop=entropy&cs=srgb)

You should communicate all the time! In a good pairing session, it really feels like you are working on this in unison. As the driver you can focus on getting the tests passed and as the navigator you can keep the pair going in the right direction, ensuring an excellent quality.

Communicating right is maybe the hardest part for most programmers — just keep doing it. It’s a skill that you can acquire and if the pair is really attuned to each other after many sessions this will feel like second nature to you.

### *General behavior*

Concentrate on the task at hand for 25 minutes. Do not watch your emails, do not take breaks, try to stay engaged. It is expensive for 2 programmers to become distracted.

Work step by step from your list. After you have finished a step, take it off the list and start working on the next step.

Don’t argue too much. This is not an ego game — if both of your solutions are equivalent, just decide and keep going ;)

## *After the session*

The session ends after 25 minutes. Take a break of at least 5 minutes. This is the time to grab a coffee, to visit the restroom, check your mails and take a break.

Good pairing is intensive. You will need the break, especially if you want to work for a few hours in a pair.

After each pairing session, switch roles. We solve this with a WIP commit to the feature branch, then we change workstations.

After the break is over, start another pairing session if needed.

## *Conclusion*

Getting started with pairing is no easy feat. Don’t get discouraged. It is worth to learn it.

In a future blog post, I will describe the many problems that you might encounter during pairing and how to tackle them.

I hope after reading this little primer you get the idea how this could work and be sustainable. Since this are not best practices by any means, feel free to implement pairing your own way.

If you have experience pairing or tried this out: What are your thoughts about this? How do you pair?