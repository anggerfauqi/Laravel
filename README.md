# Simple Laravel Project
Simple Laravel CRUD integrated with :
- Admin LTE
- Yajra Datatables
- MySQL Database

# Install Composer
[Download composer here](https://getcomposer.org/Composer-Setup.exe)

# Installation & Create New Laravel Project
I'm using Visual Studio Code for Code Editor

use terminal for installation process.

you can press **ctrl+shift+`** for open new terminal in visual studio code


### Install Laravel with composer
```
composer global require laravel/installer
```


### Create New Laravel Project
``` 
laravel new your-project 
```
**optional** Create Project also Create New GIT Repository for Your New Project
```
laravel new your-project --github="--public" --organization="laravel"
```

# Connecting Database

**http://localhost/phpmyadmin/**

**Create New Database**
```
create database yourdatabase
```
 
**Set Your New Database to Your Laravel Project
- open **.env** file on your project folder
- set DB_DATABASE=yourdatabase
- DB_USERNAME=yourdatabaseusername *Default* **root**
- DB_PASSWORD=yourdatabasepassword *Default* **empty / null**


### Installation Finish, Open Your Directory
```
cd your-project
```

# Admin LTE integration
## Install Admin LTE Project with Composer
```
composer require jeroennoten/laravel-adminlte
```

### Install Laravel UI for Manage Your UI Template by doing this step :
```
composer require laravel/ui
```

```
php artisan ui:controllers
```

```
php artisan ui:auth
```

*if auth already exist, press **Y** all step to create new authentication*

### Install AdminLTE on Your Laravel Project
```
php artisan adminlte:install
```

### Install AdminLTE Plugins
```
php artisan adminlte:plugins install
```

### Install main view
```
php artisan adminlte:plugins install --only=main_views
```

### Install authentication view
```
php artisan adminlte:plugins install --only=auth_views
```

### Everything is done successfuly, run your project
```
php artisan serve
```
Open localhost with port 8000 on your browser to run Your Project

**http://127.0.0.1:8000/** or [clik this](http://127.0.0.1:8000/)


# Yajra DataTables Integration

## install Yajra with Composer
```
composer require yajra/laravel-datatables-oracle
```

### publish Yajra configuration & assets 
set service providers & aliases inside the **config/app.php** file 
```
.....
.....
'providers' => [
	....
	....
	Yajra\DataTables\DataTablesServiceProvider::class,
]
'aliases' => [
	....
	....
	'DataTables' => Yajra\DataTables\Facades\DataTables::class,
]
.....
.....
```
### Publish Yajra Vendor
use the following command to publish configuration & assets
```
php artisan vendor:publish --tag=datatables
```

If you would like to overwrite existing files, use the **--force** switch and select the number :
```
php artisan vendor:publish --force
```
