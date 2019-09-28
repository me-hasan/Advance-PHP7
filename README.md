# Advance PHP 7

## ***Variable

### Constant Variable

```php
define ('a','american'); Constant has global scope;
Note : from php 5.6 const allow arithmatic calculation.
```
### Variable variable 
```php
$a = 'America';
$$a = 'Australia';
$$$a= 'Bangladesh';
echo $a; /* America*/
echo '<br/>';
echo $$a; 
echo '<br/>';
echo $Australia;

// $city = 'Dhaka';
// $$city ="104 sen mil";
// echo "$city is capital of bangladesh";
// echo '<br/>';
// echo "the size of $city is $Dhaka";
```

### Reference variable

```php
// $c = 'canada';
// $c= &$d;
// $d='Dhaka';
// echo $c;
// echo '<br/>';
// echo $d;

// function test (&$x)
// {
//     $x = 51110;
// }
// $y = 20;
// test($y);
// echo $y;
```

### Variable scope
```PHP
// $a = 5;
// function test ()
// {
//     global $a;
//     echo $a;
// }
// test();

// $a = 5;
// function test ()
// {
//     $a = 7;
//     echo $a + $GLOBALS['a']; //Super global $GLOBALS
// }
// test();

// $a = 1;
// function test ()
// {
//     global $a;
//     echo $a++;
// }
// test();
```