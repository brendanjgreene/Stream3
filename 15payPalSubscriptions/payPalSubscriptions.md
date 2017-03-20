#INTRODUCTION

In the last unit, we looked at taking single one-off payments using PayPal’s API.

In this unit, we’re going to build on what we’ve learned to start allowing our registered users to subscribe to a number of online magazines.


## If at any point you run into any issues with your code, you can return to this starting point by following these steps:

1. In the terminal run the following commands:
* git clone https://github.com/Code-Institute-Org/we_are_social.git
* cd we_are_social
* git checkout paypal_basic_payments

2. Make sure you have a virtualenv setup in Pycharm and then install the dependencies from ‘requirements.txt.’
3. Run python manage.py migrate

#LEARNING OUTCOMES

## Topics include:

* Setup Django for subscription handling
* Setup products that require subscriptions
* Use Django ORM to connect users to their purchases
* Test PayPal notification message handling