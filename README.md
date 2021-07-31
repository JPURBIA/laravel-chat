# Laravel based Chat Application
## Table of contents

* [Installations](#installation)
* [Additional Setup](#additional-setup)
* [How to run](#how-to-run)
* [Contributors](#contributors)
## Installation

After cloning the repo in your system, please follow the steps below:

``` bash
# Create .env file
cp .env_sample .env

# Create a MySQL DB for this system
# Set DB fields in .env file accordingly
#   e.g.
#   DB_HOST=127.0.0.1
#   DB_PORT=3306
#   DB_DATABASE=[DATABASE_NAME]
#   DB_USERNAME=[DATABASE_USER_NAME]
#   DB_PASSWORD=[DATABASE_PASSWORD]

# Install PHP dependencies
$ composer install

# Generate an application key of Laravel
$ php artisan key:generate

# Seed DB tables and data
$ php artisan migrate:fresh

# Install JS dependencies
$ npm ci
```
---
## Additional setup
### Setup Pusher

* If you don’t have one already, create a free Pusher account at [Pusher Signup](https://pusher.com/signup) then login to your dashboard and create an app.

* Add Pusher configuration to your `.env` file.
```
    PUSHER_APP_ID=your-pusher-app-id
    PUSHER_APP_KEY=your-pusher-key
    PUSHER_APP_SECRET=your-pusher-secret
    PUSHER_APP_CLUSTER=mt1
```
## How to run

Follow these steps to start your application:
``` bash
# Start the queue
$php artisan queue:work
 
# Watch JS changes to auto-build
$ npm run watch

# OR, build just once by
# $ npm run dev

# Start local server
$ php artisan serve

# Open your browser and access http://localhost:8000/
```

## Contributors

* Jonty Purbia
