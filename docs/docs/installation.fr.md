# Installation

## Prérequis

Pour utiliser PHP Data parser il est impératif d'avoir la configuration suivante :

!!! warning "Version de PHP"
	**PHP >= PHP 8.1**

## Installation via composer

Commande d'installation via composer :

```console
$ composer require dataparser/dataparser
```

## Installation manuelle

Pour installer et configurer manuellement PHP Data parser dans votre projet, veuillez suivre les instructions suivantes :

1. télécharger la librairie depuis répertoire [:simple-github: GutHub](https://github.com/MMKante/dataparser);
2. Décompressez le fichier **.zip** dans le répertoire dans un répertoire de votre projet;
3. Définissez au niveau de votre autoloader l'emplacement du _namespace **\DataParser**_;

Si vous avez suivi toutes les étapes à la lettre alors il ne devrait pas y avoir de problèmes.

## Exemple rapide d'utilisation

Voici un exemple rapide d'utilisation PHP Data Parser :

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

Sortie :
```json
{
	"firstname": "John",
	"lastname": "Doe"
}
```

Si vous n'avez aucun(s) bug(s) et que vous avez le même résultat, vous êtes prêt à utiliser PHP Data Parser.