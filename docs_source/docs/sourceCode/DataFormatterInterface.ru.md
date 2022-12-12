# DataFormatterInterface

## UML диаграмма

```mermaid
  classDiagram
    class DataFormatterInterface {
      <<interface>>
      +convert(array data) mixed
      +toArray(mixed data) array
    }
```

## Исходный код

```php  linenums="1" title="DataFormatterInterface.php"
declare(strict_types=1);

namespace DataParser;

interface DataFormatterInterface {
	
	/**
	 * Convert from array to implemented data format
	 * @param  array  $data
	 * @return mixed
	 */
	public function convert(array $data) : mixed;

	/**
	 * Convert data to array
	 * @param  mixed $data
	 * @return array
	 */
	public function toArray(mixed $data) : array;
}
```