# PHP Data Parser - An easy PHP data parser

## Introduction
PHP Data Parser is designed to facilitate and simplify the classic tasks of data parsing. By providing an all-in-one toolkit to help you parse the various data used in your applications.

The purpose of this presentation is to introduce the general concepts of PHP Data Parser, and to give you a quick overview of how these concepts are implemented in PHP Data Parser. If you are eager to start a project, you can start with the tutorial, or dive into the documentation.

## Supported parsers
Here is the list of data types supported by PHP Data Parser:

- **array**: PHP array;
- **stdClass**: A generic empty class with dynamic properties;
- **JSON**: JavaScript Object Notation;
- **XML**: Extensible Markup Language;

## Requirements

To use PHP Data parser it is imperative to have the following configuration:

!!! danger "PHP version"
	**PHP >= PHP 8.1**

## Quick example of use

Here is a quick example of how to use PHP Data Parser:

```php
use \DataParser\{DataParser, DataFormat};

$data = [
	'firstname' => 'John',
	'lastname' => 'Doe'
];

$parser = new DataParser($data, DataFormat::ARRAY_FORMAT);
$parsedData = $parser->convertTo(DataFormat::JSON_FORMAT);

print_r($parsedData);

```

Output:
```json
{
	"firstname": "John",
	"lastname": "Doe"
}
```