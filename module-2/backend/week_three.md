## Week Three Recap

### Instructions

Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1.  What is the entry at the command line to create a new rails app?

* rails new <PROJECT-NAME>

2.  What do Models generally inherit from in rails?

* ApplicationRecord

3.  What do Controllers generally inherit from in a rails project?

* ApplicationController

4.  How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

* resources :horses, only: :show

5.  What rake task is useful when looking at routes, and what information does it give you?

* rake routes, all path names, verbs, url names, and corresponding controller action

6.  What is an example of a route helper? When would you use them?

* example_path(@example), when you refactor your code to be more readable and less brittle in your controllers and views to redirect to, render, or link to them.

7.  What's the difference between what `_url` and `_path` return when combined with a routes prefix?

* `_url` is used when you need the absolute URI in order to get the https:// prefix for a secure site and to get the http:// prefix if you need to get back to where you were. `_path` seems to be used for pretty much everything else outside of the controller redirects.

8.  What are strong params and why are they necessary?

* strong params only allow the specified information/keys through the params to be used on the website. so primarily for security and preventing manipulation of your database or webpage.

9.  What role does `form_for` play in helping us create our forms?

* it tells us which attribute is being named/used for the form

10. How does `form_for` know where to submit the user's input?

* with form labels and naming conventions as keys of the different fields associated with them.

11. Create a form using a `form_for` helper to create a new `Horse`.

* <%= form_for(@horse) do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.label :breed %>
  <%= f.text_field :breed %>
  <%= f.submit 'Create' %>
  <% end %>

12. Why do we want to validate our models?

* to ensure that only valid data gets saved into a database.

13. What are the steps of the DNS lookup?

* query > root server > tld name server > reaches dns > website appears

### Review Questions

14. How would you call the method `prance` from within the method `move` on a `Horse` instance?
    * horse.move.prance
15. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```

What is the different between how you would return true vs returning 3?

* furniture[:purchased] vs furniture[:table][:height]

16. What is inheritance?

* when a class inherits methods/behaviors from a superclass

### Self Assessment:

Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel overwhelmed by the content presented this week
