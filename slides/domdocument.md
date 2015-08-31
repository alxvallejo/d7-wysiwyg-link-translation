##  DOMDocument

#### to the rescue

```
$dom = new DOMDocument;
$dom->loadHTML(mb_convert_encoding($subject, 'HTML-ENTITIES', 'UTF-8'));
foreach ($dom->getElementsByTagName('a') as $element) {
	// Translate that shit
}
```
