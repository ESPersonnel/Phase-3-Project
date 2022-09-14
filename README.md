# Phase III Project: Fantasy Novel Store

## Overview

This project is a web application that allows users to browse fantasy novels and sort them how they want. The user can also add novels to their cart and checkout.
The application is built using the sinatra framework and uses a rakefile to manage the database.

> Note:
> At the time of submission the project is not yet done but I am constantly working on it (the fundamentals are done, it just needs to work well).
> Comments from the TM are welcome.


## Technologies Used

### Backend

    Ruby
    Sinatra
    Active Record

### Frontend

    React
    Javascript
    CSS

## Installation

To install this application, clone the backend and frontend repositories.

### Backend

1. Clone the backend repository from [here](https://github.com/ESPersonnel/Fantasy-Book-Store-Backend)

2. Run `bundle install` to install the required gems.

3. Run `bundle exec rake db:migrate` to create the database.

4. Run `bundle exec rake db:seed` to seed the database.

5. Finally run `bundle exec rake server` to run the backend.

### Frontend

1. Clone the frontend repository from [here](https://github.com/ESPersonnel/Fantasy-Book-Store-Frontend)

2. Run `npm install` to install the required packages.

3. Run `npm start`.


## ERD Relationship Diagram

    Key:
    One to Many  1 ----< ∞
    Many to Many ∞ ----< ∞


    Readers --------------< Reviews >----------- Books >-------------- Author
    :reader_name           :reader_id           :author_id            :series_title
    :email                 :book_id             :title                :author_name
    :birthday              :title               :genre                :series
    :phone_no              :content             :publication_date
 

### Readers
has_many :reviews
has_many :books, through: :reviews

### Reviews
belongs_to :reader
belongs_to :book

### Books
has_many :reviews
has_many :readers, through: :reviews
belongs_to :author

### Authors
has_many :books

## Current Progress

### Backend

The backend is currently complete. It has all the required routes and controllers. The database is seeded with data.

Any other informational data will be added to this section as the project progresses.

### Frontend

The frontend is coming along but is not complete. The application can currently do the following:

- Displays all the books in the Backend database.
- Displays all the authors in the Backend database.
- Displays all the reviews in the Backend database.

Functionality to be added:

- Functionality to add, edit and delete books, authors and reviews.
