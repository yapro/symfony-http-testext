symfony-http-test-ext
--

Traits for solving the most common problems.

How to use
---
Create a class with the getHttpClient method, example: src/ExampleTestCase.php

Useful information
--
* Доступ к внутренним объектам - https://symfony.com/doc/current/testing.html#accessing-internal-objects
* Профилировщик - https://symfony.com/doc/current/testing.html#accessing-the-profiler-data
* Http Переадресация - https://symfony.com/doc/current/testing.html#redirecting
* Отключаем перехват исключений - https://symfony.com/doc/current/testing.html#reporting-exceptions.

Tests
------------
```sh
docker build -t yapro/symfony-http-test-ext:latest -f ./Dockerfile ./
docker run --rm -v $(pwd):/app yapro/symfony-http-test-ext:latest bash -c "cd /app \
  && composer install --optimize-autoloader --no-scripts --no-interaction \
  && /app/vendor/bin/phpunit /app/tests"
```

Dev
------------
```sh
docker build -t yapro/symfony-http-test-ext:latest -f ./Dockerfile ./
docker run -it --rm -v $(pwd):/app -w /app yapro/symfony-http-test-ext:latest bash
composer install -o
```
