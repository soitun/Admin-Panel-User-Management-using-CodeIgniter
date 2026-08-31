# Admin Panel — User Management using CodeIgniter

> [!WARNING]
> ## Legacy repository — no active maintenance
> This CodeIgniter project is retained as a reference implementation and is **not actively maintained**. Do not use it as the starting point for new production work. New features, security improvements, and ongoing maintenance are focused on the modern rewrite:
>
> **[CIAS Admin Panel — React + NestJS](https://github.com/kishor10d/Admin-Panel-User-Management-using-React-NodeJS)**

A legacy, role-based administration panel built with CodeIgniter, PHP, MySQL, AdminLTE, Bootstrap, and jQuery. It demonstrates the common building blocks of an administration area: login, user management, roles and access rights, password recovery, and login history.

## Legacy stack

| Area | Technology |
| --- | --- |
| Framework | CodeIgniter 3.1.x |
| Language | PHP 5.6+ legacy codebase |
| Database | MySQL with MySQLi |
| UI | AdminLTE 2, Bootstrap 3, jQuery |
| Dependencies | Composer autoloader and bundled front-end assets |

## Features

- Session-based login and logout.
- User creation, editing, soft deletion, and profile updates.
- Role management with a configurable access matrix for application modules.
- Password change, forgot-password flow, and reset-password email template.
- Per-user login history with filtering and pagination.
- Example permission-controlled Task and Booking modules.
- AdminLTE-based dashboard and administration layout.

## Modern rewrite

The maintained successor is a TypeScript monorepo built for new projects and modern deployment practices.

| Legacy repository | Maintained rewrite |
| --- | --- |
| CodeIgniter and PHP | React, NestJS, and TypeScript |
| SQL import | TypeORM migrations |
| Session-based authentication | Secure cookie sessions with rotated refresh tokens |
| Legacy role matrix | Server-enforced RBAC permissions |
| AdminLTE 2 | AdminLTE 4 |

Start new work with **[CIAS Admin Panel — React + NestJS](https://github.com/kishor10d/Admin-Panel-User-Management-using-React-NodeJS)**.

## Running the legacy application locally

### Requirements

- PHP compatible with this legacy CodeIgniter 3.1.x codebase.
- MySQL or MariaDB.
- Apache with PHP and `mod_rewrite` when using clean URLs.
- Composer.

### 1. Place the project in your web root

For example:

```text
XAMPP: C:\xampp\htdocs\cias
WAMP: C:\wamp\www\cias
```

### 2. Install the Composer autoloader

From the repository root:

```bash
composer install
```

### 3. Create and configure the database

1. Create an empty MySQL database, for example `cias`.
2. Import [db/cias.sql](db/cias.sql).
3. Set the database host, database name, username, and password in `application/config/database.php`.
4. Update `base_url` in `application/config/config.php` to match your local URL, for example `http://localhost/cias/`.

The SQL file includes sample data intended only for local demonstration. Review it and change all sample accounts and passwords before exposing an installation to any network.

### 4. Open the application

Visit the configured base URL in your browser, for example:

```text
http://localhost/cias/
```

If application routes return a 404 error, enable Apache `mod_rewrite` and ensure the web server permits the project’s URL rewrite configuration.

## Security notice

This repository contains legacy framework code and application patterns. It does **not** receive regular security patches, dependency upgrades, or production support.

If you must run it temporarily:

- Use it only in a controlled environment.
- Set `ENVIRONMENT` to `production` in `index.php` outside local development.
- Change the sample administrator credentials and application secrets.
- Enable HTTPS, restrict database access, and protect server configuration files.
- Review and enable CSRF protection before exposing write operations.
- Plan a migration to the maintained React + NestJS project.

## Demo videos

- [CodeIgniter Admin Panel Demo](https://youtu.be/RFRXUd8LHUM)
- [Legacy setup walkthrough](https://youtu.be/tU1PbcRj7ww)

[![CodeIgniter Admin Panel Demo](https://img.youtube.com/vi/RFRXUd8LHUM/0.jpg)](https://www.youtube.com/watch?v=RFRXUd8LHUM)

## License

See [LICENSE](LICENSE) for licensing information.
