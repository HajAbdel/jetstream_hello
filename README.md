# 👋 Hello Jetstream

Welcome to Jetstream!

## 🎯 Objective

Jetstream provides a complete authentication system with:

- Full authentication (login, register, reset password…)
- Email verification
- User profile management
- Two-Factor Authentication (2FA)

---

## 📝 Summary

- **Jetstream** uses **Fortify** behind the scenes to handle all authentication.
- Jetstream automatically registers and configures Fortify and provides the user interface (UI).
- Jetstream uses either **Livewire** or **Inertia.js** for rendering.

---

## 🔍 Comparison: Jetstream vs Fortify

| Jetstream                          | Fortify                                |
|-----------------------------------|----------------------------------------|
| 📱 User Interface (UI)            | 🧠 Authentication Logic (Backend)       |
| Blade + Livewire or Vue + Inertia | Handles login, register, reset, etc.   |
| Provides forms and views          | Provides routes and logic              |
| Easy to customize appearance      | Easy to customize behavior             |
| Includes features like 2FA, teams | Manages sessions, password validation  |

---

### 💡 Think of it this way:

- **Fortify** is like the **engine** of a car — it makes everything work.
- **Jetstream** is the **dashboard and body** — it shows you the buttons, screens, and layout.

---

### 📌 Example: When a user signs up

- Jetstream shows the registration form (**UI**).
- When the user submits the form, **Fortify** handles:
  - Validation  
  - Creating the user  
  - Hashing the password  
  - Logging them in

---

### ❓ Without Jetstream?

You can still use **Fortify alone** — but you have to build your own UI (forms, views, etc.).

---

# 1. Create new projetct Laravel

```bash
composer create-project laravel/laravel example-app
```

# 2. change to project folder

```bash
cd example-app
```

# 3. install Jetstream in projet

## Add jetstream lib

- add jetstream to project in composer.json & download it in vendor/ folder

```bash
composer require laravel/jetstream
```

## Install Jetstream

- choose stack : Livewire or Inertia ?
  - with Livewire (blade)

```bash
php artisan jetstream:install livewire
```

  - or with  Inertia (vuejs)

```bash
php artisan jetstream:install inertia
```

> ⚠️ This choice is irreversible once installed (unless you remove and reinstall Jetstream).

> **Options** :
- --dark    : to add dark mode
- --ssr     : for SSR support
- --teams   : to add team support 

# 4. Finalizing Installation 

## install all packages (dependencies) that project needs to run:
  - Reads package.json file (list all required packages)
  - Downloads packages from the npm registry (online)
  - Adds them to a folder called node_modules/ in project
  - Creates or updates the package-lock.json file (records exact versions installed).

```bash
npm install
```

- Remember:
  - package.json      :	Lists project's dependencies and config
  - package-lock.json	: Locks the exact versions installed (for consistency)
  - node_modules/	    : Contains all the installed packages

## start project in dev mode (live preview, auto reload, etc.)

```bash
npm run dev
```

- this will run custom script defined in package.json file
- It’s equivalent to running : vite, webpack, Laravel Mix... etc. behind the scenes
- this will :
  - start a local dev server (like Vite, Webpack, Laravel Mix, etc.).
  - Watches your files (JS, CSS, etc.) for changes.
  - Rebuilds and reloads automatically when files change (Hot Reload / HMR).
  - Shows build errors in the terminal or browser.


 ## Or start project in prod mode 

```bash
npm run build
```

- It runs the script called build from your package.json file (like running "vite build")
- This will:
  - bundles everything into a small number of files : compile and optimize your code for production (for real users on the live website)
  - makes files (JS & CSS) smaller and faster
  - removes dev-only code (console logs, debugging tools)
  - Prepares files in a special folder like /dist or /build.

# 5. migrate

- Remember :
  - A migration in Laravel is like a version-controlled script that defines a change in the DB schema (like creating or modifying tables/columns).
  - migration might : Create table; Add column; Delete a table, etc.

```bash
php artisan migrate
```

- Process :
  - 1 Laravel looks in the database/migrations/ folder
  - 2 Finds any migrations that haven't been run yet
  - 3 Applies them to your database (e.g., creates tables)
  - 4 Tracks them in a table called migrations to avoid running them again


- run all pending DB migrations in project.
- it will :
- 

# Results:

- Laravel does the following:
  - Installs Jetstream and Fortify
  - Registers Fortify routes in App\Providers\FortifyServiceProvider
  - Adds logic files in App\Actions\Fortify for things like user creation and password updates

- Example files generated:
  - app/Actions/Fortify/CreateNewUser.php
  - app/Actions/Fortify/UpdateUserPassword.php
  - app/Actions/Fortify/ResetUserPassword.php


# Customize Validation Messages

xxxx

### Livewire

resources/views/components/application-logo.blade.php
resources/views/components/application-mark.blade.php
resources/views/components/authentication-card-logo.blade.php

### Inertia

resources/js/Components/ApplicationLogo.vue
resources/js/Components/ApplicationMark.vue
resources/js/Components/AuthenticationCardLogo.vue

then 

```bash
npm run build
```

# config session in .env file :
Set this in .env:

SESSION_DRIVER=database
SESSION_LIFETIME=1
SESSION_EXPIRE_ON_CLOSE=false

---
https://jetstream.laravel.com/introduction.html
