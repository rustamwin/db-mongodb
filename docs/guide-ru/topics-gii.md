Использование Gii генератора
===================

Это расширение предоставляет генератор кода, который может быть интегрирован с Yii модулем 'gii'. Он обеспечивает генерацию
Active Record кода. Для того, чтобы включить его, вы должны настроить конфигурацию приложения следующим образом:

```php
return [
    //....
    'modules' => [
        // ...
        'gii' => [
            '__class' => Yiisoft\Yii\Gii\Module::class,
            'generators' => [
                'mongoDbModel' => [
                    '__class' => Yiisoft\Db\MongoDb\Gii\Model\Generator::class
                ]
            ],
        ],
    ]
];
```

> Note: поскольку MongoDB это schemaless - БД, существует не так много информации, которая может основываться на генерируеом коде. Таким образом, сгенерированный код очень простой и, безусловно, требует корректировки.
