# Laravel-Lumen-Remove-Public-Directory
How to removepublic directory laravel/lumen

<br>
### Version :monocle_face:
php artisan --version
```
Laravel Framework Lumen (8.2.1) (Laravel Components ^8.0)
```
<br><br><hr>

## Public Directory
When we first install the lumen, the default folder/route is set to public. ```http:example.com/public``` .When we want to remove the public directory on the site, we can follow the steps below.

# Step 1:
We move the .htaccess and index.php files in the public folder to the main directory.

# Step 2:
Change index.php
```
$app = require __DIR__.'/../bootstrap/app.php';
```
to
```
$app = require __DIR__.'/bootstrap/app.php';
```

# Step 3:
create file ```home.blade.php``` in resources/views/ 

# Step 4:
add this code in routes/web.php
```
$router->get('/', function () {
    return view('home');
});
```

### :partying_face: :ok_hand: Done. now the main project directory is not public but root directory. http://example.com/
