# Star Rating extension for laravel-admin

这是一个`laravel-admin`扩展，用来将 [bootstrap-star-rating](https://github.com/kartik-v/bootstrap-star-rating) 集成进`laravel-admin`中。

<img src="https://camo.githubusercontent.com/8ce0822c6ba8b770ddfee452392bf61e1c3bd0f2/68747470733a2f2f6c68332e676f6f676c6575736572636f6e74656e742e636f6d2f707543624e4c394c6c424d747938446d615a78417130794d38746575684d5f6845766f782d4e754a327837785765644e6873386e77536b315a6f384649534641737974383d77313336362d683736382d72772d6e6f" width=300>

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
