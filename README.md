
# 安装

```
composer require ajiho/think-paginator-driver
```


# 支持的分页驱动

- bootstrap5


# 使用

## 全局生效

在`app/provider.php`文件中重新绑定`think\Paginator`分页服务驱动


```php
'think\Paginator' => \ajiho\paginator\driver\Bootstrap5::class
```

## 部分应用生效

在应用目录中新建`provider.php`文件，然后重新绑定服务即可

```php
'think\Paginator' => \ajiho\paginator\driver\Bootstrap5::class
```

## 单次生效

在调用`paginate`分页方法前,重新绑定服务

```php
\think\facade\App::bind('think\Paginator', \ajiho\paginator\driver\Bootstrap5::class);
$users = User::paginate(10);
//...
```


