# Yark UUID
A simple trait to provide UUID support on Eloquent models.

### Installation

```composer require yark/yark-uuid-model```

### Usage

To use this in a model, add the HasUuid trait

```php
<?php

namespace App;
use YarkHQ\LaravelUuidModel\HasUuid;

class Book extends Eloquent
{
    use HasUuid;
}
```

In the default configuration, a UUID will be persisted when creating a model in the UUID column. To change the column, override the $uuidColumn property.

```php
<?php

namespace App;
use YarkHQ\LaravelUuidModel\HasUuid;

class Book extends Eloquent
{
    use HasUuid;
    protected $uuidColumn = 'uuid_key';
}
```

Route keys will also be set automatically so you can create a route and use UUIDs. If you want to change this then override the $routeKeyName property in your model.

```php
<?php

namespace App;
use YarkHQ\LaravelUuidModel\HasUuid;

class Book extends Eloquent
{
    use HasUuid;
    protected $routeKeyName = 'slug';
}
```

### License

Licensed under the MIT license
