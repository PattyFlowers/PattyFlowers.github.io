---
layout: post
title:  "Tenth week at Makers Academy"
date:   2022-11-18
categories: Programming Learning Progress
tags: ["programming", "coding", "software development", "tech", "Makers Academy"]
---

<p><img src="/assets/images/adi-goldstein-EUsVwEOsblE-unsplash.jpg" alt="Circuits with light by Adi Goldstain" width="500"></p>


## What was it like?

In week's nine retro, we covered what high quality code looked like:

# Easily Changeable
    • As simple as possible
    • Clear notation, comments
    • Principle of least astonishment, really complicated functions should be broken up.
    • Commits documenting our process
    • Keep classes loosely coupled

# Readable
    • Avoiding repeating yourself
    • No magic values
    • WELL NAMED VARIABLES AND FUNCTIONS
    • Following style conventions inc. naming.
    • Use a linter
    • Use regex sparingly, label everything
    • Avoid one liners

# Reliable
    • Good tests.
        ◦ Granular
        ◦ Testing behaviour, not state
        ◦ Isolated
        ◦ High coverage
    • SRP - Single Responsibility Principle
    • Separation of Concerns
    • Create wrapper classes
    • SOLID Principles


I think this week was meant as a resting period in between group projects as well as a way of focusing on improving the quality of our code and testing.

After a couple of busy weeks with strict schedules and in which we pushed ourselves quite a lot, we were presented with the week of **“solo projects”**, which was completely self-directed. This was intended as a practice for future tech-tests (an exercise companies make you do to see your coding processes as part of an interview).

We were highly encouraged to do one of the proposed tech-tests, called “bank tech-test”, which was the main one we would get feedback for. After that, we could either continue doing some other of the proposed exercises or continue studying something on our own.

<p><img src="/assets/images/daniel-mingook-kim-H7sHkM9eilw-unsplash.jpg" alt="Hand with a sparrow by Daniel Mingook Kim" width="300"></p>

One of the first things the coach gave us was a **list of “not-to-do”** things or anti-patterns for our repositories:

If you really want your tech-test to be likely to fail:
    • Don't have **instructions on how to install your code**
    • Don't have **instructions on how to run your code**
    • Don't have **instructions on how to run your tests**
    • Include **tests that fail** when you run them
    • Have code that doesn't **satisfy the requirements**. Example: there's a set of test input given with expected output and your code gives a different output for that input
    • Put all your code in a **single class** even though that gives it multiple responsibilities
    • **Git commits** don't show a clear process

The **bank tech-test** consisted on creating a small application from which the user could make deposits and withdrawals, as well as printing a bank statement that would show dates, operations and balance. It ended-up being quite time consuming due to TDD, but it was a great exercise to try do things properly (have a high test coverage, adhering to the single responsibility principle, refactoring, making easily readable code…). You can find this repo [here](https://github.com/PatriciaGN/bank-tech-test). I received very good feedback in most parts but one: **the README**.

I had a clear commit history, my tests showed a good progression and coverage, my code was simple and readable and I had divided the exercise in several classes that only did one thing, but my README file was an absolute disaster. The instructions to install the code didn’t work properly and the formatting was not good. It was one of those things I did at the end of the exercises without putting much effort into it, because until then, I thought my code would talk for itself. But then I came to the realisation that **many people that look at our repos will not make it past the READMEs**, they are the first thing they will encounter, and if it doesn’t look good and facilitates installing your program, there’s no point wasting their time looking at our code.

<p><img src="/assets/images/michael-dziedzic-fTdnRCpRTdE-unsplash.jpg" alt="Torn book pages by Michael Dziedzic" width="400"></p>


I was very grateful for the slightly harsh but great and thorough feedback that the coaches gave me about this test, and I will make sure from now on my READMEs are something I spend an adequate amount of time and energy on.

After that tech-test, I decided to do another one called **Gilded Rose** ([repo (here](https://github.com/PatriciaGN/gilded-rose-tech-test)), which was very good fun. It was about a shop, based on World of Warcraft, where they had objects that “aged” differently. Normal objects would decrease in quality, whilst some, like “Aged Brie”, increased quality with time. The original program was a huge mass of spaghetti code, way too many lines of nested if-else statements trying to mimic what **legacy code** would look like, and we needed to turn it into something easily changed and maintained. 

I started by **creating passing tests for all of the cases** they gave us, and then started **refactoring**, until each special object was in its own class. Then, it was very easy to add a new object with special characteristics. It was a fantastic and very fun exercise, from which I learnt a lot.

## Retrospective

The retrospective this week was mainly themed around how people had felt the shock to the system from what looked like structured days to working entirely on their own, without any particular schedule or deadlines. It was good to see how it had given everyone some breathing room.

<p><img src="/assets/images/1retro-week-ten.png" alt="Retrospective board" width="600"></p>


## Job-hunting process

During this week, we also had our first session about job-hunting, as well as a talk from a Makers alumni that had found his dream-job some months prior. We were only a few weeks from finishing, and it was difficult not to be thinking about what things would be like after makers.

Some of the useful tips from the talk:
-Have a job application spreadsheet with things like: Company, date, received response?, feedback received?
-Apply to A LOT of jobs. It’s really easy to feel like a couple of jobs a day will do, but this guy applied to over 180 jobs before getting a position.
-Tailor your cover letter to the job you are applying for. It is difficult at the beginning, it requires a lot of reading and investigating each company’s products and culture, but it becomes second nature soon enough and increases your chances of success.
-Contact old Makers alumni or even other more experienced software devs to ask them about their journey. They are generally happy to help and they can give you some good tips.
-Regarding tech interviews: 
  * You can ask for help on tech tests if needed! It’s good to show you are able to ask for help when you need it.
  * When they ask about something you don’t know, it’s always better to be honest about it.
   * Negotiate all of your offers, even when they seem reasonable.
* [Video on negotiation](https://www.youtube.com/watch?)


<p><img src="/assets/images/eric-prouzet-B3UFXwcVbc4-unsplash.jpg" alt="Door with We are hiring sign by Eric Prouzet" width="300"></p>


## What did I learn?

I would say the most important things I have learnt this week were:
* That it is worth taking the time to follow the Red-Green-Refactor TDD process both when creating your own code or working with someone elses
* That READMEs are an extremely important part of each project.
  

# Resources I used this week:

* [Refactoring and design techniques for TDD](https://www.youtube.com/watch?v=QbNhpPQkCBs)
* [Testing with Jest](https://www.youtube.com/watch?v=NHMIn723hQY)
* [Code with Ania](https://www.youtube.com/c/AniaKub%C3%B3w)

<p><img src="/assets/images/luis-villasmil-mlVbMbxfWI4-unsplash.jpg" alt="Man covered in post-its by Luis Villasmil" width="500"></p>
