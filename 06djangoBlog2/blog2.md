# INTRODUCTION – A NEW VIEW ON THINGS

In the last lesson, we put the basics of our blog together. That is, we created and tested a model and added some blog entries to our database.

In this lesson, we’ll add the views and templates needed for a non-admin user to read the blog posts. We’ll also use this as a chance to create a more flexible site architecture.

And what does that mean? It means:

* Creating static folders for content, such as CSS and JavaScript, that doesn’t change dynamically or often.

* Creating a templates folder at the project root level so that any apps added to a project can use templates that are common to the entire site.

* Creating a urls.py file for each app so that each app contains its unique calls and regular expressions within its own directory structure. The call to urls.py at the project level will then be more decoupled (a good thing) from the apps. This is very useful if you want to reuse the app in other projects.

This approach is known as delegation of responsibility. Each component part of a project is responsible for one thing and does it well, and has clear communication with the other constituent parts. In fact, this approach is at the heart of the MVC pattern.

##LEARNING OUTCOMES

By the end of this lesson,  you will be able to:

* Add views and templates needed for a non-admin user to read the blog

* Create a more flexible site architecture.

Topics include:

* Create a View

* Create the Templates

* Add static content

