Yii2-Start module Slider
========================
Slideshow module for Yii2-Start application.

Requirements
------------

This module is used with Yii2-Start application
[yii2-start](https://github.com/vova07/yii2-start).


Installation
------------

Extract the zip into the folder with your project


```
/my/path/to/yii2-start/vendor/nill/yii2_slider_module
```

Configuration
=============

- Add module to [backend] config section:

```
'modules' => [
    'slider' => [
        'class' => 'nill\slider\Module'
    ]
]
```

- Add alias to "common\config\aliases.php":

```
Yii::setAlias('backend', dirname(dirname(__DIR__)) . '/backend');
```

- Add module to extensions "vendor\yiisoft\extensions.php":

```
'nill/slider' => 
    array (
        'name' => 'nill/slider',
        'version' => '0.1.0.0',
        'alias' => 
        array (
            '@nill/slider' => $vendorDir . '/nill/slider',
    ),
    'bootstrap' => 'nill\\slider\\Bootstrap',
), 
```

- Create a new table in your database from file: `yii2_start_slider.sql`

- RBAC settings: For usage modules create Role "administrateSlider"

```
http://my.domain/backend/rbac/permissions/index/
```

You can also create other roles and change their behavior in the controller module
