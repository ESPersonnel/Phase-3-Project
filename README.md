# Phase III Project: Fantasy Novel Store

## Overview

This project is a web application that allows users to browse fantasy novels and sort them how they want. The user can also add novels to their cart and checkout.
The application is built using the sinatra framework and uses a rakefile to manage the database.

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
 

