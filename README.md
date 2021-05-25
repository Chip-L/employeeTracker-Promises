# Employee Tracker (with promises!)

## Description

The goal of this was to make a CLI for a CMS with the backend being a MySQL database. This was the second try a this and I added an extra requirement of all queries needing to be promises. The [original MVP](https://github.com/Chip-L/employeeTracker) was done using only callbacks. I have also started to do this with only [Async/Await commands](https://github.com/Chip-L/employeeTracker-async-await).

Completed site's code: https://github.com/Chip-L/employeeTracker-Promises

Video of working application (from Promises version): https://drive.google.com/file/d/1SFRmVjUKDqolDMFUIELIeOMXwMXyNl_N/view

## Table of Contents

- [User Story](#user-story)
- [Acceptance Criteria](#acceptance-criteria)
- [Usage](#usage)
- [Technologies](#technologies)

## User Story

AS A business owner
I WANT to be able to view and manage the departments, roles, and employees in my company
SO THAT I can organize and plan my business

## Acceptance Criteria

Here are the critical requirements necessary to develop a this app:

Design the following database schema containing three tables:

![Database Schema](misc/Assets/schema.png)

- **department**:

  - **id** - INT PRIMARY KEY
  - **name** - VARCHAR(30) to hold department name

- **role**:

  - **id** - INT PRIMARY KEY
  - **title** - VARCHAR(30) to hold role title
  - **salary** - DECIMAL to hold role salary
  - **department_id** - INT to hold reference to department role belongs to

- **employee**:

  - **id** - INT PRIMARY KEY
  - **first_name** - VARCHAR(30) to hold employee first name
  - **last_name** - VARCHAR(30) to hold employee last name
  - **role_id** - INT to hold reference to role employee has
  - **manager_id** - INT to hold reference to another employee that manages the employee being Created. This field may be null if the employee has no manager

Build a command-line application that at a minimum allows the user to:

- Add departments, roles, employees

- View departments, roles, employees

- Update employee roles

Bonus points if you're able to:

- Update employee managers

- View employees by manager

- Delete departments, roles, and employees

- View the total utilized budget of a department -- ie the combined salaries of all employees in that department

## Usage

Type 'npm start' to launch the application.

## Technologies

- [NodeJS](https://nodejs.org/en/)
- [MySQL](https://www.npmjs.com/package/mysql)
- [Inquirer](https://www.npmjs.com/package/inquirer)
- [Console.Table](https://www.npmjs.com/package/console.table)
- [Dotenv](https://www.npmjs.com/package/dotenv)
