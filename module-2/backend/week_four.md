## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie? A message from the browser to the server
* What’s the difference between a session and a cookie? Cookies are stored in the browser, sessions in the server.
* What’s a flash and when do you want to use flashes? Messages that appear on a view only in certain contexts.
* Why do people say “HTTP is stateless”? It has no memory: if we want to save any data about the user, it needs to happen in the browser, the user's machine, or the hosting server.
* What’s authentication? Explain. Authentication is the process that verifies a user's identity in some way (e.g. username and password)
* What’s the difference between authentication and authorization? Authorization determines what kind of access a user has (what actions they're allowed to take on your app/DB)
* What’s a before filter? If there are any methods in a controller that need to happen before requests pass through specific actions, you can add a before_action at the top that will run the methods automatically.
* How do we keep track of a user once they’ve logged in? Cookies, sessions, or both.
* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches? Nesting resources allows them to be connected, e.g. comments on job pages. You shouldn't ever need to see all the comments outside of their context in jobs, so you should nest them. I can't remember namespacing well, but I think it allows for the opposite: instead of companies/jobs/cities, you could use namespace to make a URL for just jobs/cities.
* At a high level, what tools can you use to implement authorization? How would you use them? I think you'd just use conditionals on your views: if a user is an admin, show CRUD functionality, etc.
* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum? I can't really remember...I assume it's enumerable, so the DB would need a datatype like a hash or an array.
* What are some strategies you can use to keep your views DRY? Partials, POROs with repeatable methods
