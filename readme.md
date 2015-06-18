## Backend Boilerplate

Provides a simple `/backend` page with login and simple user management to add or remove other admins with access to the backend. The default credentials are `admin`/`admin` if nothing else is set in the environment variables. The superadmin won't be visible in the admins table in the backend and cannot be deleted.

### Setup

1. `composer install`
2. `npm install`
3. `gulp`
4. Create `.env` file in the root dir and add the following:

```
  APP_ENV=local
  APP_DEBUG=true
  APP_KEY=anyRandomKey
  ADMIN_USER=admin
  ADMIN_PASS=admin
  
  DB_HOST=localhost
  DB_DATABASE=example
  DB_USERNAME=root
  DB_PASSWORD=
  
  CACHE_DRIVER=file
  SESSION_DRIVER=file
  QUEUE_DRIVER=sync
  
  MAIL_DRIVER=smtp
  MAIL_HOST=mailtrap.io
  MAIL_PORT=2525
  MAIL_USERNAME=null
  MAIL_PASSWORD=null
  MAIL_ENCRYPTION=null
```

4. Edit the DB credentials and prefered admin credentials as needed.
5. Create a new application key by running `php artisan key:generate`
5. `php artisan migrate`
6. `php artisan serve`
7. Enjoy!

### License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT) so the same goes for this project.
