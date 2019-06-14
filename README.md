ruturajmaniyar/yii2-flash-toastr
=========================
Toastr flash notification using jQuery with yii2

![GitHub release](https://img.shields.io/github/release-pre/ruturajmaniyar/yii2-flash-toastr.svg)
[![Packagist](https://img.shields.io/packagist/dt/ruturajmaniyar/yii2-flash-toastr.svg)](https://packagist.org/packages/ruturajmaniyar/yii2-flash-toastr)

Current Version
---------------
v1.0 @stable @pre-release

Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require --prefer-dist ruturajmaniyar/yii2-flash-toastr: "dev-master"
```
or

```
composer require --prefer-dist ruturajmaniyar/yii2-flash-toastr: "dev-master"
```

or add

```
"ruturajmaniyar/yii2-flash-toastr": "dev-master"
```

to the require section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
<?php if (Yii::$app->session->hasFlash('success')): ?>
    <?= ToastrFlashMessage::widget([
        'type' => 'success',
        'title' => 'Success',
        'message' => Yii::$app->session->getFlash('success')
    ]); ?>
<?php endif; ?>

<?php if (Yii::$app->session->hasFlash('error')): ?>
    <?= ToastrFlashMessage::widget([
        'type' => 'error',
        'title' => 'Error',
        'message' => Yii::$app->session->getFlash('error')
    ]); ?>
<?php endif; ?>
```

You can also use with below code

```php
<?= ToastrFlashMessageSession::widget() ?>
```
With above code, extension set toastr message dynamically based on your flash session message

Other Options
-------------
```php
'options' => [
        "closeButton" => true,
        "newestOnTop" => true,
        "progressBar" => true,
        "positionClass" => ToastrFlashMessage::POSITION_TOP_RIGHT,
        "showDuration" => "300", 
        "hideDuration" => "1000",
        "timeOut" => "5000",
        "extendedTimeOut" => "1000",
        "showEasing" => "swing",
        "hideEasing" => "linear",
        "closeEasing" => "linear",
        "showMethod" => "slideDown",
        "hideMethod" => "slideUp",
        "closeMethod" => "slideUp"
    ]
```
##### Toast Position Options:
```
POSITION_TOP_RIGHT = 'toast-top-right';
POSITION_TOP_LEFT = 'toast-top-left';
POSITION_TOP_CENTER = 'toast-top-center';
POSITION_TOP_FULL_WIDTH = 'toast-top-full-width';

POSITION_BOTTOM_RIGHT = 'toast-bottom-right';
POSITION_BOTTOM_LEFT = 'toast-bottom-left';
POSITION_BOTTOM_CENTER = 'toast-bottom-center';
POSITION_BOTTOM_FULL_WIDTH = 'toast-bottom-full-width';
```

##### DEMO

* http://codeseven.github.io/toastr/demo.html
