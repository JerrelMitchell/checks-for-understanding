## Week Four Recap

### Instructions

Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1.  What is a cookie?

* data stored as reference for other data in a users browser

2.  What’s the difference between a session and a cookie?

* a cookie is stored on a website visitors browser, a session is stored on the database

3.  What’s a flash and when do you want to use flashes?

* a flash is typically a message that pops up confirming an action has taken place (such as creating/destroying/editing a model)

4.  Why do people say “HTTP is stateless”?

* because it does not remember any data previously passed through it

5.  What’s authentication? Explain.

* authentication is basically asking who you are.

6.  What’s the difference between authentication and authorization?

* authentication is determining who you are, authorization is determining what you're allowed to do

7.  What’s a before filter?

* it's a way to set a method in a controller to happen before the (optionally specified) action(s) take place. like if you want to set an instance variable equal to found params of a model. Used to DRY up controllers.

8.  How do we keep track of a user once they’ve logged in?

* by use of sessions

9.  When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

* a namespace is used when you don't need restful routes. a nested resource gives many routes and full restful route lists of both resources used in the nesting.

10. At a high level, what tools can you use to implement authorization? How would you use them?

* set attributes for roles in a User model, add access rules to controller actions, restrict access to prohibited pages, create actions to check roles in view templates that display content with conditional statements

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

* an enum is declared at the model level where validations and relationships are declared, and is typically used to add 'state' to an object when you would like to either sort or find data in the database by the data specified by the enum. A couple of examples being if you wish for a user to be a default user or an admin, or an item being listed as discontinued or available. The advantage of using an enum is to have your code be more readable, which helps lead to fewer errors when writing and maintaining your code.

12. What are some strategies you can use to keep your views DRY?

* implement forms in the particular model view directories, or in your application layout for a navbar for instance. can also implement branch logic at the controller and view levels so the view only has access to information needed.

### Reviews Questions

13. Given the following array of hashes, how would I print an alphabetical list of holidays?

```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}
]
```

    * given.includes(:holiday).order('name ASC')

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?

    * create a method that takes in an argument and returns the string as an integer.
    * ex:
    * def number_cleanup(num)
    * clean_num = num.to_i
    * return 0 if clean_num.nil?
    * end

### Self Assessment:

Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel overwhelmed by the content presented this week
