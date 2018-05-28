## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
A cookie is stored by the clients browser and sent to the server with the HTTP request to help creat state with stateless HTTP

2. What’s the difference between a session and a cookie?
Session is stored on the server. The client can't read or edit it

3. What’s a flash and when do you want to use flashes?
It's a message sent from a controller. They're good for informing of creation, deletion, loggin in, etc

4. Why do people say “HTTP is stateless”?
It doesn't remember what went on before. It doesn't know if its logged in, etc.

5. What’s authentication? Explain.
Verifying who the user is - ie. passwords

6. What’s the difference between authentication and authorization?
Authentication is verifying identity. Authorization is who can access certain pages/data, etc.

7. What’s a before filter?
They get called before any controller action, you can check if a user is logged in

8. How do we keep track of a user once they’ve logged in?
session

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
Namesapce - if only certain users, ie. admin can access
Nested - if a resopurce belong to another respource - ie. merchan/items

10. At a high level, what tools can you use to implement authorization? How would you use them?
Hashed passwords - they are stored in an unreadable form in the database and when a user attemptas to log in they can be checked

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
Its something stored as an integer in a database, that active record can turn into various values - ie default, admin

12. What are some strategies you can use to keep your views DRY?
Partials


### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```  
given.sort_by do |holiday|
 holiday[:holiday][:name]
end

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300? 
strip away $, to_i

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
