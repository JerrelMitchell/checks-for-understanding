## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.

### Week 2 Questions

1.  At a high level, what is ActiveRecord? What does it do/allow you to do?
    * enables creation, use, and storage for data / data tables.
2.  Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

* .find(id)
* .find_by(key, value)
* .create!(keys, values)
* .delete(id)

* You get access to them through the ActiveRecord::Base superclass

3.  Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

* Team.find(4)
* Team.find(4).owner

4.  Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

* Team.owners.find(4)

5.  In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

* One Teacher to Many Students

6.  Define foreign key, primary key, and schema.

* foreign key is typically an id on the belongs_to relationship table (the previous example would have a teacher id on the student table). primary keys are those keys associated with presenting table (such as a student name being on a student table). schemas are the files that hold these keys and establish relationships between them when/if desired.

7.  Describe the relationship between a foreign key on one table and a primary key on another table.

* say you have a teachers table and a students table, a teacher id on a student table would be a foreign id while the corresponding id on the teacher table would be the primary key

8.  What are the parts of an HTTP response?

* status line
* optional header(s)
* optional message/body

### Self Assessment:

Choose One:

* I was able to answer most questions independently, but utilized outside resources for a couple

Choose One:

* I feel comfortable with the content presented this week
