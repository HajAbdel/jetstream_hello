# Hello Jetstream

Hello Jetstream

# Objectif :
- complet Authentification (login, register, reset password…)
- email verif
- user profil manage
- 2 fact Authentification (2FA)

# Resume:

### Jetstream uses Fortify behind the scenes to handle all authentication logic using Blade + Livewire or Vue + Inertia

| Jetstream                         | Fortify                               |
|-----------------------------------|---------------------------------------|
| 📱 User Interface (UI)            | 🧠 Authentication Logic (Backend)      |
| Blade + Livewire or Vue + Inertia | Handles login, register, reset, etc.  |
| Provides forms and views          | Provides routes and logic             |
| Easy to customize appearance      | Easy to customize behavior            |
| Includes features like 2FA, teams | Manages sessions, password validation |

### Think of it this way:
  - Fortify is like the engine of a car — it makes everything work.
  - Jetstream is the dashboard and body — it shows you the buttons, screens, and layout.

- Example: When a user signs up**
- Jetstream shows the registration form (UI).
- When the user submits, Fortify handles:
  - Validation  
  - Creating the user  
  - Hashing the password  
  - Logging them in

### Without Jetstream?
You can still use Fortify alone — but you must build your own UI (forms, views, etc.).

# Let's go 

## Add jetstream

```bash
composer require laravel/jetstream
```

## Install Jetstream

- with Livewire (blade)

```bash
php artisan jetstream:install livewire
```

- with  Inertia (vuejs)

```bash
php artisan jetstream:install inertia
```

- to manage team :

```bash
php artisan jetstream:install livewire --teams
```

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
