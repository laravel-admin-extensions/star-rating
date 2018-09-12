# Star Rating extension for laravel-admin

这是一个`laravel-admin`扩展，用来将 [bootstrap-star-rating](https://github.com/kartik-v/bootstrap-star-rating) 集成进`laravel-admin`中。

## 安装

首先，安装依赖：
```bash
composer require jxlwqq/star-rating
```

然后，发布资源目录：
```bash
php artisan vendor:publish --tag=laravel-admin-star-rating
```

## 配置

在`config/admin.php`文件的`extensions`，加上属于这个扩展的一些配置
```php

'extensions' => [
 
     'star-rating' => [
     
         // 如果要关掉这个扩展，设置为false
         'enable' => true,
         
         // 配置
         'config' => [
             'min' => 1, 'max' => 5, 'step' => 1, 'size' => 'xs'
         ]
     ]
 ]

```

更多配置可以到[Bootstrap Star Rating 文档](http://plugins.krajee.com/star-rating)找到。

## 使用

在form表单中使用它：
```php
$form->starRating('code');
```


## License

Licensed under [The MIT License (MIT)](LICENSE).
