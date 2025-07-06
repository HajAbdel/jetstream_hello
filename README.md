# jetstream_hello
Hello Jetstream

# Objectif :
- complet Authentification (login, register, reset password…)
- email verif
- user profil manage
- 2 fact Authentification (2FA)

## add jetstream

```bash
composer require laravel/jetstream
```

## Install Jetstream with Livewire (blade) or Inertia (vuejs)

```bash
php artisan jetstream:install livewire
```

to manage team :

```bash
php artisan jetstream:install livewire --teams
```

```bash
php artisan jetstream:install inertia
```

## Compile assets (JS/CSS)

```bash
npm install && npm run dev
```

or (for production)

```bash
npm run build
```

## create tables (users, sessions)

```bash
php artisan migrate
```

## run serv

```bash
php artisan serve
```
