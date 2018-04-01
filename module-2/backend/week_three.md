## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
rails new <project name>
2. What do Models generally inherit from in rails?
ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
'horse#show'
5. What rake task is useful when looking at routes, and what information does it give you?
rake routes/rails routes, shows you all of the available routes and how to access them
6. What is an example of a route helper? When would you use them?
Get /movies index movies/path
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
a url contains the entire pathway where as a path is just /movies
8. What are strong params and why are they necessary?
They are a security measure to ensure that what goes into your database is what you want entered
9. What role does `form_for` play in helping us create our forms?
It allows us to create the pathway for the type of resource that we are creating/editing
10. How does `form_for` know where to submit the user's input?
It grabs it from the controller as it's passed down
11. Create a form using a `form_for` helper to create a new `Horse`.
<%= form_for @horse do |t| %>
<%= t.label :name %>
<%= t.text_field :name %>
<%= t.submit %>
<% end %>
12. Why do we want to validate our models?
To make sure that the resources in our database has what we want
13. What are the steps of the DNS lookup?
It receives a query, which sends it to the TLD name server, which sends it to the DNS and it gets sent back.


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
horse.move.prance
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
16. What is inheritance?
Inheritance is when a class obtains certain methods/attributes based on it's Superclass.

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
