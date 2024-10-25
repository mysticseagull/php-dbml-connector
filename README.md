# php-dbml-connector

`php-dbml-connector` is a PHP library that connects to a database and fetches schema information. It works seamlessly with the `php-dbml-core` package, providing a convenient way to retrieve database metadata for further processing.

## Features

- **Database Connection**: Connect to different databases with minimal configuration.
- **Fetch Schema Information**: Retrieve detailed schema information, including tables, columns, relationships, and more.

## Installation

You can install the package via Composer:

```bash
composer require mysticseagull/php-dbml-connector
```

## Usage

### Connect to a Database

To connect to a database, you need to specify the connection parameters:

```php
use MysticSeagull\DbmlConnector\Connector;

$connector = new Connector([
    'driver' => 'mysql',
    'host' => '127.0.0.1',
    'database' => 'your_database',
    'username' => 'your_username',
    'password' => 'your_password',
]);

$connection = $connector->connect();
```

### Fetch Schema Information

Once connected, you can fetch the schema information:

```php
use MysticSeagull\DbmlConnector\SchemaFetcher;

$schemaFetcher = new SchemaFetcher($connection);
$databaseSchema = $schemaFetcher->fetchSchema();
```

## Requirements

- PHP 7.4 or higher
- Composer
- Database driver (MySQL, PostgreSQL, etc.)

## Contributing

Contributions are welcome! Please submit a pull request or create an issue to get started.

## License

This package is open-sourced software licensed under the [MIT license](LICENSE).

## Contact

For any inquiries, please contact [your-email@example.com](mailto:your-email@example.com).
