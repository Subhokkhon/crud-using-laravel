Project Title: Laravel CRUD Application
📘 Project Overview

This project is a CRUD (Create, Read, Update, Delete) web application developed using the Laravel PHP framework. It demonstrates how to build a full-stack data management system with clean architecture, MVC (Model-View-Controller) design pattern, and RESTful routes.

The purpose of this project is to perform basic database operations — adding, viewing, updating, and deleting records — through an interactive web interface. It’s a foundational project that shows your understanding of Laravel’s core concepts such as Eloquent ORM, routing, controllers, blade templates, and validation.

⚙️ Tech Stack

Backend Framework: Laravel (PHP 10+)

Frontend: Blade Template Engine, Bootstrap 5, HTML, CSS, JavaScript

Database: MySQL (via Laravel’s Eloquent ORM)

Server: Localhost (XAMPP / Laravel Valet)

Version Control: Git & GitHub


🧠 Key Features
1. Create

Users can fill out a form to add new records (e.g., employees, products, students, etc.).

Laravel’s form validation ensures required fields are filled correctly before saving.

On successful creation, a success message is displayed.

2. Read

The homepage lists all records from the database in a responsive table format.

Includes pagination and search functionality.

Each record shows details like ID, Name, Email, Created Date, etc.

3. Update

Users can edit existing records by clicking an Edit button.

The form is pre-filled with the existing data for user convenience.

Changes are validated before being updated in the database.

4. Delete

Each record includes a Delete button.

Confirmation prompt before deletion to prevent accidental removal.

After deletion, the list auto-refreshes with a success message.

🧩 Workflow

Setup Laravel Project

composer create-project laravel/laravel laravel-crud-app


Configure Database

Update .env file:

DB_DATABASE=crud_app
DB_USERNAME=root
DB_PASSWORD=


Run migrations:

php artisan migrate


Create Model, Controller, and Migration

php artisan make:model Student -mcr


Adds:

Model: Student.php

Controller: StudentController.php

Migration for students table

Define Routes in web.php

Route::resource('students', StudentController::class);


Build CRUD Methods in Controller

index() → Show all students

create() → Show form

store() → Save new record

edit() → Edit form

update() → Save updates

destroy() → Delete record

Design Views Using Blade

index.blade.php — list all records

create.blade.php — add form

edit.blade.php — edit form

Use Bootstrap for styling and layout

Run Application

php artisan serve


Access the app at: http://localhost:8000/students

💡 Sample Use Case

Example: Student Management System

Add new students with name, email, course, and phone number.

View all students in a table.

Edit or delete student details dynamically.

🔒 Validation and Error Handling

Laravel’s built-in validation handles form input rules:

$request->validate([
    'name' => 'required|string|max:255',
    'email' => 'required|email|unique:students',
    'course' => 'required|string',
]);


Custom error messages displayed via Blade.


🏁 Project Outcome

By completing this project, I demonstrate my ability to:

Work with Laravel MVC structure

Use Eloquent ORM for database operations

Build RESTful routes and controllers

Implement form validation, error handling, and user feedback

Design a responsive UI using Blade + Bootstrap
