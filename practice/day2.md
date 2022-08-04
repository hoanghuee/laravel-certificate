#### 1. How to exe a query using named binding?
   ![img.png](https://github.com/hoanghuee/laravel-certificate/blob/main/asset/img.png)
   
    $results = DB::select('select * from users where id = :id', ['id' => 1]);
#### 2. Can we download Laravel with composer using cmd: composer global require "laravel/installer" ? 
    Yes, for version >= 5.7 it can be use with composer global require laravel/installer
#### 3. Which is the entry point for all requests entering your application and configures autoloading in laravel?
    public/index.php file
#### 4. Which function throws error if no record is found?
    findOrFail($id)
#### 5. Which of the following are the valid middleware Groups?

    EncryptCookies
    ShareErrorsFromSession
    VerifyCsrfToken
    
    => All of those
#### 6. Which is default log file in laravel?
    app/storage/logs/laravel. log
#### 7. How to enable the Query Logging in laravel?
    DB::connection()->enableQueryLog();
#### 8. How to attach cookie to response?
    $response->withCookie(cookie('name', 'value', $minutes));
    return $response;

    $cookie = cookie('name', 'value', $minutes);
    return response('Hello World')->cookie($cookie);
#### 9. How to get Current URL without Parameters?
    use Illuminate\Support\Facades\URL;
    echo URL::current();
#### 10. Which of the following is the correct syntax to define custom blade directive in a service provider?
    Blade::directive()
    Eg: _Blade allows you to define your own custom directives using the directive method._
    Blade::directive('datetime', function ($expression) {
            return "<?php echo ($expression)->format('m/d/Y H:i'); ?>";
        });
#### 11. Which method is used in Eloquent model can use a database column 'slug' other than 'id' when retrieving a given model class?
    public function getRouteKeyName()
    {
        return 'slug';
    }
#### 12. Which artisan command is used to remove the compiled class file?
    clear-compiled
#### 13. What is Blade?
    Blade is the templating engine provided with Laravel.
#### 14. Last Insert ID in Laravel can be retrieved with:
    $id = DB::getPdo()->lastInsertId();
#### 15. Bootstrap directory in Laravel is used to
    Initialize a Laraval application
#### 16. What is difference between total() and count() in pagination?
    count() method give you the number of items in the current page and total() method give the total number of items.
#### 17. How to get a filename in Conctroller?
    $request->file('file_name')->getClientOriginalName();
#### 18. How to get information about the route handling the incoming request?
    $route = Route::current();
    $name = Route::currentRouteName();
    $action = Route::currentRouteAction();