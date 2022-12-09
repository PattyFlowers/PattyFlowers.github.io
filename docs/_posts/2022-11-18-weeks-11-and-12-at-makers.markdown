---
layout: post
title:  "Weeks eleven and twelve at Makers - The final project"
date:   2022-12-05
categories: Programming Learning Progress
tags: ["programming", "coding", "software development", "tech", "Makers Academy"]
---

Welcome to the culmination of the last four months of the Makers Academy bootcamp. It feels like ages and at the same time, I don’t know where that time went.

The objective of our last two weeks was to create an application from scratch, using our own idea and whatever tech stack we wanted. 

The previous week we had a short session in which we had to brain-storm and write at least two ideas each on a board. Afterwards, our coach divided them into topics (tech for good, social, location-based…) and we had to fill in a form with our preferences.

![Ideation board for our cohort](/assets/images/september22ideation.png "Ideation board for our cohort")

I knew what I wanted: to **work with our Grumblebook team again.** I wasn’t too concerned about the tech we used, but I knew I would like to do a project that **helped consolidate all of concepts** we had learned during the course (a full-stack application). I was also quite keen on do something within the **tech-for-good** topic, as I wanted to do something that motivated me and that I felt passionate about.

So I just wrote all that in the form, even though I wasn’t too sure they would straight away put us with the people we wanted. On Sunday, I went to London, as I wanted to spend those final two weeks working in the office with all those wonderful people from my cohort, and on Monday we were told our groups. To my surprise, **I had the group, the tech and the topic I wanted, and I couldn’t be happier!**

This time, we were team Undefined, and according to our team charter, we valued:
* Happyness
* Honesty
* Compassion
* Learning
* FUN
* Understanding
* Achievement
* Celebrate each other's wins
* Health and sleep
* Breaks
* Drinking

![App names brain-storming session board](/assets/images/brainstormingapp.png "App names brain-storming session board")

That first day was all **brain-storming ideas, discussing them and trying to choose one**. One of my colleagues suggested an app that would let you know every time your MP voted, and you would easily be able to see what each of their votes were. To be honest, my first thought was “I don’t really want to do anything related to politics, because I don’t like politics”. But the more I thought about it, the more I realised that was the reason that app should exist. People don’t like politics because they are not accessible, they live in their own bubble and all the information we get is through the media, which isn’t necessarily as objective as it should. **It was an original and innovative idea, and we didn’t think it had been done before.**

![Initial design options for our logo and application layout](/assets/images/votewatchdesign.png "Initial design options for our logo and application layout")
<!-- <p><img src="/assets/images/element5-digital-T9CXBZLUvic-unsplash.jpg" alt="Finish line by Ajoshua Hoehne" width="500"></p> -->

Once our idea was defined, we spent our second day **diagramming and deciding on what our MVP (minimum viable product) looked like, as well as writing tickets**. We wanted an app that could get a list of votes from a particular MP when given their name, and we wanted to build **phone-first**. To do that, we needed to get information from three different APIs from the government and display the votes in our main page. It sounded easy, but it ended up taking a couple of days to figure out how to use **React Native** (which is similar to React, but not quite the same) and how to chain our fetches to the APIs in an asynchronous way so that we could get information from one and feed it to the other.

![Our trello board with the different tickets](/assets/images/votewatchtrello.png "Our trello board with the different tickets")

By the end of that week, we had our **MVP** up and running and some people were already working on new features, like push notifications (which ended up being the most complicated feature to implement and took pretty much two full weeks of work).

<p><img src="/assets/images/MVP.png" alt="How our MVP looked on a phone" width="200"></p>

On Wednesday, we were treated to some **dog cuddles** by our Joy Chief Officer Forest, the Cocker Spaniel, which made our day ten times better.

<p><img src="/assets/images/forest.jpg" alt="Picture of Forest, the Cocker Spaniel" width="300"></p>

We also discovered that, although React Native had the advantage of allowing us to create an application for **IOS, Android and web at the same time**, that didn’t mean that all the code we wrote was going to work for the three of them. This caused some **extremely difficult bugs** to fix after the main merges, as some of us were only able to test their features on web whilst others had only an IOS or Android phone. We ended-up having to discard several features due to them causing the app to crash in a different platform. **FUN**.

<!-- ![Car coming out of a wall by Conor Samuel in Unsplash](/assets/images/conor-samuel-K5BFXOsFp7g-unsplash.jpg "Car coming out of a wall by Conor Samuel in Unsplash") -->

On our last Thursday, we were planning to go out for lunch, but decided to order some pizza to save time. Unfortunately, one of the members of our team had a severe nut allergy, and nobody thought that cheese in vegan pizza could turn out to be cashew cheese. So the poor thing had to be taken to hospital. So much for trying to save time by not going out for lunch. :poop:

Some of us had to stay in the office until 11-10p.m. that day trying to get everything working, with the added problem that our application was only working correctly on IOS, so only one of us could properly test it. I stayed for moral support, although felt quite bad for not being able to help more.

![Our tech stack](/assets/images/techstack.png "Our teck stack")

## Demo day
In the blink of an eye, the final day of our course had arrived. Time was up, and we needed to wrap-up and present our projects to our cohort, other cohorts, family, friends and potential future students.

It was a very intense day, that started with the presentations to our own cohort, which served as a bit of a rehearsal. It was amazing to see what other teams had achieved in such a short period of time. We had done it, we were developers!

After that, we continued to present our application through a video-call, to anyone from Makers that wanted to have a look. This meant doing our presentation on a loop 3 or 4 times, and the more we did it, the better it got.

![Man presenting to a group of people by Matthew Osborn in Unsplash](/assets/images/matthew-osborn-wMRIcT86SWU-unsplash.jpg "Man presenting to a group of people by Matthew Osborn in Unsplash")

Later, we had some lunch together, followed by our **final retrospective**. It was so much better to be able to do it in person, with almost everyone there in the office, sharing their experiences, thoughts, feelings, challenges and achievements during the course, seeing that we were not alone, and how much we had grown during the past 16 weeks. It was one of my favourite moments.

Finally, we had our **last presentation** in the new Makers offices, with some partners coming to see us and many people tuning-in online to watch it. You can see this presentation [here](https://youtu.be/jNPUt79UpsA) (we were the first group presenting, but if you have time, check the other projects, they were very cool!).

We were done, and we couldn’t believe it. After that, we got treated to some pizza and drinks while we had a chat to each other and the coaches. You could see everyone’s tension disappearing from their bodies, and then we had a really nice night out all together (we went to the pub, finally!).

![One of our presentation slides explaining our experience](/assets/images/theexperience.png "One of our presentation slides explaining our experience")


## About our application

<video controls width="300">
    <source src="/assets/images/FN.mp4"
            type="video/mp4">
</video>

List of features:
* A user can **register** and **login**. Their **session** will stay open on their phone until they decide to logout, even if they close the application.
* A user can **register adding their MP name**.
* A user can receive **push notifications** when their MP has just voted.
* A user can **see the most recent vote** on their screen, as well as **swipe** to check older votes.
* A user can get **redirected to a google search** of a particular vote directly from the application.
* A user can **emaill their MPs about a particular vote** by pressing the email button. This gives them direct access  to their email client and will be presented with a template, including their MP email address, the name of the division as a subject and a draft email.
* A user can **“Approve” or “Disapprove”** a vote and see a percentage of their MP’s approvals.

<p><img src="/assets/images/features.png" alt="A diagram of some of our features" width="600"></p>

Things we would have liked to do if we had more time (and may still do in the future):
* We were not particularly proud about the **code quality** and **lack of tests**. Although we initially decided we wanted to use TDD, we soon found out that React Native is not as easy to test as we expected. Part of our team spent two days trying to figure out how to do it unsuccessfully, and given the time pressure, we had to decide between having out MVP running by the end of those two weeks or having a small amount of code that was good quality but didn’t have enough functionality. 
* **Being able to change the MP** to look at what other MPs are doing– We had this feature almost working by the time of our presentation, but one of our team-members got really ill and we couldn’t merge it on time.
* Implement **user input and data validation and error handling**– This was initially done but only worked on web, causing serious bugs on the other platforms, so we needed to delete it due to the time constraints.
* User being able to **set their MP by writing a postcode**.
* Use users’ “Approves” and “Disapproves” anonymously to **gather data about how MPs are doing** and give them direct feedback of what the public really thinks about them and their votes.
* **Deploy our application** and put it in the App Store

# Resources we used this week:

* [Trello](https://trello.com) for our tickets
* [Excalidraw](excalidraw.com) and [Miro](miro.com) for our diagrams and ideas
* [Parliament](https://api.parliament.uk), [Members of Parliament](https://members-api.parliament.uk/api/) and [Commons votes](https://commonsvotes-api.parliament.uk) APIs
* [Expo installation](https://docs.expo.dev/get-started/installation/)
* [Blog on making a CRUD REST API with Node.js, Express and PostgreSQL](https://blog.logrocket.com/crud-rest-api-node-js-express-postgresql/)
* [The complete guide to testing React Native app using Cypress](https://glebbahmutov.com/blog/testing-react-native-app-using-cypress/)
* [Github repo using Jest to unit test and Cypress for end to end testing of React Native](https://github.com/bahmutov/ReactNativeTodo)
* [Download X-code for MAC](https://itunes.apple.com/us/app/xcode/id497799835?mt=12)
* [Making API calls in React Native using fetch](https://programmingwithmosh.com/react-native/make-api-calls-in-react-native-using-fetch/)
* [React Native video tutorial for beginners](https://www.youtube.com/watch?v=0-S5a0eXPoc&t=4212s)
* [Bundling with Webpack from Expo documentation](https://docs.expo.dev/guides/customizing-webpack/)
* [Login authentication video tutorial](https://www.youtube.com/watch?v=QMUii9fSKfQ&t=327s  https://youtu.be/QMUii9fSKfQ?t=341)
* How to create swipe gesture [here](https://instamobile.io/react-native-controls/react-native-swipe-cards-tinder/) and [here](https://www.geeksforgeeks.org/how-to-create-tinder-card-swipe-gesture-using-react-and-framer-motion/)
* [Deploying a Node.js Posgres/Sequelize app to Heroku](https://anjelicaa.medium.com/deploying-a-node-js-postgres-sequelize-app-to-heroku-da3dc9de07cd)
* [Passing data deeply with context](https://beta.reactjs.org/learn/passing-data-deeply-with-context)
* [How to generate apk using React Native Expo](https://dev.to/chinmaymhatre/how-to-generate-apk-using-react-native-expo-kae)


