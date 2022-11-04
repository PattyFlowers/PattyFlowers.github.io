---
layout: post
title:  "Seventh week at Makers Academy"
date:   2022-10-30
categories: Programming Learning Progress
tags: ["programming", "coding", "software development", "tech", "Makers Academy"]
---

<p><img src="/assets/images/antonin-carvalho-INL1xCkonxw-unsplash (1).jpg" alt="Yawning cat" width="300"></p>


## What was it like?

This week, we have continued to learn JavaScript, focusing on retrieving information from API or a server and storing it. It has been a very hard week, in which most students have noticed a sudden increase in difficulty, from easy exercises where you were given the solution in case you wanted to check if yours was correct or got stuck, to a “you have to do this thing that looks and functions like this, but are on your own, off you go”.

It has been a very difficult week, probably one of the worst ones. Most of us ended-up feeling various degrees of frustration at the end of the week, and I have learnt one of the most valuable lessons yet: I should be asking for help sooner. It is difficult, it hurts your ego, and it goes against that feeling of “it’s a challenge, I want to do it on my own and proof myself I can do it”, but it’s the only way that is reasonable and kind to yourself and others working with you. There is no point on spending several hours stuck on a problem and not making any progress, when there are coaches or peers happy to help.

So much frustration and hopelessness. I thought I was the only one really feeling it, until one of my peers sent a message saying how low they were after that week, and how little they thought they had understood, and saying sorry for whomever had to work with them the following week. As much as I don’t like to see other people having a hard time, it really helped to see that somebody else was going through the same, and the amount of people replying to their message made me realise it was quite a general thing.

I had been made aware of the fact that becoming a software developer in three weeks was going to be hard, but I don’t believe I had fully understood the implications of that statement. There is a lot to learn, and we won’t get proficient at everything we try in that time, unfortunately. It is more about learning how to learn and how to search for things, managing to get the tools we will need to get by. Like some of my IT friends say: “If we didn’t have access to the internet when we are working, we are unlikely to get very far with it”.

So, to whomever is going on a similar journey, don’t loose hope and persevere. It will be very hard, it will require a lot of effort, consistency, and threatens to the ego in the form of never-ending error messages, but it is possible to get to the other side, and whomever you are, I have faith in you and I am certain you have what it takes :).


<p><img src="/assets/images/pexels-josh-hild-2423959.jpg" alt="Woman with umbrella" width="400"></p>

# Code review

On Monday, I had my first code review. This is a resource that Makers offer and it’s probably **one of the most valuable ones so far**. 

It consists on a scheduled hour where the **reviewer role-plays as a client and gives you a problem to solve and answer any questions that, as a software developer you may have in order to create the product** they are looking for. They will then watch you code and watch the process you follow. At the end of the session, they give you some feedback on what you have done well and what you could improve, and a few days later they send you a full and very detailed report on this.

The the things they evaluate and include in the report are:

* **I use an agile process:** Understanding the requirements of the “client” and take notes of them, asking about edge cases (if a misspelled string or a wrong type of or empty input is given, for example. Write some examples of input-output in plain English before start writing any tests or code. This will help with the rest of the exercise and also if someone else was working on your code.

* **I can model anything:** Good planning on using classes and methods for the exercise, starting by writing pseudocode and adhere to naming conventions and best practices. Use a logical approach to the problem.

* **I can TDD anything:** Make sure of introducing tests for edge cases. Start with very basic and simple tests and have a good progression in complexity, try not to jump from very simple cases to complex ones as this will reflect on the quality of the code as well. My reviewer recommended the following resources about test triangulation to learn how to isolate the smaller problems from the larger ones through an incremental test progression:
  https://www.youtube.com/watch?v=E8gipX_C5fM&ab_channel=Codemanship

  https://www.tddfellow.com/blog/2016/08/31/getting-stuck-while-doing-tdd-part-3-triangulation-to-the-rescue/

* **I can program fluently:** Being comfortable with setting up the development environment and being familiar with the language syntax and constructs. 

* **I can refactor anything:** Follow the Red-Green-Refactor cycle. First, write a failing test, then, make the test pass through modifying your code, last, refactor both. Repeat. It is best to not wait until the end of the coding session to refactor our code, as this can lead to more difficult to change code.

* **I can debug anything:** Being familiar with common errors and being able to identify problems using the backtrace and the information gathered from failing tests. Being capable of gaining visibility to determine which areas of the code are not behaving as expected.

* **I write code that is easy to change:** Making regular commits on each Green-Refactor phases. Making sure to refactor often enough and try to keep code as simple as possible to pass our tests.
Name variables so that it is clear what they represent.

* I have a methodological approach to problem solving: Make sure to follow the RGR cycle (checklist provided by my reviewer):
-Write a failing test.
-Did you run the test?
-Did it fail?
-Did it fail because of an assertion?
-Did it fail because of the last assertion?
-Make all tests pass by doing the simplest thing that could possibly work.
-Consider the resulting code. Can it be improved through refactoring? If so, do it, but make sure that all tests still pass.
-Ask yourself the question, ‘what is my code currently assuming’ and think of the next simple test that will break that assumption and introduce a new failing test.
Repeat

* **I can justify the way I work:** They would like you to voice step by step what you are doing and why. This keeps the reviewer updated and it is good practice for future pairing or interviews.

# Pairing

Once more this week I found myself in the situation of being paired with some people that didn’t seem very keen to pair. I also paired with someone that was feeling very drained, and preferred to do things at their own pace, so we only paired for a couple of hours.
It was the last week of random pairing, and one of my best friends and I hadn’t paired yet, so we asked the coaches if they could put us together for the remaining couple of days. Both of us were also feeling quite tired, so it helped to pair with someone we already knew we’d work well with.

Because we were a bit more comfortable around each other than with some other people from the cohort, it also helped to **work on setting boundaries**, and because we work at a similar pace, we could take the time to put more emphasis on actually **understanding what we were doing and explaining it to each other to create a solid foundation.** Despite a very intense couple of days of working and pairing almost constantly through video-call, we also had a lot of fun, and I think it was one of my favourite things of the week.

# Workshops
This week we had two workshops, but I ended-up only going to the first one. We were all struggling with HTTP requests, so we asked for a workshop on that topic. 

The person running it was lovely, but I felt like it would have been more enjoyable and far more useful if they had had something prepared, at least an exercise to work on and a clear idea of how to move forward, rather than starting everything from scratch and trying to figure things out as they go. It was great to see the whole process with all the googling-up things and such, but after an hour and a half, we had barely touched the topic we needed the most.

# Retrospective

To be honest, I thought that after such a difficult and frustrating week, the retrospective was going to reflect that general feeling of hopelessness. But then something magical happened, people decided to **focus more on the positive** than the negative, and the grateful messages about pairing and people helping each other popped-up like mushrooms after a rainy day, and it helped lift the spirit. It had been hard and exhausting, sure, but it had also helped us realize that we are not alone, that we care for each other and are there to help, and that was a beautiful thing to witness.

<p><img src="/assets/images/retroboard.png" alt="Retrospective board" width="700"></p>

## What have I learnt?

**Using JavaScript and making requests to an API**. I have also been getting more comfortable with the syntax throughout this week, and learnt more about how to test this language.​

Most of us ended-up feeling various degrees of frustration at the end of the week, and I have learnt one of the most valuable lessons yet: I should be asking for help sooner. It is difficult, it hurts your ego, and it goes against that feeling of “it’s a challenge, I want to do it on my own and proof myself I can do it”, but it’s the only way that is reasonable and kind to yourself and others working with you. There is no point on spending several hours stuck on a problem and not making any progress, when there are coaches or peers happy to help.

I also learnt a lot from my code review in what I can do to improve my coding and what the best process to follow is. Looking forward to the next one!


<p><img src="/assets/images/pexels-dương-nhân-1510149.jpg" alt="Woman looking out the window" width="500"></p>
