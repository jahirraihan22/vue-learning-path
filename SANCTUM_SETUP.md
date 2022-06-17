# setup sanctum in lumen

### step 2
    
    composer require laravel/sanctum
    
### step 3

     php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"


### step 3

    
    php artisan migrate
    
    
### step 4

in ***app/Http/Kernel.php***

    'api' => [
          \Laravel\Sanctum\Http\Middleware\EnsureFrontendRequestsAreStateful::class,
          'throttle:api',
          \Illuminate\Routing\Middleware\SubstituteBindings::class,
      ],
      
 src : https://remotestack.io/laravel-sanctum-auth-and-crud-rest-api-tutorial/
