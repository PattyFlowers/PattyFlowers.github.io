---
layout: post
title:  "Ninth week at Makers Academy"
date:   2022-11-12
categories: Programming Learning Progress
tags: ["programming", "coding", "software development", "tech", "Makers Academy"]
---

<p><img src="/assets/images/64e21dec-70d0-489b-be5a-4d9b8ed3c5a8.jpeg" alt="Owlpaca by an image generator" width="500"></p>


## What was it like?

During this week, we continued with our **group projects**. I had done what felt like a good amount of progress during the weekend, by adding **security to the front and back-end** as well as **messages responsive to user input** on the form fields. I enjoyed a lot working on it and was really proud of this as I was relatively certain no other groups would have this feature (as it was not one of the suggested or required by the coaches).

On Monday, we spent most of our day trying to **share what we had learnt** so far. It was very difficult to get everyone on the same page when we were all working on very different things, and an explanation of what had been done didn't necessarily mean that the rest of the people would understand it as well as the ones who had tackled the problem. That was something we had to live with if we wanted to continue. And it was hard, as we all wanted to get really good at everything.

We spent the rest of that day **deciding which features we were going to work on** for the first few days and on our pairs. I decided I wanted to try implement **“likes” and “dislikes”** (which in our case we decided to call “agrees” and “disagrees” to match the theme of the page), and someone else joined me. It didn’t take us too long to realise two things: 1. Implementing that feature was not as simple as it looked and 2. We knew what we had to do, but didn’t really have much of a clue of how to do it.

The idea was to **add the “agrees” and “disagrees” to our posts schema, which would default to zero, display these values along with each of the posts and then add buttons the user could press to modify those values.**. We had examples for creating new elements from scratch on MongoDB, but the last time we tried to modify something on a database, we were using Postgresql.

It took almost three days, a lot of tinkering, calls with the coach and help from my partner to finally solve the mystery of how to do it. Turns out, even though all the examples of queries we had in the pre-made part of the program were in lowercase, **PATCH needed to be in uppercase**, and that was breaking everything. Then, I realised **I didn’t understand asynchronicity as well as I thought**, and some of my functions weren’t awaiting a response from the database before continuing with other things.

It was a great learning experience, and although I had several moments of utter frustration, I enjoyed learning how to approach these problems and **ask for help as soon as I felt I was properly blocked rather than waiting** days and days in the hope that I would find my way through.

I spent most of Thursday playing around with CSS. One of my project-peers had come up with a retro design and had had the fantastic idea of putting my responsive messages into a speech bubble next to a Jhonny Bravo (a.k.a. Kyle) pixel image that jumped when you hovered over it. It looked bad in a great way, and you could really feel this is how social media would have looked if they were created in the 80s. We implemented a similar appearance on the rest of the site and got most of it to function relatively well.

We had our **demo** scheduled for Friday afternoon and our Friday morning became way busier than I would have liked. We finished giving the site the last touches and prepared our presentation after spending over an hour just adding funny posts, as we wanted people to have as much fun seeing it as we had had making it. We created users for each of us (and Kyle) and created posts voicing some of our frustrations over the last couple of weeks. It was great fun and we laughed a lot.

Then, we recorded the demo-video of the application itself, which was part of our presentation:

<video controls width="500">
    <source src="/assets/images/grumblebook_demo.mp4"
            type="video/mp4">
</video>

We also explained our motivations for this project as well as how we had worked as a group. I was very proud of what we had achieved and couldn’t believe how much fun I had and how much I had learnt thanks to it. The amount of sneaky grins or outright laughters during the demo let us know that we had achieved our main goal: have fun and make others have fun. I was also incredibly proud of the technical part of it, and I wished I could work in this same team once again in the future.

# Retrospective

I was kind of surprised to see how many people hadn’t enjoyed those two weeks as much as we did. Feelings of overwhelm, annoyance at the coaches for throwing in new technologies when some people could barely manage with JS and so on. There were a couple of groups were none but one person wanted to present their projects, and it ended-up all being up to that one person to do so. I realised how very lucky I had been to be working with such a wonderful bunch of people.

Someone opened the **debate on test-driving when you faced a new technology** and weren’t quite sure yet how it worked. Some people thought it was better to leave TDD on the side and try to build something that works first in order to learn how to best test it. Other people said that, without the tests, they would have had a much more difficult time understanding the code itself.

<p><img src="/assets/images/1_h0cg0aiV0xVCB5giRJdesg.png" alt="Meme saying: You can't have failing tests if you don't have any tests" width="400"></p>

Our retrospective board for the week:

<p><img src="/assets/images/retroweeknine.png" alt="Retrospective board" width="600"></p>


## What did I learn?

These last two weeks have been incredibly exhausting, due to being presented with a completely new stack and some pre-built features we didn’t quite understand. But with a bit of **persistence**, **a lot of diagramming** and **good team-work practices**, we were on the move soon enough, and very quickly implemented a bunch of new features.

I feel like I now have a **much better understanding of JS** and have also **discovered a love for React and its endless possibilities**, making fluid software that is easy and fun to use.

I also got more comfortable with **dividing the code into different pieces that had only one responsibility**. I remember at the beginning, when I insisted on trying to fit everything on one single method or one single class, that was then a nightmare to change. With a bigger project in my hands, I have seen much clearly the benefits of using the SOLID principles to work quality code that is **easily readable and changeable**.

What I felt like I **didn’t do so well** this time was **writing tests**. I felt getting used to test-driving React with Cypress extremely challenging and so did the rest of the people in my cohort. Once I realised how it worked, I was a bit more comfortable implementing some tests, but it is still something I need to put a lot more time an work on.

Only three more weeks to go!

P.S. One of the on-going memes for our cohort was when someone posted a "Pub?" message on Slack, and somehow it got around 400 likes, so we decided to honour it on out app:

<p><img src="/assets/images/image.png" alt="Sample of one of our posts saying 'pub?'" width="300"></p>

# Resources I used this week:

* Using Flexboxes on CSS: https://flexbox.malven.co/
* Some retro CSS templates: https://codeburst.io/10-amazing-and-retro-css-kits-24612169f550
* Double rendering and strict mode: https://reactjs.org/docs/strict-mode.html#ensuring-reusable-state
* React:  https://reactjs.org/docs/forms.html
* Timestamp: https://steveridout.com/mongo-object-time/
* Tokens (around 7 minutes in): https://www.youtube.com/watch?v=meTABGgrO2c
* What is React: https://www.youtube.com/watch?v=1wZoGFF_oi4&t=422s
* React in 30 mins: https://www.youtube.com/watch?v=hQAHSlTtcmY&t=1295s
* Deconstructing: https://www.youtube.com/watch?v=NIq3qLaHCIs&t=0s
* useState: https://www.youtube.com/watch?v=O6P86uwfdR0&t=154s
* Props vs State: https://www.youtube.com/watch?v=IYvD9oBCuJI
* useEffect: https://www.youtube.com/watch?v=0ZJgIjIuY7U
* Learn to use MongoDB with Codeacademy: https://www.codecademy.com/courses/learn-mongodb/informationals/welcome-to-learn-mongo-db
* Junior vs Senior React project structure: https://youtu.be/UUga4-z7b6s
* Firebase (image hosting + other services): https://www.youtube.com/watch?v=YOAeBSCkArA&t=474s
* Express in 35 minutes: https://youtu.be/SccSCuHhOw0
* MongoDB crash course: https://youtu.be/ofme2o29ngU
* MongoDB cheatsheet: https://www.mongodb.com/developer/products/mongodb/cheat-sheet/