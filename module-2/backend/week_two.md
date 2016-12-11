## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR. 

1. At a high level, what is ActiveRecord? What does it do/allow you to do? It allows us to interact with databases without having to memorize all the complexities of SQL.
2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

Our class inherits from a "normal" Ruby module (or class) that defines some methods for us. Without setting up associations, it allows us to do some basic CRUD and array mapping stuff, like .update, .delete, .all, etc.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

Team.find(4)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
team = Team.find(4)
team.owner

3. What do they allow you to do? Is "they" associations? They allow for more specific methods for dealing with the data in your database in terms that make sense in your particular context (i.e. they follow the relational schema you define)
7. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
A student has one teacher, but a teacher has many students. Since I can't do much diagramming here: I would add a foreign key of "teacher_id" in my students table, which would connect the two.

8. Define foreign key, primary key, and schema.
Primary key: A unique identifier for each row in a table.
Foreign key: A reference to the primary key of an object in another table, which can be used to establish a relationship between the two tables.
Schema: An automatically generated map of the table setup in a database (how many columns, what they're called, what type it expects them to be, etc.)
9. Describe the relationship between a foreign key on one table and a primary key on another table. Foreign keys are primary keys for another table, so SQL knows how to relate the data in both.
10. What are the parts of an HTTP response? Head, body? Or verb, path? 
11. Describe some techniques to make our Sinatra code more DRY. Give an example of when you would use these techniques.
I actually didn't find myself repeating much with Sinatra, since it required a lot less code than the Black Thursday/HTTP iterations of these types of tasks. We did extract some methods into a helper class for our controller, but we only had a couple methods that qualified. I did notice it's easy to repeat yourself in RSpec though.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
4. What can you expect from a group as you begin working together? As you continue working together?
5. What two columns does `t.timestamps null: false` create in our database?
6. What cURL flag can you use to send a `POST` request?
7. What case does JSON (and JavaScript) use for multi-word variables?
8. What case does Ruby use for multi-word variables?
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
11. Give an example of when you might want to store information besides ids on a join table.
12. Describe and diagram the relationship between patients and doctors.
13. Describe and diagram the relationship between museums and original_paintings.
14. What are some examples of acceptable values for the parts of an HTTP response?
15. What types of output do we want to test when we test our controllers?
16. What could you see in your code that would make you think you might want to create a partial?
17. Why might you use a helper method?
