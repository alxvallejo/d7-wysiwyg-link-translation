##  Alias is in path

```php
$path = drupal_get_normal_path($path, $lang);
$translations = translation_path_get_translations(trim($path, '/'));
if (isset($translations[$lang])) {
	$translated_path = $translations[$lang];
	// Check for alias
	$translated_path = drupal_get_path_alias($translated_path, $lang);
}
```
