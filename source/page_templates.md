---
title: Page templates
type: guide
order: 6
---

## Register page templates

Declare **get_virtual_templates()** function in your theme's functions.php. This function should return array value.

``` php
if ( !function_exists('get_virtual_templates') )
{
    function get_virtual_templates()
    {
        return [
            'custom' => 'Custom template',
        ];
    }
}
```
