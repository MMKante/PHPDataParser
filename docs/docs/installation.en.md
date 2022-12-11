# Installation

## Requirements

To use PHP Data parser it is imperative to have the following configuration:

!!! warning "PHP version"
	**PHP >= PHP 8.1**

## Installation via composer

Installation command via composer:

```console
$ composer require dataparser/dataparser
```

## Manual installation

To manually install and configure PHP Data parser in your project, please follow these instructions:

1. download the library from repository [:simple-github: GutHub](https://github.com/MMKante/dataparser);
2. Unzip the file **.zip** into a directory in your project;
3. Define in your autoloader the location of the _namespace **DataParser**_.;

If you have followed all the steps to the letter then there should be no problems.

## Quick example of usage

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

Si vous n'avez aucun(s) bug(s) et que vous avez le même résultat, vous êtes prêt à utiliser PHP Data Parser.