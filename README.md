## Local dev setup, on Ubuntu 18.04 LTS

First install php7.2, composer for installing the project dependencies and the php extensions required by laravel.

    # apt install php composer php7.2-xml php7.2-zip php7.2-tokenizer \
        php7.2-json php7.2-mbstring

Install laravel using composer

    $ composer global require laravel/installer

Clone the project

    $ git clone https://github.org/axelwtf/AGRIDEM
    $ cd AGRIDEM

Install the project dependencies (libraries)

    $ composer install

create a default .env file

    $ cp .env.example .env

generate the application secret key

    $ php artisan key:generate

start the application server

    $ php artisan serve
    
 by default `php artisan serve` will start the dev server on localhost:8000 to specify a different address and port use the `--host` and `--port` flags
 
    $ php artisan serve --host 0.0.0.0 # will be accessible to all.
