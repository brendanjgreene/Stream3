#INTRODUCTION

You’ve probably noticed throughout the last four lessons that all blog posts were added from the admin screen. This isn’t the best way to do things for two reasons; security and usability.

Security, because once someone has access to the admin page, they may inadvertently (or deliberately) modify other key data areas registered with the admin module. And usability, because a blogger really shouldn’t have to go through the back door to add a new post.

Also, a blog post should display any images required to illustrate what might be the post’s main point.

In this lesson, we’ll add a post submission form to allow users to add images to a post, and to create a new blog post form.

#LEARNING OUTCOMES

Topics include:

* Adding Images to a Post

* Create a New Blog Post Form

# ADDING IMAGES TO A POST

We’ll start with the images. As in the last two lessons, we’ll first modify our Post model.

To do this:

* Add a new imageField to the Post model.
* Install Pillow to handle image storage and retrieval.
* Migrate.
* Add MEDIA_ROOT value to settings.py.
* Add a custom url pattern to the project level urls.py file.
* Add a reference to the Post model image attribute in an <img> tag inside the postdetail template to view.
  
#CREATE A BLOG POST FORM

##Now that we have the ability to upload an image, we’re going to create a blog post creation form that users can access without having to log into the admin screen. We’ll take advantage of Django’s built-in ModelForm functionality to help us out on this task. More Django goodness!

To do this:

* Create a forms.py file to add selected model fields to the form.
* Create new views to render the form.
* Add a new url pattern to our project level urls.py.
* Create a new template for submitting new posts.
* Add the 3rd party django-forms-bootstrap library to dress up the form display.
* Make the post content in our postdetail template editable.
* Enable saving of new posts.
* Enable editing of existing posts.