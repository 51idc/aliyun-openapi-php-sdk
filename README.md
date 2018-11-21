# Open API SDK for php developers

## Requirements

- PHP 5.3+

## Build

- to run unit tests, you will have to configure aliyun-sdk.properties files in your user directory, and make sure your project has corresponding service enabled, eg. openmr.

## Composer Support

```shell
composer require qfz9527/aliyun-openapi-php-sdk:dev-master
```

## Example

```php
include_once 'vendor/autoload.php';

use Ecs\Request\V20140526 as Ecs;

$iClientProfile = DefaultProfile::getProfile("cn-hangzhou", "<your accessKey>", "<your accessSecret>");
$client = new DefaultAcsClient($iClientProfile);

$request = new Ecs\DescribeRegionsRequest();
$request->setMethod("GET");
$response = $client->getAcsResponse($request);
print_r($response);
```
## Authors && Contributors

- [Zuhe]()
- [Ma Lijie](https://github.com/malijiefoxmail)

## License

licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.html)
