# Filament 4 Starter Kit – Laravel 12

A modern, production-ready **admin panel starter kit** built with **Laravel 12** and **Filament 4**.

This project provides a clean, secure foundation for building admin applications with:

- Beautiful Filament v4 admin panel
- User management (full CRUD)
- Role & Permission system (via Filament Shield + Spatie Permissions)
- 2FA / Multi-Factor Authentication (MFA) – compatible with Google Authenticator, Authy, etc.
- User profile editing with avatar, password change, 2FA setup, browser sessions, and more
- Ready for rapid customization and scaling

## Features

- Laravel 12 & PHP 8.2+
- Filament 4 – TALL stack admin panel
- Full **User CRUD** resource
- **Filament Shield** – Role & permission management
- Native **Multi-Factor Authentication (2FA/MFA)**
- **Edit Profile** system (using joaopaulolndev/filament-edit-profile)
- Avatar upload support
- Dark mode & responsive design
- Optimized Filament caching
- Easy to extend with additional resources, pages, and widgets

## Requirements

- PHP ≥ 8.2
- Composer
- Node.js & npm (for frontend assets)
- Database (MySQL, PostgreSQL, SQLite, etc.)

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   cd YOUR-REPOSITORY
Install PHP dependencies

composer install
Install frontend dependencies

npm install
npm run dev          # for development
# or
npm run build        # for production
Copy environment file

cp .env.example .env
Generate application key

php artisan key:generate
Configure your database in .env

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_username
DB_PASSWORD=your_password
Run migrations and seed initial data

php artisan migrate --seed
This command will:

Create users, roles, permissions tables
Set up columns needed for 2FA and avatars
Create a default super admin user
Publish Filament Shield configuration (recommended)

php artisan vendor:publish --tag=shield-config
Generate Shield permissions (run this after adding new resources)

php artisan shield:generate --all
Create storage symlink (for avatar uploads)

php artisan storage:link
Start the development server

php artisan serve
Open in your browser:
http://127.0.0.1:8000/admin

Default login credentials:
Email: admin@admin.com
Password: password

Important: Change the password immediately after first login!
