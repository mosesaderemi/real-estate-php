# Real Estate Management System

A PHP and MySQL web application for listing and managing properties. Visitors search properties by state and city and use a loan calculator. Registered users submit their own listings, and administrators manage every part of the data from an admin panel.

## Features

### Public site and users

- Home page with featured properties and property search by location
- Property grid and list views, state-based browsing and a property detail page with floor plans
- User registration, login and profile
- Users can submit, update and delete their own property listings
- Feedback form and contact form
- About and features pages
- Loan calculator (`calc.php`)

### Administration (`/admin`)

- Separate admin login and dashboard
- Add and edit properties
- Add and delete states and cities
- Manage users, agents and builders, and other administrators
- Review and delete contact messages and feedback
- Manage the About page content

## Tech Stack

| Area | Technology |
| --- | --- |
| Language | PHP 7.3 or later |
| Database | MySQL 5.7 or later (mysqli) |
| Frontend | HTML, CSS, JavaScript, Bootstrap-style admin theme, Font Awesome |

## Project Structure

```text
.
├── index.php, about.php, property.php, propertydetail.php, ...   Public pages
├── login.php, register.php, profile.php                          User accounts
├── submitproperty.php, submitpropertyupdate.php, ...             User listings
├── calc.php                                                      Loan calculator
├── config.php                                                    Database connection
├── Database/developers.sql                                       Schema and sample data
├── include, css, js, fonts, images
└── admin                                                         Admin panel and its own config.php
```

## Getting Started

### Prerequisites

- XAMPP, WAMP or any PHP and MySQL stack

### Installation

1. Clone the repository into your web root (for XAMPP, the `htdocs` folder):

   ```bash
   git clone https://github.com/mosesaderemi/real-estate-php.git
   ```

2. Create a database named `developers` and import `Database/developers.sql` with phpMyAdmin or the MySQL command line.
3. Check the connection settings in `config.php` and `admin/config.php`. The defaults are host `localhost`, user `root`, empty password and database `developers`.
4. Open `http://localhost/real-estate-php/` for the site and `http://localhost/real-estate-php/admin/` for the admin panel.

### Sample administrator

The SQL file creates one administrator: username `admin`, password `admin123`. Change it as soon as you sign in.

## Security Notes

This project is suitable for learning and local demonstration. Before any real deployment:

- Replace the string-concatenated SQL in the login and form pages with prepared statements, which closes SQL injection holes.
- Store passwords with `password_hash()` instead of plain text.
- Add validation and size limits to image uploads.

## Author

Aderemi Moses Timileyin
GitHub: [@mosesaderemi](https://github.com/mosesaderemi)
LinkedIn: [linkedin.com/in/mosesaderemi-6a70a5405](https://www.linkedin.com/in/mosesaderemi-6a70a5405)

## License

Released under the MIT License. See the `LICENSE` file for details.
