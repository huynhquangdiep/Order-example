<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

## How to use

- git clone https://github.com/MinhTri1911/order-demo.git ten-project
- composer install
- npm install
- config file .env
- Every time when change config then shutdown server and run command
```
 php artisan config:clear
```
- Restart server
```
 php artisan serve
```

## Example

# 1 Move all model to folder Models
- path: app/Models
- config model User file config/auth.php
```
'providers' => [
    'users' => [
        'driver' => 'eloquent',
        'model' => App\Models\User::class,
    ],
]
```

## Explain struct assets
```
   - js // folder contain all file js will be combine to folder public/js
   - sass // folder contain all file scss will be build to file css in folder public/css
   - images // folder contain all file png, svg v.vvv to will be copy to folder public/images
   - lang // folder contain all file translate
   - views // folder contain all file will be render html
```

# Step to build scss and js to public/css and public/js

# 1 Run command

```
npm run watch // command will be watch all change and rebuild to css or js to public/css or public/js
```

# 2 Create new file js or scss

- After crete file in folder scss or js then config file webpack.mix.js
- Add line code ```sass('resources/sass/path_to_file_name/filename.scss', 'public/css')```
then laravel mix will be build content file to public/css/path_to_file_name/filename.css
- Add line code ```js('resources/js/path_to_file_name/filename.js', 'public/js')```
then laravel mix will be build content file to public/js/path_to_file_name/filename.js
- Shutdown npm (CTRL + C) and restart command ```npm run watch```
