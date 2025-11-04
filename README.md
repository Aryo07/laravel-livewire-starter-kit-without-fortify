# Laravel 12 + Livewire 3 Starter Kit

<p align="center">
<img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo">
</p>

<p align="center">
<a href="https://laravel.com"><img src="https://img.shields.io/badge/Laravel-12-FF2D20?style=flat&logo=laravel" alt="Laravel 12"></a>
<a href="https://livewire.laravel.com"><img src="https://img.shields.io/badge/Livewire-3-4E56A6?style=flat&logo=livewire" alt="Livewire 3"></a>
<a href="https://tailwindcss.com"><img src="https://img.shields.io/badge/Tailwind-4-38B2AC?style=flat&logo=tailwind-css" alt="Tailwind CSS 4"></a>
<a href="https://pestphp.com"><img src="https://img.shields.io/badge/Pest-4-FF2D20?style=flat" alt="Pest PHP 4"></a>
<a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License"></a>
</p>

## 📋 Tentang Project

Starter kit modern untuk Laravel 12 dengan Livewire 3, **tanpa menggunakan Laravel Fortify**. Project ini menyediakan implementasi autentikasi custom menggunakan Livewire components murni, dilengkapi dengan UI yang indah menggunakan Livewire Flux dan Tailwind CSS 4.

### ✨ Fitur Utama

- ✅ **Laravel 12** - Framework PHP terbaru
- ⚡ **Livewire 3** - Full-page components tanpa reload
- 🎨 **Livewire Flux** - UI component library yang elegan
- 🎯 **Livewire Volt** - Single-file Livewire components
- 💨 **Tailwind CSS 4** - Utility-first CSS framework
- 🔐 **Custom Authentication** - Tanpa Fortify, implementasi murni Livewire
- ✉️ **Email Verification** - Verifikasi email terintegrasi
- 🔑 **Password Reset** - Reset password via email
- 👤 **User Profile Management** - Manajemen profil pengguna
- 🔒 **Password Change** - Ubah password
- 🎨 **Appearance Settings** - Pengaturan tampilan
- 🧪 **Pest PHP 4** - Testing framework modern
- 🚀 **Vite** - Fast build tool

## 🔐 Fitur Autentikasi

Project ini menyediakan sistem autentikasi lengkap tanpa Fortify:

- **Login** - Halaman login dengan remember me
- **Register** - Pendaftaran pengguna baru
- **Forgot Password** - Lupa password dengan email reset
- **Reset Password** - Reset password via token
- **Email Verification** - Verifikasi email pengguna
- **Confirm Password** - Konfirmasi password untuk aksi sensitif
- **Logout** - Keluar dari sistem

## 📦 Persyaratan Sistem

- PHP >= 8.2
- Composer
- Node.js >= 18.x
- NPM atau Yarn
- Database (MySQL, PostgreSQL, SQLite, atau SQL Server)

## 🚀 Instalasi

### 1. Clone Repository

```bash
git clone <repository-url>
cd laravel12-livewire
```

### 2. Install Dependencies

```bash
# Install PHP dependencies
composer install

# Install JavaScript dependencies
npm install
```

### 3. Konfigurasi Environment

```bash
# Copy file .env
cp .env.example .env

# Generate application key
php artisan key:generate
```

### 4. Konfigurasi Database

Edit file `.env` dan sesuaikan konfigurasi database:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel12_livewire
DB_USERNAME=root
DB_PASSWORD=
```

### 5. Migrasi Database

```bash
php artisan migrate
```

### 6. Konfigurasi Email (Opsional)

Untuk fitur email verification dan password reset, konfigurasi email di `.env`:

```env
MAIL_MAILER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=your_username
MAIL_PASSWORD=your_password
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS="noreply@example.com"
MAIL_FROM_NAME="${APP_NAME}"
```

### 7. Build Assets

```bash
# Development
npm run dev

# Production
npm run build
```

### 8. Jalankan Server

```bash
php artisan serve
```

Aplikasi akan berjalan di `http://localhost:8000`

## 📁 Struktur Project

```
├── app/
│   ├── Http/
│   │   └── Controllers/
│   │       └── Auth/
│   │           └── VerifyEmailController.php
│   ├── Livewire/
│   │   ├── Actions/           # Action classes untuk Livewire
│   │   ├── Auth/              # Komponen autentikasi
│   │   │   ├── Login.php
│   │   │   ├── Register.php
│   │   │   ├── ForgotPassword.php
│   │   │   ├── ResetPassword.php
│   │   │   ├── VerifyEmail.php
│   │   │   └── ConfirmPassword.php
│   │   └── Settings/          # Komponen pengaturan
│   │       ├── Profile.php
│   │       ├── Password.php
│   │       └── Appearance.php
│   └── Models/
│       └── User.php
├── resources/
│   ├── views/
│   │   ├── livewire/         # View Livewire components
│   │   ├── components/       # Blade components
│   │   ├── flux/             # Flux UI components
│   │   ├── dashboard.blade.php
│   │   └── welcome.blade.php
│   ├── css/
│   │   └── app.css
│   └── js/
│       └── app.js
├── routes/
│   ├── web.php               # Web routes
│   ├── auth.php              # Authentication routes
│   └── console.php
├── tests/
│   ├── Feature/
│   │   ├── Auth/             # Auth tests
│   │   ├── Settings/         # Settings tests
│   │   └── DashboardTest.php
│   └── Unit/
└── database/
    ├── migrations/
    └── seeders/
```

## 🧪 Testing

Project ini menggunakan Pest PHP untuk testing:

```bash
# Jalankan semua tests
php artisan test

# Jalankan tests dengan coverage
php artisan test --coverage

# Jalankan specific test file
php artisan test tests/Feature/Auth/LoginTest.php

# Jalankan dengan parallel
php artisan test --parallel
```

## 📚 Dokumentasi Tambahan

- [Laravel Documentation](https://laravel.com/docs/12.x)
- [Livewire Documentation](https://livewire.laravel.com/docs)
- [Livewire Flux Documentation](https://fluxui.dev/docs/installation)
- [Livewire Volt Documentation](https://livewire.laravel.com/docs/volt)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Pest PHP Documentation](https://pestphp.com/docs)

## 🔒 Keamanan

### Best Practices yang Diterapkan

- ✅ CSRF Protection (bawaan Laravel)
- ✅ XSS Prevention (bawaan Blade & Livewire)
- ✅ SQL Injection Prevention (menggunakan Eloquent ORM)
- ✅ Password Hashing (menggunakan bcrypt)
- ✅ Rate Limiting pada login dan password reset
- ✅ Email Verification
- ✅ Secure Password Reset dengan token
- ✅ Middleware authentication & authorization
- ✅ Validated form inputs

## 🎯 Use Cases

Project ini cocok untuk:

- 📱 **SaaS Applications** - Build aplikasi SaaS dengan autentikasi lengkap
- 🏢 **Admin Panels** - Dashboard admin dengan user management
- 🛍️ **E-commerce** - Foundation untuk online shop
- 📊 **Business Applications** - Internal business tools
- 🎓 **Learning Projects** - Belajar Laravel & Livewire

## 📝 License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

---

<p align="center">
<b>Made with ❤️ using Laravel & Livewire</b><br>
⭐ Star this repo if you find it helpful!
</p>
