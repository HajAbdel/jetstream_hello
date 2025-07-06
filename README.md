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

### 🔍 Comparison: Jetstream vs Fortify

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

# Let's go 

## add jetstream

```bash
composer require laravel/jetstream
```

## OR Install Jetstream

- with Livewire (blade)

```bash
php artisan jetstream:install livewire
composer require laravel/jetstream
```

- with  Inertia (vuejs)

```bash
php artisan jetstream:install inertia
```

- to manage team :

```bash
php artisan jetstream:install livewire --teams
```

- Laravel does the following:
  - Installs Jetstream and Fortify
  - Registers Fortify routes in App\Providers\FortifyServiceProvider
  - Adds logic files in App\Actions\Fortify for things like user creation and password updates

- Example files generated:
  - app/Actions/Fortify/CreateNewUser.php
  - app/Actions/Fortify/UpdateUserPassword.php
  - app/Actions/Fortify/ResetUserPassword.php

## Compile assets (JS/CSS)

```bash
npm install && npm run dev
```

- or (for production)

```bash
npm run build
```

## Migrate

- create tables (users, sessions)

```bash
php artisan migrate
```

## run serv

```bash
php artisan serve
```

## Customize Validation Messages


