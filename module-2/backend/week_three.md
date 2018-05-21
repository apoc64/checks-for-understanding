## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
rails new project_name -T -d="postgresql" --skip-turbolinks --skip-spring 

2. What do Models generally inherit from in rails?
ApplicationRecord

3. What do Controllers generally inherit from in a rails project?
ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
resources :horses [only: show]

5. What rake task is useful when looking at routes, and what information does it give you?
rails routes

6. What is an example of a route helper? When would you use them?
horse_path(horse) - use in links, redirects, feature tests

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
_url shows the full path with http://... _path is just within the site

8. What are strong params and why are they necessary?
They are used for security. There is a private method and specific params are allowed

9. What role does `form_for` play in helping us create our forms?
It starts a form block with rails methods to create html forms

10. How does `form_for` know where to submit the user's input?
From the controller method

11. Create a form using a `form_for` helper to create a new `Horse`. 
Controller:
def new
  @horse = Horse.new
end
View:
<%= form_for @horse do |f| %>
<%= f.label :name %>
<%= f.text_field %>
<%= f.submit %>
<% end %>

12. Why do we want to validate our models?
To make sure that necesary fields are actually there

13. What are the steps of the DNS lookup?
The browser goes to the OS. The OS looks on the internet to see where the domain is located


### Review Questions
14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
def move
  prance
end

15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3? 
furniture[:purchased] vs furniture[:table][:height]

16. What is inheritance?
It's where a class gets methods and attributes from a superclass

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week/
* I feel overwhelmed by the content presented this week
