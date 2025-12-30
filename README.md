# Internal Notes Module

An internal notes module built using Symfony 4.4 (LTS) as part of a recruitment task.

## Tech Stack
- PHP 7.x
- Symfony 4.4 (LTS)
- Doctrine ORM
- Twig
- MySQL

## Features
- List all notes
- Create a new note
- Edit a note
- Delete a note

## Assumptions
- UI/UX is not a priority for this task

## What Confused Me
- Nothing significant; the requirements were clear and straightforward

## What I Would Improve in a Production System
- Add validation constraints
- Add pagination for large datasets
- Add automated tests
- Improve UI/UX

## Setup Instructions
1. Clone the repository
2. Run `composer install`
3. Configure database connection in `.env.local`
4. Create database: php bin/console doctrine:database:create
5. Run migrations: php bin/console doctrine:migrations:migrate
6. Start the server: php bin/console server:run