# Yandex Object Storage for Laravel
Adding configuration for working with Yandex cloud storage to Laravel

## Usage

To work with Yandex Object Storage, you need to add a package using the Composer:

```
composer require league/flysystem-aws-s3-v3 ~1.0
```

Add the following code to your config/filesystems.php

```
'yandexcloud' => [
    'driver' => 's3',
    'key' => 'your_key',
    'secret' => 'your_secret_key',
    'endpoint' => 'http://storage.yandexcloud.net/',
    'region' => 'us-west-2',
    'bucket' => 'static.example.com',
    'url' => 'http://static.example.com/',
],
```

And then you can use

```
$disk = Storage::disk('yandexcloud');
```

to get your yandex cloud storage instance

## How to check?
```
php artisan tinker
```

```
Storage::disk('yandexcloud')->put('hello.txt', 'check text');
Storage::disk('yandexcloud')->files();
Storage::disk('yandexcloud')->url('hello.txt');
```
## Cloud documentation
https://cloud.yandex.ru/docs/storage/quickstart
