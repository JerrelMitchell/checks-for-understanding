## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1.  List the five common HTTP verbs and what the purpose is of each verb.
    * GET - read information from page
    * POST - create new resource(s) for parent
    * PUT - update resource(s) of parent
    * PATCH - update part of a resource of parent
    * DELETE - delete resource(s) of parent
2.  What is Sinatra?
    * a language that helps with creating web applications with Ruby.
3.  What is MVC?
    * Model View Controller - pattern that separates applications into pieces that work together for developing an application
4.  Why do we follow conventions when creating our actions/path names in our Sinatra routes?
    * So others and our later selves can have an easier time reading and editing our code
5.  What types of variables are accessible in our view templates without explicitly passing them?
    * instance variables and local variables when
6.  Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
    * add '@count = 1' above the line containing erb, shown below.

```ruby
get '/horses' do
  @count = 1
  erb :index, locals: { name: 'Mr. Ed' }
end
```

8.  In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
    * adding a comma after the erb :index, followed by a locals key set to a value of a hash containing the name key set to a value of 'Mr. Ed'
9.  What's the purpose of ERB?
    * to embed html into our ruby code
10. Why do I need a development AND test database?
    * development database is used to work out bugs at the very base level of a project to ensure MVC is compatible, while a test database is used more when the project is getting ready for production.
11. What is CRUD and why is it important?
    * Create Read Update and Delete, ensures resources are able to be manipulated within the context of html
12. What does HTTP stand for?
    * Hyper Text Transfer Protocol
13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
    * string interpolations and erb template interpolations, erb template uses %=, string does not.
14. What's an ORM?
    * object relational mapping
15. What's the most commonly used ORM in ruby (Sinatra & Rails)?
    * SQL
16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

    * get '/restaurant'
    * get '/restaurant/new'
    * get '/restaurant/:id'
    * get '/restaurant/:id/edit'
    * put '/restaurant/:id'
    * delete '/restaurant/:id'
    * post '/restaurant'

17) What's a migration?
    * the set of commands used to move information from a database to a table
18) When you create a migration, does it automatically modify your database?
    * No
19) How does a model relate to a database?
    * It is the representation of the data in the database
20) What is the difference between `#new` and `#create`?
    * new needs a following save command to ensure the resource is saved. create does new and save for the resource.

### Review Questions:

21. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?
    * Film.create(id: film[:id], title: film[:title], film[:description])
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

* activities[:hiking][:supplies] << 'granola bar'

23. What are the 4 Principles of OOP? Give a one sentence explanation of each.
    * Encapsulation - Hiding data implementation by restriction of public access to methods
    * Abstraction - one class should not need to know the inner details of another in order to use it
    * Inheritance - derived classes can reuse code of superclasses
    * Polymorphism - method overriding and method overloading.

### Self Assessment:

Choose One:

* I was able to answer a few questions independently, but relied heavily on outside resources

Choose One:

* I feel overwhelmed by the content presented this week
