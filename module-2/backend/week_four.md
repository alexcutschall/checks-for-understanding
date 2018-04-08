## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
A cookie is a small bit of storage that gets stored on the browser when a user visits a website and then gets sent
back to the server during each request with that information so it doesn't have to be loaded every time.
2. What’s the difference between a session and a cookie?
A session can store larger amounts of data or can be what a cookie points to. As a cookie is quite small, the session
allows the developer to store larger amounts of data without a loss in performance.
3. What’s a flash and when do you want to use flashes?
A flash is a message that comes up on a page to notify the user of some interaction. Some examples would be
if a user logged in correctly, if they had an incorrect password, or they successfully created a new resource
(such as a tweet on Twitter).
4. Why do people say “HTTP is stateless”?
HTTP doesn't 'remember' anything about the user, that's why we use sessions and cookies
5. What’s authentication? Explain.
Authentication boiled down is the application knowing who the user is and how to cater the site to their information.
6. What’s the difference between authentication and authorization?
Authentication simply records who you are where as authorization permits or restricts users depending on their
role in a site ex: user or admin.
7. What’s a before filter?
This allows you to run a method that restricts who is allowed a certain action.
8. How do we keep track of a user once they’ve logged in?
We keep track of them through a method in ApplicationController called current_user
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
Namespace allows you to create nested paths without creating an entire resource for the namespace. Use of namespace
include admin privileges. You don't want to create a new admin resource, but you want your resources nested within.
You use nested resources when you have two different resources, but you want one to be accessible through another
resource.
10. At a high level, what tools can you use to implement authorization? How would you use them?
Bcrypt. OAuth. You use Bcrypt to encrypt your passwords and you use OAuth to authorize through other websites
such as Twitter and Facebook.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
An enum is a way to declare different roles that you can assign to your users. You declare an enum in the model.
12. What are some strategies you can use to keep your views DRY?
Forms and Partials


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```  
holidays.sort_by do |holiday|
  holiday[:holiday][:name]
end

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
  string = "$300"
  string = "300.00"

  if string.include?($)
    string.delete($).to_i
  else
    string.to_i
  end

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel confident about the content presented this week
