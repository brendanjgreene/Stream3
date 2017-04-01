# INTRODUCTION

Now that we’ve had some experience in creating more complex relationships in our models, and also in packaging our apps into reusable packages that we can store on GitHub, we begin to see the power of the Django framework in action!

In this lesson, we will create a user authenticated forum.

We’ll also start filtering the forum’s functionality, based on who owns the content and whether or not they are logged in
- giving you a good overview of how basic permissions and login checking happen.

Then we’re going to link our forum threads and posts to each user, and use those relationships to extract some statistics about our users to display how many posts and how long ago they started a thread, and how long ago they posted.



If at any point you run into any issues with your code, you can return to this starting point by following these steps:

* In the terminal run the following commands:
    * git clone https://github.com/Code-Institute-Org/we_are_social.git
    * cd we_are_social
    * git checkout reusable_blog

* Make sure you have a virtualenv setup in Pycharm. You’ll have to update the requirements.txt file by using git+https://github.com/brendanjgreene/reusable_blog_app.git instead of the link that’s already there. Once that’s done, you can go ahead and install the dependencies from ‘requirements.txt.’
* Run python manage.py migrate

## LEARNING OUTCOMES

Topics include:

* Extend the User model to add Threads and Posts to the user’s profile

* Collect information from multiple forms in one go

* Link in JavaScript support to enable tinymce WYSIWYG editing

* Enable or disable site functionality based on a user’s ownership of content and login status

* Use template tags to provide stats for users

_______

## ENABLE OR DISABLE SITE FUNCTIONALITY BASED ON A USER’S OWNERSHIP OF CONTENT AND LOGIN STATUS

Often you’ll want to restrict some of your site’s functionality based on the visitor’s login status, or even restrict them from editing content that does or does not belong to them. This is probably the most basic level of permissions checking that most social sites allow.

So how do you actually do that with Django?

### OWNERSHIP PERMISSIONS

Checking for ownership is simply a case of checking whether the current object’s user relationship is correct:
##
    {% if post.user == user or user.is_staff %}
    ...# show something"
    {% endif %}


Here we also check if the user is a staff member, as we want posts to be staff-moderated.

LOGIN STATUS

In addition to using the @login_required decorator on views that require an authenticated user, we can also use the is_authenticated() method, which is available anywhere you can access the user model.

When accessing in the templates, we need to omit the () section of the call, as seen here:


##

      {% if user.is_authenticated %}
        <p>
          <a href="{% url 'new_post' thread.id %}" class="btn btn-primary">New post</a>
        </p>
      {% endif %}
