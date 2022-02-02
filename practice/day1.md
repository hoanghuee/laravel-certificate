### Day 1
#### 1. Which timezone is used by default? 
    UTC
#### 2. Which class is used to hash the Password by-default?
    Hash
#### 3. Can this command: create-project -prefer-dist laravel/laravel <projectname> be used to create project?
    Yes
#### 4. How many characters key "php artisan key:generate" command generates?
    32
#### 5. Which Exception is thrown by findOrFail($id)?
    ModelNotFoundExc
#### 6. How can we pass variables from controller to view in laravel?
    return view('users', $users);
    return view('users')->with('users', $users);
#### 7. In which directory laravel log file is located?
    project_name/storage/logs/
#### 8. Which is default log file in laravel?
    laravel.log
#### 9. How to execute a query using named binding?
    $results = DB::select('select * from users where id = ?', ['id' => 1]);
#### 10. How to access the file extension in controller method?
    $request->file('file_name')->getOriginalFileExtension();
#### 11. Which of the following is used to get the file real path?
    $request->file('file_name')->getRealPath();
#### 12. Which of the following is used to get the file size?
    $request->file('file_name')->getSize();
#### 13. Which command is used to create forms and the associated controllers to perform authentication?
    php artisan make:auth
#### 14. In which method is used to use your own resolution logic in routing?
    Route::bind
#### 15. Which of the following is used to change the default table name in Model?
    protected $table = 'tableName';
#### 16. How can we bind your model to a route with a value other than the model's ID so that it uses column named slug than table ID?
    public function getRouteKeyName() { return 'slug'; }
#### 17. Which is the correct syntax to define a mutator for column name to get value before saving in the database?
    setNameAttribute
#### 18. What does the vendor directory contain?
    Laravel Framework code
#### 19. Where can you find a default time zone set?
    config/app.php
#### 20. How to get current action name in Laravel 5?
    request()->route()->getActionMethod()
#### 21. How to disable maintenance mode in Laravel?
    php artisan down
#### 22. How to install tinker?
    composer require laravel/tinker
#### 23. If you want to create your own config file in config/ folder, what should be the returned value inside of that file?
    Array
#### 24. How to use skip() and take() in Laravel Query?
    $posts = DB::table('user')->skip(5)->take(10)->get();
#### 25. What is softDeletes();
    It does not remove the data from the table. It is used only to flag the records as deleted.
#### 26. In default Laravel 5 Auth, when user fills in email in 'Forgot password', where the generated token is stored?
    in database table "password_reset"
#### 27. Which method returns the average value of a given key?
    avg()
#### 28. Where will you define Laravel's Facades?
    Illuminate\Support\Facades namespace.
#### 29. To enable maintenance mode, simply execute this Artisan command:
    artisan down
#### 30. How to create a controller in Laravel by cmd?  
    php artisan make:controller generate
24/30

#### 1. Can you give an alias to route name
    Yes
#### 2. How to apply required check on 'name' field using Laravel Validation?
    Validator::make(['name' => 'required']);
#### 3. This single command: $ php artisan make:model Post --migration will give you boilerplate for which of the following- i) app/models/Post.php ii) app/controllers/PostsController.php iii) app/database/migrations/timestamp-create_posts_table.php (including the schema)
    i) and iii)
#### 4. Which is the entry point for all requests entering your application and configures autoloading in laravel?
    public
#### 5. Which directory houses a cache directory which contains framework generated files for performance optimization such as the route and services cache files?
    bootstrap
#### 6. Which step do you follow in case the root directory doesn't contain the .env file?
    rename the .env.example to .env file
#### 7. How to get total number of records while using Pagination?
    $users = User::paginate(10); $users->getTotal();
#### 8. How to produce parameters as optional in the routes?
    Route::get('route-name/{param}', function ($param = 'Optional Parameter') { return $param;});