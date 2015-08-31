##  node/1234

```php
if (strstr($href, 'node/')) {
    $url_parts = explode('node/', $href);
    $nid = $url_parts[1];
    // Check language of url
    $node = node_load($nid);
    if (isset($node->tnid)) {
    	$check = translation_node_get_translations($node->tnid);
    }
}
```