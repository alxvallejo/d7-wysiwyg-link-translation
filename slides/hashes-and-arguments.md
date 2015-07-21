##  Hashes and Arguments

```php
$href = $element->getAttribute('href');

// Check for hash on URL
if (strpos($href, '#')) {
	$fragments = explode('#', $href);
	$href = $fragments[0];
}
// Check for arguments in url
if (strpos($href, '?')) {
	$arguments = explode('?', $href);
	$href = $arguments[0];
}
$href = trim($href, '/');
```