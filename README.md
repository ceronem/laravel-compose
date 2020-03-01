# Laravel Compose
![GitHub stars](https://img.shields.io/github/stars/ceronem/laravel-compose?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/ceronem/laravel-compose?style=social)
![GitHub issues](https://img.shields.io/github/issues/ceronem/laravel-compose)
![GitHub](https://img.shields.io/github/license/ceronem/laravel-compose)


Laravel Compose is a Docker-based basic PHP development environment designed for Laravel applications.

## Installation

Just clone this repo.

```bash
git@github.com:ceronem/laravel-compose.git
```

## Configuration

Create an .env file (see .env.example).
```bash
./start --build
```
Is this a new project? No problem, just run:
```bash
./install-laravel
```
A fresh laravel app will be ready soon in your $APP_SRC

Do you have an existing Laravel Project? Just run:
```bash
./init-laravel
```
Laravel Compose will update your Laravel .env with the env variables (please backup it first)
Are you tired of working (we are all tired of working)? Just stop the everythings:
```bash
./stop
```
Go out, take a beer with friends and tell them how Laravel Compose is easy to use. Yes, your friends are all developers!!

## Script
Laravel Compose provides some usefull script:
### start
It's a shortcut to 
```bash
docker-compose up -d
```
You can add the flag --build if you want to build the image, otherwise
```bash
./start
```
is enough to bring up the environment
### stop
I had already explained to you, just stop everything and drink beer
```bash
./stop
```
### install-laravel
It's usefull to bring up a new laravel project. It will prepare a freshly Laravel app in your $APP_SRC and update the Laravel .env with the environments variable.
```bash
./install-laravel
```
### init-laravel
Update the Laravel .env with the environments variable.
### artisan
It will execute an artisan command inside the php_fpm container e.g.
```bash
./artisan make:migration create_example_table
``` 

### composer
It will execute a composer command through the composer container e.g.
```bash
./composer install
``` 
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
