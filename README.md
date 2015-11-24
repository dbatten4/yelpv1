This week's project is a clone of [Yelp](http://www.yelp.co.uk). This project serves as an introduction to Rails, focusing especially on:

* Creating Rails applications
* The structure of Rails apps (MVC, the router, helpers)
* TDD in Rails, with RSpec & Capybara
* Associations
* Validations
* AJAX in Rails

## Specification

## Version 1 - MVP

For the initial version we want to duplicate the core functionality of Yelp - users should be presented with a list of restaurants which they can leave reviews for.

Remember to drive the addition of all features using feature tests, and unit tests when needed.

### V1 Specification

- Visitors can create new restaurants using a form, specifying a name and rating
- Restaurants can be edited and deleted
- Visitors can leave reviews for restaurants, providing a numerical score (1-5) and a comment about their experience
- The restaurants listings page should display all the reviews, along with the average rating of each restaurant
- [Validations](https://github.com/makersacademy/course/blob/master/walkthroughs/validations.md) should be in place for the restaurant and review forms - restaurants must be given a name and rating, reviews must be given a rating from 1-5 (comment is optional)


## Version 2 - User login

Although our initial version serves its purpose - it's limited in a few respects. First any visitor can freely delete or edit restaurants, leaving our site open to vandalism. Additionally, a user can leave multiple reviews for the same restaurant - making it easy for restaurant scores to be skewed.


### V2 Specification

* Users can register/login
* A user must be logged in to create restaurants
* Users can only edit/delete restaurants **which they've created**
* Users can only leave **one review per restaurant**
* Users can delete their own reviews
* Some indication should be given on the page (as part of the layout) whether the user is currently logged in, along with links to the available actions (i.e. Logout/Edit account is signed in, otherwise Sign In/Sign Up)
* The email address of the reviewer should be displayed as part of the review
* *Optional* - Users can't review a restaurant which they created

## Getting started

`git clone https://github.com/dbatten4/yelpv1.git` to clone the repository.

## Usage

run `gem install bundler` to install the bundle gem followed by 
`bundle`
to imstall the gems and dependencies.
To start the server, run 
`rails s`
and navigate to http://localhost:3000/

## Running tests

run 
`rspec`
from the command line to the run the Rspec tests.
