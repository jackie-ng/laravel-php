### Docker

Install + start container

```bash
.vendor/bin/sail/up -d
```

Check status of containers

```bash
docker ps
```

Go to main container

```bash
./vendor/bin/sail bash
```

### PHP

All about PHP Artisan CLI

```bash
php artisan --help
```

Install laravel/breeze dev dependency

```bash
composer require laravel/breeze --dev
```

Create a migration in the database

```bash
php artisan make:model File -m
```

Apply change or check if the application is connected to sucessfully or "migrated"

```bash
php artisan migrate
```

Run Laravel application

```bash
php artisan serve
```

### Create Laravel Database

Connect to a database by changing the necessary ports in .env

Generate a new table

```bash
php artisan make:migration create_products_table
php artisan migrate
```

### Create Laravel Model

Eloquent

```bash
php artisan make:model Products
```

Product.php

```php
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Database\Eloquent\Model;

class Product extends Model
{
    use HasFactory;

    protected $fillable = [
        'name',
        'qty',
        'price',
        'description'
    ];
}

```

### Create Laravel Controllers

```bash
php artisan make:controller ProductController
```
