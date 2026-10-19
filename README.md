
# RottenPotatoes Movies

A Ruby on Rails application for managing a movie collection.

## Live Application

**Deployed URL:** https://rottenpotatoes-bhagavatiraj.onrender.com

## Features

- Create, view, edit, and delete movies.
- Display movies in a table.
- Sort movies by title, rating, and release date in ascending or descending order.
- Highlight the currently sorted column and display a sort indicator.
- Display the total number of movies.
- Seed the database with 3 sample movies.
- Use handwritten CSS for page layout, tables, forms, and buttons.

## Technology Stack

- Ruby 3.4.10
- Ruby on Rails 8.1.3.1
- SQLite for local development
- PostgreSQL for production
- Render for deployment

## Run Locally

Install the required Ruby version and dependencies, then run:

```bash
bundle install
bin/rails db:prepare
bin/rails db:seed
bin/rails server
```

Open http://localhost:3000 in your browser.

The application redirects the root URL to the movies dashboard.

## Deployment

The application is configured for deployment on Render.

The `bin/render-build.sh` script installs dependencies, precompiles assets, runs database migrations, and seeds the database.

Configure the production database using `DATABASE_URL` and provide `RAILS_MASTER_KEY` through Render's environment settings. Do not commit secret keys or credentials.

## Database Seeds

The seed file is `db/seeds.rb`. It creates five sample movies and uses `find_or_create_by!` to avoid inserting duplicate titles when the seed script is run again.
