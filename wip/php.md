---
title: PHP
category: PHP
layout: 2017/sheet
prism_languages: [php]
---

### Hello world

#### hello.php

```php
<?php
function greetMe($name) {
  return "Hello, " . $name . "!";
}

$message = greetMe($name);
echo $message;
```

All PHP files start with `<?php`.

See: [PHP tags](http://php.net/manual/en/language.basic-syntax.phptags.php)

### Objects

```php
<?php

$fruitsArray = array(
  "apple" => 20,
  "banana" => 30
);
echo $fruitsArray['banana'];
```

Or cast as object

```php
<?php

$fruitsObject = (object) $fruits;
echo $fruitsObject->banana;
``` 

### Inspecting objects

```php
<?php
var_dump($object)
```

Prints the contents of a variable for inspection.

See: [var_dump](http://php.net/var_dump)

### Classes

```php
class Person {
    public $name = '';
}

$person = new Person();
$person->name = 'bob';

echo $person->name;
```

### Getters and setters

```php
class Person 
{
    public $name = '';

    public function getName()
    {
        return $this->name;
    }

    public function setName($name)
    {
        $this->name = $name;
        return $this;
    }
}

$person = new Person();
$person->setName('bob');

echo $person->getName();
```

### isset vs empty
```php

$options = [
  'key' => 'value',
  'blank' => '',
  'nothing' => null,
];

var_dump(isset($options['key']), empty($options['key'])); // true, false
var_dump(isset($options['blank']), empty($options['blank'])); // true, true
var_dump(isset($options['nothing']), empty($options['nothing'])); // false, true

```

### String Functions

Getting length of a string

```php

$str = "change me";
echo strlen($str); //9

```

Counting number of words

```php

$str = "change me";
echo str_word_count($str); //2

```

Reverse a string

```php
$str = "change me";
echo strrev($str); //em egnahc

```

Concatenation of strings

```php

$str = "hello ";
$str2 = "world";

echo $str1.$str2; //hello world 

```

Hash of a string

```php

$str = "change me";
echo md5($str); // c9be20c442bb0680b7c941961f5c3db

```

Lowercase/Uppercase the string

```php

$str = "Change Me";

echo strtolower($str); // change me
echo strtoupper($str); // CHANGE ME

```

Search for text position in a string

```php

$str = "A needle in a haystack";
echo strpos($str,"needle"); // 2

```

String Compare

```php

$str1 = "hello";
$str2 = "Hello world";

echo strcmp($str1,$str2); // 1, because $str1 > $str2

```

Getting part of a string

```php

$str = "Hello world";

echo substr($str,0,6); //Hello ; substr(string, start, end*) *end is optional

```

See More: [String Functions](https://www.php.net/manual/en/ref.strings.php)
