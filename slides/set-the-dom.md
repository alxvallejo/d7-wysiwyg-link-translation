##  Set the DOM

```php
$element->setAttribute('href', $new_alias);
$urls_translated++;
```

```php
if ($urls_translated > 0) {
	$new_subject = preg_replace('/^<!DOCTYPE.+?>/', '', str_replace( array('<html>', '</html>', '<body>', '</body>'), array('', '', '', ''), $dom->saveHTML()));
	$num_updated = db_update($table)
	  ->fields(array(
	    $field . '_value' => $new_subject
	  ))
	  ->condition('entity_id', $row->entity_id, '=')
	  ->condition('language', $row->language, '=')
	  ->execute();
	if ($num_updated > 0) {
	  drush_print($urls_translated . ' links translated in field ' . $field);
	}
}
```

