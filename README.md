Covidopoly Intern Getting Started Guide

Working on the covidopoly codebase is a privilege. Before you commit to the codebase, we need to be confident you’re up to speed on coding skills, the technologies we use, and the design patterns we follow.

We do a bunch of advanced stuff and specific patterns I’ve learned from making dozens of past projects. By the time you finish this getting started sequence, you’ll learn these without making all the design mistakes I’ve made over 5 years. 
Things you need to master
Typescript: This is the coding language of our front end and back end
React: What we use to build the front end user interface
State management (without redux)
Hooks (do not use class based React Components)
JSX (HTML)
Redux: This is how we manage state on the front end. Redux has solved a lot of problems I had when making big projects with React
CSS: This is how we make things look pretty
You’re going to need to be a pro at this especially
@emotion/styled is the library we use to use CSS in javascript files rather than css files. This also has solved a huge amount of problems I’ve had trouble with when making big apps.
Node: This is how we use javascript on the backend 
Express: makes node easier to use
Socket.io: allows real time communication
Github: Version control management system
Jeez, that’s a lot of words I don’t know, where do I start?
I think the best way to learn web development is by making dummy projects, and to start with the bare minimum amount of technologies. Here’s some example projects that you may want to do in order. You can follow these projects exactly, or try to extrapolate them to an idea you have that you’ll remake from scratch in each dummy project. After each project, we’ll go over them and talk about what went right and wrong. You’ll want to fix things before going  to the next project. You’ll learn the  design practices we use in covidopoly in these critique sessions, but the projects will be made initially by you calling all the design shots.

None of these projects should take a super long amount of time. It would take someone who knows how to do things a few minutes to a few hours depending on the project, although it will take you longer as you’re learning things for the first time.
Coding mentality
Coding is all about being able to learn new things fast. If you don’t know a tech, first try reading the docs. If the docs don’t make sense, look up youtube videos on those parts. Experiment with how things behave on your own too to get an intuition. Remember everything in the coding world should be seen as a tool. Algorithms, libraries, etc. are tools you can use to get your job done.

If you feel totally lost, you’re probably going to figure things out soon. That feeling of desperation makes you open to any new way of seeing things. Sometimes all it takes is saying to yourself “How hard can this be?” to change the way you see things that seems to make no sense.  If you feel like you’re thrashing with no progress, reach out to me and I can give some pointers.

Good coders know how to get things done. Once good coders get to a point where they feel comfortable being able to use different technologies, they often stop improving. Once you get to this stage, you should be looking up or buying books about best practices and design practices on these technologies. Good coders get things done, but often in messy ways. Great coders write clean code. 

Every time you pick up a new project, make sure to use one or two new technologies in it so you’re always learning. That is how this project sequence was designed.

Beware of blindly trusting stack overflow. A lot of code on there may work, but is disgusting, out of date, and should not be emulated. 
First  Make a github repo that will house all these projects
Go to github.com and make a free public repo. All projects should be pushed to this repo. One directory (folder) per project. If you refactor a prior project in your new project, make sure to copy all the code from the old project into a new directory before you start working.

If you aren’t familiar with github, watch youtube videos until you are.




rootGithubDirectory  
→ projectOne
→ projectTwo
... etc.

Make a Counter App User Interface with just HTML and CSS
Any static website will do. You could make a portfolio site, or just the user interfaces for a few pages for a project you’re passionate about that you might want to re-make in each of these example projects. Make sure there’s multiple unique pages in this project. I’d recommend a counter app with buttons to increment, decrement, or reset the value. These buttons should not work

Don’t use React or any other libraries. You need to get experience doing things the traditional way so you know why the libraries we use are important. 

Don’t expect any dynamic website on this project. This is purely to make things look pretty. You  probably don’t need javascript.



Rewrite your static website in React
Here’s where you’re going  to use lots of javascript. You’ll see how React makes web dev way less janky and more powerful. It’s still a static website, so nothing too fancy.

Do not use class based components. If you’re writing this, you’re doing things the old fashioned way. 
class MyComponent extends React.Component {
   ....
}

Only use function based components
function MyComponent() {
   ...
}
Create a dynamic counter website (front end only)
React is not just useful to make HTML easier to manage. It provides nice abstractions that allow you to change what’s rendered on the page without getting into the nitty gritties of dom management (not covered in these dummy projects).

I’d recommend starting with a website that provides a counter with buttons that increment the count, decrement the count, and resets the count to zero. The count can’t go below 0. 

Optional: If you have a project idea you’ve been making in past dummy projects, make it fully functional. Although I would make the counter app before this.  If it’s a game, you can’t play with other people over the internet in this project. So make sure it’s single player, or make it multiplayer but realize that both players would have to use  the same screen to play.

Refreshing the page will probably wipe your entire state in this project.

Make sure to be really familiar with hooks in React, especially useState, useEffect, useRef. You probably should NOT be querying for elements manually using doucment.geElementBy* or document.querySelector.
Create a dynamic counter website using redux
Although it’s not as important in small apps like a counter app, redux is a godsend in making big apps.It allows you to hook into a global state object (called a store) from any component in the dom tree. This avoids the callback hell you might have experienced in the previous dummy projects. You’ll learn to love redux. You don’t need to rewrite your app from scratch if you don’t want to in this project. You should be able to refactor your code to use redux.

Replace your css files with @emotion/styled
CSS is great, but has a bunch of rough parts that are hard to manage in big apps. The globally scoped style sheets are especially nasty. Plus CSS is a weak technology since you don’t have any concept of dynamic variables.

Get rid of all your css files in your dynamic project and replace them with styled components using the @emotion/styled library. Now css lives with your javascript components in the same file.

Add a backend to your dynamic site using node/express
For the counter app, make sure that users can retain their count state after reloading the page.
If you had another project you’ve been doing in this sequence, make it fully functional. Try doing it without socket.io

Use socket.io to make a real time chat app.
Make a real time chat app. If you have another project, integrate socket.io if it makes sense. You could try replacing your GET and POST requests from the backend with socket.io in the counter app.