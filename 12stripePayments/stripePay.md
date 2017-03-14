#INTRODUCTION

At some point in your career as a web developer, you’ll be asked to setup some form of payment system for your client’s website. One of the most popular methods currently used for taking payments online today is Stripe.

Stripe offers safe and secure payments without the need for special security methods on the developer’s part, or the website hosting platform to ensure that the customer’s details are safe.

To that end, we’re now going to look at how you can take single one-off payments using Stripe. In our case we will require a user to make a payment when registering on the site. In a later lesson, you’ll be ready to add in more complex payments like subscriptions.
In the process, we’ll also get our first chance to reuse our custom User model that we made in our previous unit dealing with authentication!



##LEARNING OUTCOMES

Topics include:

* Installing and configuring Stripe
* Taking credit card details and generating a stripe token
* Taking a single payment when a new user registers
* Altering your User model to record the unique stripe token
