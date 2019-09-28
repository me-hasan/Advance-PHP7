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


#

## ***Operator

### Assignment operator
```php
$a = $a +7;
$a += 4;
$a -= 4;
$a *= 4;
$a /= 4;
$a %= 4;
```

### Arithmetic Operator
```php
+ - % *
```

### Comparision Operator
```php


echo $a == $b // 1 if it is true
  Identical comparision operator ===
  value same but type not equal !==

  Not equal != or <> 

  spaceship operator
     |$a = 6
     |$b = 6
     |$c = 7   
     $a<=>$b // 0
     $a<=>$c // -1
     $c<=>$a // 1l
```

### String operator
```php
$a .= 'Bangladesh';

Implement implement operator
	post implement++, pre implement --
```

### Bitwise operator  	
```php
   5&1 // first convert 5 into binary then it will check condition.....

	if(5&1){
	   echo 'even';
	}else{
		echo 'odd';
	}
   &  --- and
   !  --- or
   ^  --- XOR
   << --- Left shift
   >> --- Right shift
```
