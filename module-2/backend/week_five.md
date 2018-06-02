### Week 5 Questions

Re-pull from this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions

1.  How do we make flash messages display on a page?

* having a flash notice object in the view and the message the object is assigned to in the controller actions' logic

2.  Where is cart information/temporary information usually stored?

* in a cookie / session or database

3.  What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?

* interested in keeping information when not storing cookies or if browser is closed/cleaned

4.  What is the purpose of the asset pipeline?

* compressing javascript/css files/assets

5.  Why do we precompile our assets?

* make the data being grabbed/read smaller so it doesn't take as long for a user to load it

6.  What do each of the following tags do?

<%= stylesheet_link_tag "application" %>

* links to application stylesheet for use by the view(s)
  <%= javascript_include_tag "application" %>
* links to application javascipt used by the application(s)
  <%= image_tag "rails.png" %>
* adds an image to the view

7.  What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

* explaining what a project does for a user and tells the story of what the code is trying to do for a developer or your future self.
* helps with having something to glance over/read to understand the concepts behind your code/project

8.  What are the top four accessibility issues that we as developers should be aware of?

\*

9.  `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

* callbacks. model level.

10. Given the following object, how would we create a scope for all users who are active?

* scope: :active_users, -> (active) { where("users.active", active) }

```ruby
User.create(name: "Happy", active: true)
```

11. What is the difference between a scope and a class method?
    * scopes express intent, when doing more than chaining built-in scopes to create larger scopes use class methods.

### Review Questions:

12. Given the following hash:

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

12a. How would you add item with id of 48 with a quantity of 4?

* given[:cart]["48"] = 4
  12b. How would you increase the quantity of item 29?
* given[:cart]["29"] += 1
  12c. How would you find out how many items your user is thinking about purchasing?
* given[:cart].values.sum

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?

* means a subclass can override a method of the base class. they're both features a language can have. you can use polymorphism by over riding a method like count in a poro or model. you can use duck typing to implement certain actions or data through multiple controllers or views.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?

* given.gsub(/\D/, '')

### Self Assessment:

Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel overwhelmed by the content presented this week
