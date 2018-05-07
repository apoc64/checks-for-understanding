## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
Get - Used for reading a resource
Post - Used for creating a resource
Put - Used for editing a resource
Delete - Used for deleting a resource
Patch - Used for updating part of a resource

2. What is Sinatra?
A web framework for Ruby.

4. What is MVC?
Model View Controller - a way to structure your code/files and design your app

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
So Sinatra finds the right files in the right places - ie erb files in the views folder. Also, because if someone else looks at it, it should make sense

6. What types of variables are accessible in our view templates without explicitly passing them?
instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
{locals => {name: 'Mr. Ed'}

9. What's the purpose of ERB?
Its a templating language for creating dynamic HTML with Ruby

10. Why do I need a development AND test database?
So you can have seed data in the development database for use in a browser, but you can start with a fresh, empty db everytime in your tests

11. What is CRUD and why is it important?
Create, Read, Update, Delete - beacuse thats the basics of all database apps, you can't do anything else if you don't have CRUD


12. What does HTTP stand for? 
Hypertext transfer protocol

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<% %> just runs the code
<%= %> outputs the results to the HTML file

14. What's an ORM?
Object Relational Mapping - Used for dealing with databases with objects

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
Active Record

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
get /restaurants - shows them all
get /restaurant/id - shows one of them
get /restaurant/new - shows a form to create one
post /restaurant/id - creates a new one
get /restaurant/id/edit - shows a form to edit one
put /restaurant/id - updates one of them
delete /restaurant/id - deletes one of them

17. What's a migration? 
Making a change to a database

18. When you create a migration, does it automatically modify your database?
You have to run it - rake db:migrate

19. How does a model relate to a database?
Only the model talks to the database

20. What is the difference between `#new` and `#create`?
new just makes an object, create saves it in the database

### Review Questions:  
21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
films = CSV.read("films.csv", headers: true, header_converters: :symbol)
films.each do |line|
  Film.create!(id: line[:id]
  title: line[:title]
  description: line[:description])
end

22. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone'],
  brunch: {cost: $35, supplies: ['mimosa flutes'],
  antiquing: {cost: $200, supplies: ['list of antique stores'] 
}
```
How would I add 'granola bar' to things you should have when hiking?
activities[:hiking[:supplies]] = 'granola bar'

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
Encapsulation - Don't expose things you don't have to
SRP - Single Responsibility Principal - objects sould do only one thing



### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few
Copied out of little shop for the CSV read


Choose One:
* I feel confident about the content presented this week
Conceptually I understand it. I need to get to the point where I can actually write it and fix bugs faster
