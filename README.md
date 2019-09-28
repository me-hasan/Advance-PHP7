# Advance PHP 7

## 1.Variable
#### Constant Variable

```php
define ('a','american'); Constant has global scope;
Note : from php 5.6 const allow arithmatic calculation.
```#### Variable variable 
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
#### Reference variable

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
#### Variable scope
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

## 2.Operator
#### Assignment operator
```php
$a = $a +7;
$a += 4;
$a -= 4;
$a *= 4;
$a /= 4;
$a %= 4;
```
#### Arithmetic Operator
```php
+ - % *
```
#### Comparision Operator
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
#### String operator
```php
$a .= 'Bangladesh';

Implement implement operator
	post implement++, pre implement --
```
#### Bitwise operator  	
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

## 3.Control Structures

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

#
## 4.Function
#### It get all args as array
```php
// function test(){
//     $args = func_get_args(); // It get all args as array... by function
//     print_r($args);
// }
// echo '<pre>';
// test(5,2,5);


```
#### Expect array type parameter
```PHP
// function test(...$arg){
//     // It get all args as array... 
//     print_r($arg);
// }
// echo '<pre>';
// test(5,2,5);

```#### It pass array to function
```PHP
// function test($a, $b, $c, $d){
//     echo $b;
// }
// $param = [5,4,3,2,1,0];
// test(...$param);
```#### Function within Function
```PHP
// function foo(){
//     function bar(){
//         return "<br/>bar";
//     }
//     return 'hello';
// }
// echo foo();
// echo bar();
```
#### Conditional function
```PHP
// $makefoo = true;
// if($makefoo){
//     function foo(){
//         return 'foo';
//     }
// }
// echo foo();
```
#### Recursive function
```PHP
//Recursive function
// function calcfact($num){
//     static $product = 1;
//     if($num>1){
//         $product *= $num;
//         $num--;
//         calcfact($num);
//     }
//     return $product;
// }
// echo calcfact(4);


// function x(){
//     echo 5;
// }

// function y(){
//     echo 7;
// }

// echo x()+y();

```
#### Strict type
```php

//declare(strict_types = 1);

// function test(int $u){ //receive result with type 
//     return $u;
// }

// echo test(5);

// function test(array $u){
//     echo '<pre>';
//     print_r($u);
// }

//  test([1,4,32]);


// function test():float{ // return result with type
//     return 5+1.2;
// }
// echo test();

```
#### Variable function
```php
// function sum ($x, $y){
//     return $x+$y;
// }
// $x = 'sum';
// echo $x(7,5);

```
#### Anonymous function
```php
// $test = [
// function  (){
//     return 5;
//     },

// function (){
//     return 6;
//     }
// ];

// echo $test[0]();
// echo $test[1]();


// $makegreeting = function($name, $timeOfDay){
//     return "$timeOfDay $name";
// };

// echo $makegreeting("Khayrul", "Good Morning,");

```
#### LAMDA FUNCTION 
```php
// If a function take a annonymous function as (parametter or args) IT"S CALL LAMDA FUNCTION
// function test($a){
//     return $a();
// }
// echo test(function(){return "Hello world";});
```
#### Closures Function 
```php
// $student = "Khayrul";
// $output = function() use($student){
//     return "Welcome $student";
// };
// echo $output();

function myClosure($num){
    return function ($x) use ($num){
        return $num*$x;
    };
}

$clouse = myClosure(10);
echo $clouse(2)."<br/>";
echo $clouse(3)."<br/>";
echo $clouse(5)."<br/>";

```

## 5. Array
```php
// php array ..............
$a = [3, 4, true]; // basic syntex

$a = array('fdfd', 9); // array function

```
####  Type of array base on "Dimension"
```php

//
// 1. single array
// 2. nested array 


```
####  Type of array base on "Index"
```php

// 1.Numeric array (index will be number)
// 2. Associative array (Index will be string)
// 3. Hybride array ( Index will be number & string)


$z= ['a'=>'america', 'b'=>2, 'c'=>true];
$a=['a','a'=>'america','b'];


$man = [2=>7, 0=>9, true, 3=>4, 1,2];


/***
 * numeric array gula alada vabe indexing hoy, jodioo maj khane string index thake . 
 * maximum number er jonno array index er maximum index + 1 assign kore porer index er jonno.
 * 
 */

//  $m = ['a', ['b',['c'=>'d',[1,2]]]];

//  $n=[[[[[['while']]]]]];

// echo '<pre>';
// echo ($m[1][1][0][1]);

// echo $n[0][0][0][0][0][0];



```
####  Array print different way
```php
$m = ['a'=>'america', 'b', 'c'=>'canada', 4, 8, 'man'];

reset($m);

/** out put foreatch */
// foreach($m as $key=>$value){

//     //echo '<br/>', $value;

//     //echo '<br/>', $key;

//     echo '<br/>',"key". ' '.$key. '. value '.$value;
// }
```
####  Array print different way
```php

/** out put for loop */
// for($i = 0; $i < count($m); $i++){

//     //echo '<br/>', $value;

//     //echo '<br/>', $key;

//     //echo '<br/>',"key". ' '.$i. '. value '.$m;

//     echo key($m).' value '.current($m), '<br/>';
//     next($m);
// }

```
####  Out put for while loop
```php
$i = 0;
$arr = count($m);
while($i<$arr){
    echo key($m).' value '.current($m), '<br/>';
    next($m);
    $i++;
}


// for($i = 0; $i<=10; print $i.'<br/>',  $i++);

// $am = 1;

// while(10>$am):
//      $am++;
//     echo $am;
// endwhile;      

```
####  array to variable convert
```php
// 
// $b = 'apple';
// $array = ['america', 'b'=>'beljiam', 'c'=>'canada', 'Australia'];
// // extract($array);
// // echo $a, ' ', $b;

// extract($array, EXTR_PREFIX_SAME, 'x');
// echo $x_0, ' ', $x_b, ' ', $x_c, ' ', $x_1, ' ';
// echo $b;

```
####  Variable to array convert ...
```php
// 

// $a = 'Red';
// $b = 'Green';
// $c = 'Blue';

// $array = compact(['a', 'b', 'c']);
// echo '<pre>';
// print_r($array);


```
####  List
```php
$arr = ['a', 'b', 'c', 'd'];
// list($x, $y, $z) = $arr;
// echo $x, ' ', $y, ' ', $z;


//each function
// echo '<pre>';
// print_r(each($arr));

// while(list($key, $value) = each($arr)){
//     echo "$key = $value", '<br/>';
// }

```
####  Call back function for array order
```php

//

// $a  = ['a'=>'a', 'b'=>'d', 'd'=>'b', 'c'=>1];
// function sortAsc($a, $c){
//     if($a == $c){
//         return 0;
//     }
//     return $a<$c ? -1:1;
// }
// uksort($a,'sortAsc');
// echo '<pre>';
// print_r($a);
```
####  Array multi sort array
```php
// 

// $arr1 = [10,100, 500, 100, 103];
// $arr2 = [12,105, 503, 155, 3];
// array_multisort($arr1, $arr2);
// pr($arr1);
// pr($arr2);


```
####  Range function for array filter
```php
// 

// $number = range(1, 30);
// $odd = array_filter($number, function($num){
//     return $num % 2 === 1;
// });
```
####  Array filter by key (use user defined)
```php
// 

// $county = ['a'=>'America', 'b'=>'Bangladesh', 'c'=>'canada', 'd'=>'denmak'];
// function filterBykey ($key){
//     return ($key == 'a' || $key == 'c');
// }
// $myarray = array_filter($county, 'filterBykey', ARRAY_FILTER_USE_KEY);
// pr($myarray);

```
####  Array filter by key and both (use user defined)
```php
// 

$county = ['a'=>'America', 'b'=>'Bangladesh', 'c'=>'canada', 'd'=>'denmak'];
function filterByBoth ($val, $key){
    return ($key == 'a' || $val == 'denmak');
}
$myarray = array_filter($county, 'filterByBoth', ARRAY_FILTER_USE_BOTH);
pr($myarray);



function pr($data)
{
    echo '<pre>';
    print_r($data);
    echo '</br>';
}


```
####  sortAsc
```php
$a = $b = $c = ["a"=>3, "b"=>2, "e"=>5, "d"=>6, "f"=>1]; 
function sortAsc($a, $b){
    if($a == $b){
        return 0;
    }
    return $a<$b ? -1:1;
}
```
####  usort
```php

usort($a, "sortAsc");
echo "<pre>";
print_r($a);
```
####  asortAsc
```php

echo "<br>"; 
function asortAsc($a, $b){
    if($a == $b){
        return 0;
    }
    return $a<$b ? -1:1;
}
```
####  usort
```php

uasort($b, "asortAsc"); 
print_r($b);

echo "<br>";
```
####  uksort
```php
uksort($c, "asortAsc");
print_r($c);
```
####  Sequence filter first to second array
```php

// 
$ar1 = [10,100,100,0];
$ar2 = [1,3,2,4];
array_multisort($ar1, $ar2);
print_r($ar1);
print_r($ar2);

echo "<br>";
$numbers = range(1,30);
print_r($numbers);

echo "<br>"; 

print_r(array_filter($numbers, function($num){
    return $num % 2 == 1;
}));

print_r(array_filter($numbers, function($num){
    return $num % 2 == 1;
}, ARRAY_FILTER_USE_KEY ));

$country = ['a'=>"america", 'b'=>"bangladesh", "c"=>"canada",'d'=>"denmark"];

print_r(
    array_filter($country, function($key){
        return ($key == "a" || $key == "c");
    }, ARRAY_FILTER_USE_KEY));

print_r(
    array_filter($country, function($value, $key){
        return ($key == "a" || $value == "denmark");
    }, ARRAY_FILTER_USE_BOTH ));

---------------------
```
####  Array Map
```php
$number = range(1,5);
echo "<pre>";
print_r(array_map(function($num){
    // return pow($num, 3);
    // return $num*$num*$num;
    return $num ** 3;
}, $number)); 

print_r(array_filter($number, function($num){
    return $num**3 == 8;
}));

$arr = [
    "a"=>"Ruhul Amin",
    "b"=> "Habib Khan",
    "c" => "Karim Uddin" 
];
echo "<br>";
```
####  Array Walk
```php


array_walk($arr, function($value, $key){
    echo "In $key has $value<br>";
});

$arr_2d = [
    "a"=>"Ruhul Amin",
    "b"=> "Habib Khan",
    "c" => "Karim Uddin",
    "d"=> [
        "a"=>"Ruhul Amin",
        "b"=> "Habib Khan",
        "c" => "Karim Uddin",
        "d"=> [
            "a"=>"Ruhul Amin",
            "b"=> "Habib Khan",
            "c" => "Karim Uddin",
        ] 
    ] 
];
echo "<br>";
```
####  Array walk recursive
```php

array_walk_recursive($arr_2d, function($value, $key){
    echo "In $key has $value<br>";
});


echo "<br>";
echo "<br>";
echo array_sum($number);
echo "<br>";
echo array_product($number);
echo "<br>";
echo array_reduce($number, function($a, $b){
    $a += $b;
    return $a;
});  

echo "<br>";
```
####  Array reduce
```php

echo array_reduce($number, function($a, $b){
    $a *= $b;
    return $a;
},1); 

// total er sathe 10 Plus
echo "<br>";
echo array_reduce($number, function($a, $b){
    $a += $b;
    return $a;
},10);
// total er sathe 10 Minus
echo "<br>";
echo array_reduce($number, function($a, $b){
    $a += $b;
    return $a;
},-10);

$letters = range("a", "z");
```
####  Array Chunk
```php


print_r(array_chunk($letters,5,true)); // array_chunk er third parameter true kore dile key gulu nosto hobe na
```
####  Array Slice
```php
print_r(array_slice($letters, 3, 5));
print_r(array_slice($letters, 3, 5, true)); // forth parameter true kore dile key gulu nosto hobe na
print_r(array_slice($letters, 3)); // prothom tin ta bad dibe
print_r(array_slice($letters, 3, true)); // shudhu tin number ta asbe
print_r(array_slice($letters, -3)); // shudhu sesher tin ta
print_r(array_slice($letters, 3, -2)); // prothom theke tinta ses theke duita bad 


// exponentiation oparator (**);

// array_walk - without loop you can get your data from an arrray
// array_walk_recursive - eta array_walk er motoi tobe eta mulitdimentional array er jonno o  kaj korbe
// array_sum - array er sob valuer jogfol
// array_product - arrray er sob valuer gunfol
```
#### arrray_column
```php
// arrray_column ekti array er kono column niye arekti array toiri korar jonno use kora jay
$students = [
    ["Name"=>"Habib", "Mobile"=>"01770", "address"=>"Dhaka"],
    ["Name"=>"Karim", "Mobile"=>"0177854", "address"=>"Khulna"],
    ["Name"=>"Siddique", "Mobile"=>"0186547", "address"=>"Chittagong"]
];
echo "<pre>";
$names = array_column($students,"Name");
$all = array_column($students,NULL); // second parameter null dile full array ta chole ase
$new_index = array_column($students,"Name", "address"); // third parameter take onno kono column diye dile sei column er value gulu new array er index hisabe kaj korbe
print_r($names);
print_r($all);
print_r($new_index);
```
#### To make a new array from multiple array. etate duitar array er kono index mile gele porer ta diye prothom ta override hoye jabe. override na korte chaile array_merge_recursive function use korte hobe 
```php
// 

$a = [1,2,"Habib",'khan',"bangladesh"]; 
$b = range(1,4);
$c = array_merge($a, $b); 
print_r($c); 
```
#### array_merge_recursive diye same index gulur value diye arekti array toiri hoy. eta array_merge e jeta override hoye jeto seta ekhane overide hobe na borong alada ekta array hoye jabe
```php
// 
$a1=array("a"=>"red","b"=>"green");
$a2=array("c"=>"blue","b"=>"yellow");

print_r(array_merge_recursive($a1,$a2));

echo "<br><br><br>";

$x = ["a", "b", "c"];
```
#### Array Push
```php
array_push($x, "d", "e"); // array er moddhe new value add korar jonno. eta array er sese value add hobe. surute add korar jonno array_unshift use korte hobe
print_r($x);
```
#### Array POP
```php
array_pop($x); // array er last element ta out kore dibe. prothom ta bad dewar jonno array_shift use korte hobe
print_r($x);
```
#### Array unshift
```php
array_unshift($x, "Hello", "bangladesh"); // array er surute new value add korar jonno
print_r($x);
```
#### Array shift
```php
array_shift($x); // array er prothom theke 1ta value bad dewar jonno array_shift use kora jay
print_r($x);
```
#### Array splice
```php
$inputs = ["red", 'green', 'blue', 'white', "pink"];
array_splice($inputs, 2); // prothom duita rekhe baki gulu bad
print_r($inputs);

$inputs = ["red", 'green', 'blue', 'white', "pink"];
// array_splice($inputs, 1, -1); // start r end value ta thakbe
// print_r($inputs); 

// array_splice($inputs, 3,0,"purple");
// print_r($inputs);

// array_splice($inputs,1,2);
// array_splice($inputs, 3,1,["a", "b", "c"]); // third parameter e joto dibe toto gulu remove korbe tarpor new value gulu add hobe, ekkhetre third parameter ta 0 dile kono value remove hobe na
// print_r($inputs);
```
#### Array diff
```php
$array_1 = ["a"=>"green", 1.00, "blue", "purple", "yellow"];
$array_2 = ["a"=>"green", "b"=>"1", "red", "blue", "yellow"];
// print_r(array_diff($array_1,$array_2)); // first parameter er je value ta second parameter e nai
// print_r(array_diff($array_2,$array_1));
```
#### Array diff sort
```php
print_r(array_diff_assoc($array_1,$array_2)); // key er defference ber korte chaile 
print_r(array_diff_key($array_1,$array_2)); // je key gulu pawa jabe na 2nd parameter er array te
```

```php
// echo "<pre>";
// $array_1 = ["a"=>"green", "c"=>"red", "blue", "d"=>"holud"];
// $array_2 = ["b"=>"GREEN", "c"=>"yellow", "red", "d"=>"holud"];
// print_r(array_intersect($array_1, $array_2)); // common value gulu ber korbe; first parameter er sathe second parameter er array ta k match koray tai first parameter er array er index gulu thik thake. eta case sensetive. case insensetive korte chaile array_uintersect() er third parameter e strcasecmp use korte hobe
// print_r(array_intersect_assoc($array_1,$array_2)); // key ebong valu duitai common thakle seta asbe
// print_r(array_intersect_key($array_1,$array_2)); // common key gulu asbe
// print_r(array_uintersect($array_1, $array_2, "strcasecmp")); // strcasecmp eta case insensetive kore check kore
```

