# JSON Web Token Authentication for Lumen REBOOT

I see that a lot of you are having problems with my blog post on [JSON Web Token Authentication for Lumen](https://laravelista.com/posts/json-web-token-authentication-for-lumen#comments). I've been reading all comments and emails about it, but because this post was written more than one year ago I decided to reboot the whole post instead of trying to fix issues that have been piling on.

At the time when I wrote that post you could actually follow along and get the wanted result, but packages changed/updated, new versions of Lumen released and things broke.

So, for this lesson I will be using Lumen 5.3 (which is the latest Lumen version released at the time of this lesson) with [tymondesigns/jwt-auth](https://github.com/tymondesigns/jwt-auth) package version `1.0.0-alpha.3` to implement JWT authentication in Lumen.

## Installation

Clone repository to your drive and type in terminal there:

```
composer install
```

## Configuration

Copy file `.env.example` to `.env` file:

```
cp .env.example .env
```

and change the `APP_KEY` in `.env` to a 32 characters long string.

Run `php artisan jwt:secret` to generate a new *JWT Authentication Secret*.

Create empty database file called `database.sqlite` in `database` directory.

Run migrations and seed database with:

```
php artisan migrate --seed
```

## Running

From terminal type:

```
php -S localhost:8000 -t public/
```

You should get an address to open in your browser like http://localhost:8000.

**Have fun!**
