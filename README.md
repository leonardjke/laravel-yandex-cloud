# yandex-object-storage
Adding configuration for working with Yandex cloud storage to Laravel


# Yandex Object Storage

## Usage

Add the following code to your config/filesystems.php

	    'yandexcloud' => [
		    'driver' => 's3',
		    'key' => 'your_key',
		    'secret' => 'your_secret_key',
		    'endpoint' => 'http://storage.yandexcloud.net/',
		    'region' => 'us-west-2',
		    'bucket' => 'static.example.com',
		    'url' => 'http://static.example.com/',
	    ],

And then you can use

    $disk = Storage::disk('yandexcloud');

to get your yandex cloud storage instance
