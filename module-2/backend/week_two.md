## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
ORM - Object Relational Map - it goes between your Ruby objects and your database with a lot of useful methods and built in behavior

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
Team.all, Team.find, Team.create... They inherit from ActiveRecord::Base

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
Team.find(4), Owner.find(Team.find(4).owner_id)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```
Team.find(4).owner

Now how would you find the owner of the team with an id of 4?

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
How do I draw in here?
teachers have many students
??students belong to teachers or students have many teachers with a join table of student_teachers

6. Define foreign key, primary key, and schema.
Students:
Primary key - The main way you identify records in a table. They are always unique
Foreign key - Defines the relationship of a row in one table to a row in another table
Schema is the structure of all the tables and columns ina database 

7. Describe the relationship between a foreign key on one table and a primary key on another table.
A foreign key in one table is always a primary key in another table

8. What are the parts of an HTTP response?
Response code, headers with information about the response, body including HTML, CSS, JS


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
.all - Class method that returns an array of all the members of that class
.find(id) - Finds a specific record by its primary key
.create - created a new record and saves it in the database
.update - changes attributes of that record and saves it in the database
.destroy - removes it from the database

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
rake db:create - creates the databases for your project
rake db:migrate - runs your migrations to make changes to the database
rake db:reset - gets rid of everything in the db and re-migrates and seeds

3. What two columns does `t.timestamps null: false` create in our database?
created_at and updated_at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
The answer you're probably looking for is schoold have many teachers and teachers belong to school... except when one teaches at multiple schools which does sometimes happen

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
Add a school_id to teachers ... again with the drawing

6. Give an example of when you might want to store information besides ids on a join table.
InvoiceItems with a unit price

7. Describe and diagram the relationship between patients and doctors.
many to many - 
patient_doctors have foreign keys for patients and doctors

8. Describe and diagram the relationship between museums and original_paintings.
one to many - paintings have a foreign key for museum_id

9. What could you see in your code that would make you think you might want to create a partial?
repeated html

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
-- I need to get faster with Rails --
