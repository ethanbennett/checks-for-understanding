## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app? rails new AppName
2. What do Models generally inherit from in rails? ApplicationRecord
3. What do Controllers generally inherit from in a rails project? ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality? resources :horse, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you? rake routes--gives prefix, verb, URI, and Controller#Action
6. What is an example of a route helper? When would you use them? I think the route helper is the shortcut, i.e. jobs_path, and can be used to reference specific URI paths.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix? URL includes unnecessary information in views ("http://localhost:3000/companies") rather than the shorter path ("/companies")?
8. What are strong params and why are the necessary? They filter out unwanted or unneeded data from the user's valid input
9. What role does `form_for` play in helping us create our forms? It simplifies the routing and connects the form with whichever object we declare as an argument
10. How does `form_for` know where to submit the user's input? It can figure it out based on the object (eg @company) we provide
11. Create a form using a `form_for` helper to create a new `Horse`. 
<%= form_for @horse do |f| %>
<%= f.label :name %>
<%= f.text_field :name %>
<%= f.submit %>
<% end %>
12. Why do we want to validate our models? It can cause confusion or skew our analysis if we save empty or partial rows in the table, and the inclusion of nil could cause errors that keep pages from loading properly.
