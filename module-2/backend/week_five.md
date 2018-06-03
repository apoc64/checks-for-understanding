### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 5 Questions
1. How do we make flash messages display on a page?
flash[:notice] = "message"  - can use error or any other type, then call them in your view, best to use application layout, so they always show up

2. Where is cart information/temporary information usually stored?
session, you can create a PORO to work with the session data

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
If you stored in a database it would take up extra space, and if the cart belonged to a user, then a non-logged in visitor couldn't add to cart. There are reasons to persist it. If a user logs in much later on a different device, they should still be able to see their cart

4. What is the purpose of the asset pipeline?
It feeds CSS, JS, and images to the client efficiently. CSS and JS are minified to take up less space

5. Why do we precompile our assets?
So we can see them they way they will be in production

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %> Links to the application.css in the assets folder which will be sent through the asset pipeline
<%= javascript_include_tag "application" %> Same thing but javaspript
<%= image_tag "rails.png" %> Links to an image in the assets/images folder. The file extension becomes necessary in production
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
Explains the project, says how to install it and how to test it

8. What are the top four accessibility issues that we as developers should be aware of?
Blind/visually impaired, non-english speakers, color-blind, ???

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
Callback - ApplicationRecord or in an ActiveRecord class

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```

11. What is the difference between a scope and a class method?


### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  cart["48"] = 4
  12b. How would you increase the quantity of item 29?  cart["29"] = cart["29"] + 1
  12c. How would you find out how many items your user is thinking about purchasing?  Go through all the keys, and add up all the total values 
  
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications? 
A principal of object oriented programming, many changing
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  Remove ()-. and anything else that isn't an integer


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
