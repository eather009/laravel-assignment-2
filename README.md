# Steps for Assignment tasks

## 1. Create Project
<code>composer create-project laravel/laravel ostad-laravel-assignment</code>

## 2. Controller Create
<code>php artisan make:controller UserController</code>

## 3. Route added
routes/web.php<br/><code>Route::get('/sayhello',[UserController::class,'sayHello']);</code>

app/Http/Controllers/UserController.php<br/><code>
public function sayHello(){
        return 'Hello, Laravel!';
    }</code>

<code>php artisan route:list</code>

## 4. Create Server and Test by URL
<code>php artisan serve</code>

URL: http://127.0.0.1:8000/sayhello
