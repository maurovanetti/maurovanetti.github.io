---
layout: post
title: There will always be a Turkish bug
tags: geek en
original: baco-turco
---
Programming can seem like very dry work, and in part it is. Yet, every now and then it gives occasion to do a bit of philosophy.\
I'm telling a story about my previous workplace, hoping that revealing these important industrial secrets won't push them to take me to court...

One of the things you learn right away when programming is that it's not possible to make the perfect program, one that works correctly in all possible conditions. There's always something we hadn't thought of, the only perfect program is a program that gets continuously reprogrammed: software either evolves or dies. In the best case it must evolve to keep up with changes in the context in which it operates (including changes in user requirements), in the worst case it's simply a matter of realizing subtle errors (*bugs*) made by developers, errors that manifest their harmfulness only with the concrete use of the application.

One day, in the large multinational where I worked before, someone notices that a part of the application that dozens and dozens of people had been working on for years, and which had now reached its seventh or eighth version, *didn't work in **Turkey***. I don't mean it worked badly, it just wouldn't start.

The person who notices this sends an alarmed message to the internal mailing list. Someone who thought he knew better replies: *"Come on, that's impossible, check better, you must have done something wrong"*. Half an hour later, the same person writes: *"I tried changing the computer configuration as if I were in Turkey. It's true, it doesn't start!"* But what the heck...?!

What's special about Turkey?

An hour passes, another email: *"We discovered that during the startup phase a trivial check on string comparison fails, it seems that in Turkey **toLowerCase()** doesn't work well"*. The *toLowerCase()* method, in Java, as its [documentation](http://java.sun.com/j2se/1.3/docs/api/java/lang/String.html#toLowerCase()) explains, converts text to its lowercase version. Why shouldn't it work well in Turkey? Especially since Turkey uses the Latin alphabet, ever since the modernizing and pro-Western reforms of Mustafa Kemal Atatürk.

**Eureka!** Even though I didn't count for much in that company, I couldn't resist the temptation to send an email explaining the mystery. Turkey definitely has something special: it's the only country in the world, as far as I know, where the lowercase version of the letter *I* is not the letter *i*. In the Turkish alphabet there are indeed two very similar letters: one is the *I*, without a dot, which becomes *ı* in lowercase, the other is the *İ*, with a dot, which becomes *i* in lowercase.

At startup, that program applied the *toLowerCase* method to a sentence containing an *I*, and compared it with a certain constant string, which contained an *i*. The comparison failed in Turkey, because in Java that method is *localized*, that is, it performs the lowercase conversion in a way that depends on the language and other "regional settings" of the system on which it's executed.

You have to be careful to dot your *i*'s, because the Turkish bug is always lurking.