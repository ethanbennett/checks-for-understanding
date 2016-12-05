## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.
Get: Retrieves information to display on the screen
Post: Returns data from user to the server
Patch: Same as post
Put: Updates information
Delete: Destroys information
2. What is Sinatra? A framework for interpreting Ruby code and displaying it in a browser.
4. What is MVC? Models, Views, Controllers -- Models are the objects/classes, views are the rendered browser displays, controllers determine the path functionality
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes? It makes it easier to follow for users and easier to comprehend for other developers.
6. What types of variables are accessible in our view templates without explicitly passing them? Instance
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    name = "Mr. Ed"
    erb :index, locals: name
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed`?
9. What's the purpose of ERB? It allows the HTML structure of the page to understand and interpolate Ruby code
10. Why do I need a development AND test database? It allows the developer to only load as much data as necessary in the tests (improving speed) and keeps the real database free of irrelevant data the developer might add just for the purpose of testing.
11. What's responsive design? The page's content responds to the window size.
12. What is CRUD and why is it important? Create Read Update Destroy--it's the basic for framework necessary for any effective database
13. What does HTTP stand for? Hypertext Transfer Protocol
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways? <% %> || <%= %> ; The latter specifies a return value, often but not always printed to the screen.
15. What's an ORM? Object Relational Method
16. What's the most commonly used ORM? ActiveRecord
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
get '/'
get '/trips'
get '/trips/new'
post '/trips'
get '/trips/:id'
put '/trips/:id'
delete '/trips/:id'
18. What's a migration? Migrations create or update databases through the ORM.
19. When you create a migration, does it automatically modify your database? Not necessarily, it just enacts your code if you did modify it.
20. How does a model relate to a database? via ORM? Each row is an instance of an object.
21. What's the difference between agile workflow and waterfall method? Little bits at a time vs. start to finish
22. What is the difference between `#new` and `#create`? #create = #new + #save
