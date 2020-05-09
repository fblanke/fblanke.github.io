---
layout: post
title: On the difficulty of programming
description: Why is it that we still have software bugs and expensive apps and systems when anyone can access and learn a programming language in a few hours online?
---

## *The challenge with programming is not technical, it's the discipline and the craftmanship*

Is programming hard? That depends, obviously. 

Some might argue that programming requires depth in mathematical knowledge, that you need to be able to work with multiple abstract models in your head and write in some arcane and mysterious language involving 1s and 0s.

On the other hand, almost anyone could write a Hello World or print their name 10 times in a loop with Python, create a Wordpress blog or setup a simple web server with node.js in no time.

Both of these statements are of course true, but I would still make the case that programming is hard. But not in the sense of logic and data manipulation, rather it is within the discipline to adhere to good standards and ensure longevity of your code.

Let’s take an example.

Picture a company, Corp Inc which need to further develop their software. They have a user story which states that: “As a newly registered user, I want to receive a message that welcomes me and if I’m either under 18 or over 65, it should let me know that I’m eligible for a discount”.

Seems easy enough, right? If we don’t have it already, we create a user model something like this:

```javascript
class User {
	first_name: String
	last_name: String
	email: String
	age: int
	eligable_for_discount?: boolean
}
```

We can pair this with a form on the web to let a user sign up. When they’re done and press send, we can take all the info and send them a message saying: 
```
“Welcome to Corp Inc <First name>!”
```
And if 18 < Age < 65 we will also add a line saying that the user is eligible for our discount.

Done! And it was easy right?

This was an easy story and an example can probably be implemented in it’s easiest form in under 1 hr by the majority of people. 

But the real difficulty is hidden behind the simple need that we want. For instance, what happens if a user with that name is already registered? Should someone who registers when they’re 17 get a message when they turn 18 to let them know they’re no longer discounted? What happens if a user pressed our “Create user” button twice before the page reloaded?

## Knowing how to use a hammer and a saw doesn't qualify you for being a builder

In Sweden, where I'm from, we have woodworking as a subject in school. You are taught to use basic tools and make simple things like butter knives or sauna scoops (is that even a word?).

I could use my skills and knowledge from woodworking class to build something simple but useful, say a table. I would take a couple of planks, use a saw to get them to the correct length, nail them together and then use a screwdriver and drill to attach to table legs. Ta da! Am I now a builder? I would say no.

A builder or carpenter can make more complex but very useful things, and that would require more knowledge. What type of wood to use, different techniques for screwing and using sockets, how to get a smooth edge without sacrificing durability, making sure a wall will hold up a roof of thousands of kilos etc.

### Discipline and craftmanship

A lazy programmer might create the happy path example I described above and just call it done. But a good programmer would of course also handle the corner cases, error handling, make sure tests are in place to verify a correct flow, add logging to get persisted history and might even ask the question to figure out what expected behaviour should be as a user ages.

To try and recap and summarize let me say this:

**Logic is easy (well somewhat..), software engineering is hard.**

An observant reader might notice that I threw in a new word into the mix, software engineering. 

To me, software engineering is the practice that makes something stable, flexible, scalable and efficient. I do not consider it to have anything to do with business logic. It is simply what is required to turn software into good software (Remember our example above?)

Okay so now you're thinking "thanks for that opinion.. But what now?".

Should a user story or requirement of some sort capture these details too so that a lazy programmer is more easily caught? No! Requirements are always hard, and according to me a big driver of why software projects become more expensive and take longer than expected, more on that some other time. Even if you tried to capture ALL of the possible outcomes and expected behaviour, error handling etc, it would not be worth the effort since there is still probably something that a lazy programmer might skip. 

Instead you should focus on building a good software engineering culture, where lazy programmers turn into good programmers who adhere to the discipline needed to create good software. Pair this with a product or requirement side which can produce requirements at the right level and lead the way and you will be building greatness every day.

Thanks for reading!

