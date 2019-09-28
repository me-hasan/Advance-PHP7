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

### Structure Control

#### if
```php
$a = 5;
if(!$a){
    echo "Yes";
}else{
    echo "No";
} 
echo "<br>";
if($a){
    echo "Yes";
}else{
    echo "No";
}

echo "<br>";
echo "<br>";
if($a == 1){
    echo 1;
}elseif($a == 2){
    echo 2;
} // if ba ifelse er jonno else mandatory na


echo "<br>";
echo "<br>";
```
#### Switch

```PHP
$switching = 10;
switch($switching){
    default:
    echo "tai naki";
    break;
    case 10:
    echo 10; 
} 
echo "<br>";
echo "<br>";

for($i = 1; $i<=10; ++$i){
    echo $i, "<br>";
} 

```

#### Do While
```php
$do = 11;
do{
    echo $do;
} 
while($i<=10);

```
#### for
```php
for($i = 1; $i<=10; ++$i){
    if($i == 5){
        break;
    }
    echo $i, "<br>";
}  
echo "<br>";
echo "<br>";
for($i = 1; $i<=10; ++$i){
    echo $i, "<br>";
    if($i == 5){
        break;
    }
}  
echo "<br>";
echo "<br>";
for($i = 1; $i<=10; ++$i){
    if($i == 5){
        continue;
    }
    echo $i, "<br>";
}  

echo "<br>";
echo "<br>"; 

for($i = 1; $i<=10; ++$i){
    if($i == 5 || $i == 7){
        continue;
    }
    echo $i, "<br>";
}  

echo "<br>";
echo "<br>";

goto a;
echo "Foo";
for($i = 1; $i<=10; ++$i){
    if($i == 5 || $i == 7){
        continue;
    }
    echo $i, "<br>";
} 

a:
echo "bar";


for($i=0, $j=50; $i<100; $i++){
    while($j--){
        if($j == 30) goto end;
    }
}
echo "i = $i";
end:
echo "J hit $j"; 



echo "<br>";
echo "<br>";
echo rand(100,1000);

```
