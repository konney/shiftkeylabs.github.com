---
layout: post
category : Reflective blog
title: "February 2, 2016"
author: Brian Yip
tags : [blog]
---
# February 2, 2016

##Summary
This week was extremely busy. I applied to about five different jobs and interviewed at two companies.

However, the main focus of this blog is meeting new people in the industry outside of school. I went to **Global Game Jam** on the weekend. This event is like a hackathon, except that it does not have the competitive aspect of winning a big money prize for the best game.
</br>
![Global Game Jam 2016](http://gamecenter.nyu.edu/wp-content/uploads/2016/01/Screen-Shot-2016-01-04-at-3.31.27-PM.png)
</br>
At this event, I was again exposed to rapid innovation and development. Although my team did not get any feedback on our product, I did learn that in hackathon events, it is more important to focus on delivering something that the end-user can see. Although I did not plan a group in advance, I believe that groups formulated in advance are generally better prepared. This is because they have already agreed upon the technologies and frameworks they are going to use. At the event, they can then develop a simple idea to implement.

Our team's goal was to implement a strategy game where we could have a real board game with a companion app. Because we had a team of seven people, we split ourselves up into teams of two and three. This worked because everyone on our team possessed a diverse skillset. Because I took on a developer role, I worked with another developer on our board game's companion app.
___

## Companion app disaster
I have to admit, I came to the hackathon prepared to use Unity3D, but this was not the technology I ended up using. Being open-minded, I was willing to work with the technologies that would be most productive for my task.

I thought that the companion app should be used on mobile devices. In order to accomplish this, my team and I decided that we would use Angular.js for our front-end framework (most of us were also familiar with Angular.js).
___

### Sounds good so far, but what where is the disaster?
As I mentioned previously, in rapid development, developers do not have the time to implement too much software architecture. Me and the other developer I was working with made a few mistakes.

#####Mistake #1
We implemented the server-side in vanilla PHP and used that code to query our MySQL database. A better solution would have been to use an ORM (object-relational-mapping) leveraging an established web framework like [Laravel](https://laravel.com/), [Django](https://www.djangoproject.com/), or [Rails](http://rubyonrails.org/).

##### Mistake #2
We mixed PHP tags with Angular.js tags. Consequentially, we ended up burning Angular.js. A better solution would have been to let the front-end send asynchronous HTTP requests to a RESTful API instead.
___
## So What?
As mentioned before, a little preparation goes a long way for events that require rapid development. However, it is not simple to prepare for the unknown. By this I mean that I was planning to join a group and work with what they knew best so that I could learn from them. I knew that working in vanilla PHP was not going to turn out pretty, but why did I still go with it? This was because I did not fully understand all of the benefits of having an ORM and an MVC framework aid the structure of our app. Now I realize that this is extremely important because the ORM and MVC framework provide an easier way to query data from the database without having to waste too much time implementing all of the necessary custom queries. You also do not need to worry about re-establishing connections with your database because the web framework will handle all of that under the hood.

Most server-side web MVC frameworks also provide ways to quickly create RESTful APIs which would have been great for our integration of our Angular.js front-end.

If I were to have done this event again, I would have taken a leap of faith to learn a new web framework because not only would I have developed a useful skill, but I would have also been more productive and have started the app in the right way.
___
### What we did right
Despite our companion app disaster, the artists, designers, and story writers in our team were very good and finished all of their tasks on time. Why? Because they were prepared and already had the skills and tools. Our front-end design also looked great and was finished on time. Additionally, I felt like we worked very well together as a team. We were always in communication, got along well, and all easily came to an agreement on how were were going to implement our idea.

Additionally, I still liked the idea of MVC, so I structured our server-side using models, views, and controllers (in vanilla PHP). So even though we spent a bunch of time implementing our own little framework, I still felt like our code had some degree of structure to it.
___

### Now What?
- When building something from scratch, **ALWAYS USE A WEB FRAMEWORK**!
- When the group is formulating an idea, if you haven't already, **go research a web framework and start implementing a prototype as soon as possible.**
- Always use **ORM** to maintain **state** of data **models**. Trying to build a deliverable in 48 hours while also building your own MVC app is like playing with fire.
- Focus more on the **front-end** of the app and *less* on the business logic. The demo product needs something to show right?
- Once roles are established, it is better to have the **non-developers formulate the idea** while the **developers research tools and frameworks** so that they can develop faster without worrying too much about the low level details. Though it is still important to keep constant communication throughout the whole event so that developers still know what they are supposed to deliver.
- **Avoid mixing HTML tags** from different frameworks in a single HTML. (I.e. mixing Angular.js with vanilla PHP tags in a single html file is bad!)

___
## Where is the Code?
> [Right here](https://github.com/itsbriany/OCDOC)
