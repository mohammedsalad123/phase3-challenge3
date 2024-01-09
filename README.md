# phase3-challenge2
Restaurant Review Domain - SQLAlchemy Project
 ## Overview
This project is a Python application that models a restaurant review domain using SQLAlchemy, a powerful Object-Relational Mapping (ORM) library. The application defines three models: Restaurant, Review, and Customer. These models are interconnected to represent a many-to-many relationship between Restaurant and Customer through the Review model.

## Project Structure
The project follows a structured layout with separate files for each model:

models/

restaurant.py - Contains the Restaurant model
customer.py - Contains the Customer model
review.py - Contains the Review model
migrations/ - Folder to store database migration files

seeds.py - File for creating sample instances to test models and relationships

app.py - Main file to execute the application and test the defined methods

Setup
Clone the repository:


git clone https://github.com/your-username/restaurant-review-sqlalchemy.git
 
 ## Install dependencies:
pip install -r requirements.txt

## Run migrations to set up the database:
python manage.py db init
python manage.py db migrate
python manage.py db upgrade

## Seed the database with sample data:
python seeds.py
 
 ## Usage
The application provides various methods to interact with the models and relationships. Test these methods in the app.py file.

## Object Relationship Methods
Review
Review.customer() - Returns the Customer instance for this review
Review.restaurant() - Returns the Restaurant instance for this review

Restaurant
Restaurant.reviews() - Returns all reviews for the restaurant
Restaurant.customers() - Returns all customers who reviewed the restaurant

Customer
Customer.reviews() - Returns all reviews left by the customer
Customer.restaurants() - Returns all restaurants reviewed by the customer
Aggregate and Relationship Methods
Customer

Customer.full_name() - Returns the full name of the customer
Customer.favorite_restaurant() - Returns the restaurant with the highest star rating
Customer.add_review(restaurant, rating) - Adds a new review for the restaurant
Customer.delete_reviews(restaurant) - Deletes all reviews for the given restaurant
Review

Review.full_review() - Returns a formatted string with review details
Restaurant

Restaurant.fanciest() - Returns the restaurant with the highest price
Restaurant.all_reviews() - Returns a list of strings with all reviews for the restaurant
 
## Author
mohammed salad
# phase-3-challenge2