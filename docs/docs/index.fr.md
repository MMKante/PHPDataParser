# PHP Data Parser - Un parser de données PHP simple

## Introduction
PHP Data Parser est conçu pour faciliter et simplifier les tâches classiques du parsing de données. En fournissant une boite à outil tout-en-un pour vous aider à parser les différentes données utilisées dans vos applications.

Le but de cette présentation est d’introduire les concepts généraux de PHP Data Parser, et de vous donner un aperçu rapide de la façon dont ces concepts sont mis en œuvre dans PHP Data Parser. Si vous êtes impatient de démarrer un projet, vous pouvez commencer avec le tutoriel, ou vous plonger dans la documentation.

## Parsers pris en charges
Voici la liste des types de données pris en charges par PHP Data Parser :

- **array**: les tableaux PHP;
- **stdClass**: Une classe générique vide avec des propriétés dynamiques;
- **JSON**: Notation des objets JavaScript;
- **XML**: Langage de balisage extensible;

## Prérequis
Pour utiliser PHP Data parser il est impératif d'avoir la configuration suivante :
!!! danger "Version de PHP"
	**PHP >= PHP 8.1**

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