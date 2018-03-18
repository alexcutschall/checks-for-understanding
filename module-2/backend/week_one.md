## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
GET, POST, PUT, PATCH, DELETE
2. What is Sinatra?
Sinatra is a DSL
4. What is MVC?
Model, Views, Controller is the standard way to structure a Sinatra website
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
We use RESTful routes
6. What types of variables are accessible in our view templates without explicitly passing them?
None
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
```ruby
get '/horses' do
  @name = 'Mr. Ed'
  erb :index
end
```
9. What's the purpose of ERB?
Embedded Ruby allows us to run Ruby code within HTML
10. Why do I need a development AND test database?
A development database may change, where as you want your test database to test certain inputs and outputs
11. What is CRUD and why is it important?
Create, Read, Update, Delete. It is how we manipulate our resource data
12. What does HTTP stand for?
HyperText Transfer Protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<%  %>, <%=  %> The second one prints out the result where as the first just runs the code
14. What's an ORM?
Object Relational Mapping, turns resources into Objects and let's us interact with them
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
Activ Record
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
1) GET, List Resources
2) GET, Create form for resource
3) POST, Create Resource
4) GET, Get a Resource
5) GET, Edit a resource form
6) DELETE, Delete a resource
7) PUT/PATCH, Edit Resource
17. What's a migration?
They are a way to alter your schema over time
18. When you create a migration, does it automatically modify your database?
No it doesn't. You have to run rake db:migrate
19. How does a model relate to a database?
A model is how we interact with the information within the database
20. What is the difference between `#new` and `#create`?
New requires us to save the object afterwards while create does both

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
CSV.foreach('/films.csv',
            headers: true,
            header_converters: :symbol) do |info|
            Film.create(id: info[:id],
                        info[:title],
                        info[description])
                        end
22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?

activites[hiking][supplies] << 'granola bar'
23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
Encapsulation: Any object should only reveal as much information about itself as absolutely necessary.
Abstraction: Being able to work with an object without knowing exactly how that object works
Inheritance: An object can take on properties of another object
Polymorphism: The ability to process an object through several ways


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week
