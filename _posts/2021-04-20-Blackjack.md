---
title: "Blackjack Simulator"
excerpt: "I wrote a Python program that will simulate a number of games of Blackjack."
categories:
tags:
  - Python
  - Learning
---

##### I wrote a Python program that will simulate a number of Blackjack games. It allows you to change variables like, number of players, number of decks, player hit strategies, and player split strategies. The results of each hand are written to a Pandas DataFrame and pickled where it's then read into a Jupyter Notebook and analyzed. It's still a work in progress, but I'm at a place where I can summarize what I have so far.

##### It's ugly and inefficient, but it's mine and it works (as far as I can tell). This is the first thing I've written that I'd classify as a *program*. Everything I've done prior to this has been a one-off, throw-away script.

Keep reading, or go straight to the code [here](https://github.com/evancanady/Blackjack).

***

I overheard a converstaion between friends about a casino Blackjack game one of them was playing. He was upset the guy to his left hit on 17 and **took** what should have been his card.

The basic strategy of Blackjack is to get as close to 21 as you can without going over - going "bust", as they say. Face cards are worth 10. Aces are worth 1 *or* 11 depending on what's better for the player. All other cards are worth their stated (or pip) value. The players are trying to beat the dealer, who is also trying to get 21 without going over. Read more about the rules [here](https://bicyclecards.com/how-to-play/blackjack/). Get a higher total than the dealer without going over, you get paid. Dealer goes bust and you don't, you get paid.

As soon as I heard my friend's complaint about the stolen card my bullshit detector perked. It may have been a poor decision by the other player, but how could a randomly drawn card from the deck *definitely* be bad for him. Isn't it just as likely that it helps him? What if my friend had 15, was planning to hit, and the other guy drew a 10. That bad decision by the other player potentially prevented my friend from going bust. I'd guess the only time he would have seen it as a bad thing is if the other player drew a 6 which would have put my friend at 21. [Hindsight bias](https://en.wikipedia.org/wiki/Hindsight_bias) anyone? This all assumes he is not counting cards and adjusting probabilities in his head on the fly.

It was one of those 5 minute conversations that came and went and that was it. But, it got me thinking. How could prove his thinking was wrong, or at least flawed? As mentioned in a [previous post](https://evancanady.com/Learning-Python/), learning python and data analysis has been on my to-do list for years. I've slowly made progress buying a book here, taking an online course there, but nothing to write home about. Maybe I could use this as a real-world project to push myself up the learning curve. I could simulate a large number of Blackjack games while varying the strategies of certain players. Then, do a little basic analysis on the results and see how players are the table are affected. Easy!

Up to this point the bulk of my time has been spent writing the code to simulate the Blackjack game. A few weeks on-and-off. I started simply. Write a function to shuffle a deck and store it as an object. A function to deal from that deck. A function to total the hands. And so on.

At this point the user can set and modify Hit Strategies (at what point does a player stop hitting based on his hand and the dealer's up card) and Split Strategies (what hands should be split based on the player's pair and the dealer's up-card).

I'm beginning to wrap my head around Object-Oriented Programming. I've never needed Classes or even that many functions in the little scripts I've written in the past. I was writing code to do one thing and then I threw it away. Unsurprisingly, Google has been a huge help. But, how do you find and answer to a question you don't know how to ask?

This experience has support my thoguht that there are (at least) two distinct phases in learning something new. In phase 1 you don't-know-what-you-don't-know. So the questions you ask aren't that good and the feedback you get may confuse you even more. Then, at some point you have built enough foundational knowledge that you begin to see patterns emerge from the chaos. At this point, phase 2, you can articulate your questions and get better feedback. This is why learning is not linnear. Once you hit phase 2 learning accelerates and compounds more quickly.

I'll post again once I get the model finished and I start to make sense of the results.

