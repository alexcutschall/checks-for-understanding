### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
We add code into the application.html.erb to have it display.

2. Where is cart information/temporary information usually stored?
A PORO where a hash is held

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
Every single time someone added an item to the cart, you would have to send a request to the database which
would slow it down a lot. You would also have a ton of extra information polluting your database

4. What is the purpose of the asset pipeline?
Previously, every time a web page was loaded, it had to ping every single time for html and css and javascript. The
asset pipeline pulls all this into one single file that gets called. Then when the website pings the server
it just checks the cache(fingerprint) to see if it's the same file.

5. Why do we precompile our assets?
Concatenation, Minification, and allows us to use higher level languages

6. What do each of the following tags do?

```ruby
<%= stylesheet_link_tag "application" %> - Links to a certain stylesheet
<%= javascript_include_tag "application" %> - Generates HTML that links views to feeds
<%= image_tag "rails.png" %> - This allows you to load an image in erb
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
Concise, Simple, Setup/Installation- Code Snippets
Good Read Me's are a nice cherry on top of a project and a simple way to show that you care about your product

8. What are the top four accessibility issues that we as developers should be aware of?
Keyboard accessibility, Text alternatives, Simple functionality, semantic structures

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
Callback, In the model

10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```

User.find_by(active: true)

11. What is the difference between a scope and a class method?
A class method can be called on an collection of that resource where as scope can only
be performed on a specific instance of that resoruce


### Review Questions:  
12. Given the following hash:  

```ruby
given = {cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?
  given[:cart]["48"] = 4

  12b. How would you increase the quantity of item 29?  
  given[:cart]["29"] + 1

  12c. How would you find out how many items your user is thinking about purchasing?
  give[:cart].values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
Polymorphism allows to write a structure in a similar fashion as something else like an array or hash so that you
can use it is similar ways. Duck typing is a similar philosophy. Using ActiveRecord "arrays" and also "instances"
of resources coming out of your database

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
x.delete("()").gsub(/\s/,'.').gsub(/-/, '.')

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel confident about the content presented this week
