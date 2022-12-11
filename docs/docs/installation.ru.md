# Установка

## Необходимые условия

Для использования парсера данных PHP Data необходимо иметь следующую конфигурацию:

!!! warning "PHP версия"
	**PHP >= PHP 8.1**

## Установка через composer

Команда установка через composer:

```console
$ composer require dataparser/dataparser
```

## Ручная установка

Чтобы вручную установить и настроить парсер PHP Data в вашем проекте, следуйте приведенным ниже инструкциям:

1. скачать библиотеку из директории [:simple-github: GutHub](https://github.com/MMKante/dataparser);
2. Распакуйте файл **.zip** в директорию вашего проекта;
3. Определите расположение _пространства имен **DataParser**_ в вашем автозагрузчике;

Если вы выполнили все шаги в точности, то проблем возникнуть не должно.

## Быстрый пример использования

Вот краткий пример использования PHP Data Parser:

```php
use \DataParser\{DataParser, DataFormat};

$data = [
	'firstname' => 'Иван',
	'lastname' => 'Иванович'
];

$parser = new DataParser($data, DataFormat::ARRAY_FORMAT);
$parsedData = $parser->convertTo(DataFormat::JSON_FORMAT);

print_r($parsedData);

```

Выход:
```json
{
	"firstname": "Иван",
	"lastname": "Иванович"
}
```

Si vous n'avez aucun(s) bug(s) et que vous avez le même résultat, vous êtes prêt à utiliser PHP Data Parser.