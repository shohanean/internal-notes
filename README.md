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
- Authentication already exists in the system
- A User entity is available (used for the mid-task requirement)
- UI/UX is not a priority for this task

## Mid-Task Change Handling
After receiving the requirement to make notes user-specific:
- A relationship between Note and User was added
- Notes are associated with the currently authenticated user
- Only the owner of a note can view, edit, or delete it

## Note on Authentication
The project assumes an existing authentication system as per the task instruction.
In the local setup, no authentication is configured, therefore `$this->getUser()` returns null.
As a result, existing and newly created notes may have a null user locally.
In a real environment with authentication enabled, notes would be automatically associated with the logged-in user.

## What Confused Me
- Nothing significant; the requirements were clear and straightforward

## What I Would Improve in a Production System
- Use Symfony Voters for authorization
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