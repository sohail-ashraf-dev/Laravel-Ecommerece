
<h1 align="center">E Commerce REST API</h1>

<p align="center">
  <strong>A robust E-Commerce REST API platform integrated with a Filament Admin Panel.</strong>
</p>

<p align="center">
    <a href="https://php.net">
        <img src="https://img.shields.io/badge/PHP-%5E8.1-777BB4?style=flat-square&logo=php" alt="PHP Version">
    </a>
    <a href="https://laravel.com">
        <img src="https://img.shields.io/badge/Laravel-9.x-FF2D20?style=flat-square&logo=laravel" alt="Laravel Version">
    </a>
    <a href="https://filamentphp.com">
        <img src="https://img.shields.io/badge/Filament-2.x-F2C14E?style=flat-square&logo=livewire" alt="Filament Version">
    </a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License">
    </a>
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#installation">Installation</a> •
  <a href="#configuration">Configuration</a> •
  <a href="#api-documentation">API Docs</a>
</p>

---

## 📖 Overview

E-Commerce is a comprehensive backend solution for e-commerce applications. It provides a full suite of RESTful APIs for frontend consumption and includes a powerful Admin Panel built with Filament for managing users, products, orders, and finances.

## ✨ Features

### Admin Panel


The system includes a robust admin interface with the following capabilities:

| Module | Description |
| :--- | :--- |
| **Users** | Create employees and manage all customer accounts. |
| **Orders** | Full order lifecycle management. |
| **Finances** | Overview of earnings and financial stats. |
| **Withdraw** | Manage merchant withdrawal requests. |
| **Banking** | Create and manage available banking options for merchants. |
| **Categories** | Manage product categories and taxonomy. |
| **Profile** | Admin profile and password management. |

## 🛠 Tech Stack

* **Framework:** Laravel 9.x
* **Language:** PHP ^8.1
* **Admin Panel:** Filament v2
* **Realtime/Websockets:** Laravel Websockets, Pusher (Server & JS)
* **Search:** Laravel Scout (Database driver)
* **Payment Gateway:** Midtrans
* **Shipping:** RajaOngkir
* **Performance:** Laravel Trend, Laravel Debugbar

## 🚀 Installation

Follow these steps to set up the project locally.

### 1. Clone the Repository
```bash
git clone [https://github.com/sohail-ashraf-dev/Laravel-Ecommerece.git](https://github.com/sohail-ashraf-dev/Laravel-Ecommerece.git)
cd Laravel-Ecommerece
````

### 2\. Install Backend Dependencies

```bash
composer install
```

### 3\. Install Frontend Dependencies

```bash
npm install
```

### 4\. Environment Setup

Copy the example environment file and configure it.

```bash
cp .env.example .env
```

### 5\. Generate Application Key

```bash
php artisan key:generate
```

### 6\. Database Setup

Ensure your database credentials in `.env` are correct, then run migrations and seeders.

```bash
php artisan migrate --seed
```

### 7\. Storage Linking

Link the storage folder to the public directory for image serving.

```bash
php artisan storage:link
```

### 8\. Build Assets

```bash
npm run dev
```

## ⚙️ Configuration

Open your `.env` file and configure the following services.

### Database & Email

Update the standard Laravel DB and MAIL credentials:

```ini
DB_DATABASE=your_database_name
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

### Realtime (Websockets/Pusher)

```ini
PUSHER_APP_ID=your_app_id
PUSHER_APP_KEY=your_app_key
PUSHER_APP_SECRET=your_app_secret
PUSHER_HOST=127.0.0.1
PUSHER_PORT=6001
PUSHER_SCHEME=http
PUSHER_APP_CLUSTER=mt1
```

*Note: If using Laravel Valet with SSL, uncomment the `LARAVEL_WEBSOCKETS_SSL` section in the `.env` file.*

### 3rd Party Integrations

```ini
# RajaOngkir (Shipping)
RAJAONGKIR_API_KEY=your_api_key

# Midtrans (Payment)
MIDTRANS_SERVER_KEY=your_server_key
MIDTRANS_PRODUCTION=false
MIDTRANS_SANITIZED=true
MIDTRANS_3DS=true
```

### Search

```ini
SCOUT_DRIVER=database
```

## 📚 API Documentation

The full REST API documentation, including endpoints for authentication, products, and orders, is available via Postman.

[**View Postman Documentation**](https://documenter.getpostman.com/view/25234064/2s93JnUSRS)


## 📄 License

