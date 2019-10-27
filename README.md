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

## 6. Object Oriented Programming...



#####Class − 
classes contain the data members and member functions

#####Object − 
instances of classes

#####Member Variable − 
These are the variables defined inside a class. 

#####Member function − 
These are the function defined inside a class and are used to access object data.

#####Inheritance − 
Child class will inherit all or few member functions and variables of a parent class.

#####Parent class − 
A class that is inherited from by another class. This is also called a base class or super class.

#####Child Class − 
A class that inherits from another class. This is also called a subclass or derived class.

#####Final Class - 
Whom no class can not inherit from other class.

#####Polymorphism − 
Function name will remain same but it take different number of arguments and can do different task.

#####Data Abstraction − 
Any representation of data in which the implementation details are hidden (abstracted).

#####Encapsulation − 
Encapsulation is an Object Oriented Programming concept that binds together the data and functions that manipulate the data, and that keeps both safe from outside interference and misuse

#####Constructor − 
Constructor is involved when object are Created

#####Destructor − 
Destructor is involved when object are deleted.

#####Traits
Traits are a mechanism for code reuse in single inheritance languages such as PHP.

#####Access privilage/visibilty of Class method and property
-Public
- Protected (Class and his child class will be able to use this)
- Private (Only for own use)

#####:: Scope Resolution
When we access  static property and constant then we have to use Scope Resolution.
- outside of class [ClassName::property]
- inside of class [self::property]

#####Object Handler 
The variable that the object is placed in is called the object handler

#####Rule of OOP
- Is not mandatory give parentheses [()] end of the class 
- You do not have to give $ when using a class property

```php
class myClass{
    public $a = "Hello world";
    static $c = "Tai";
}
$obj = new myClass;
echo $obj->a;
echo myClass::$c;
```
- The value of private or protected property can be used for the following uses:
```php
class test{
    Private $d;
    public function setvalue($a){
        $this->d = $a;
    }
    public function getvalue(){ 
        return $this->d;
    }
}
$test_obj = new test;
$test_obj->setvalue(10);
echo $test_obj->getvalue();
```

#####Chain method 
```php
class Person {
    private $name;
    private $age;

    //Set Method
    public function setName($name){
        $this->name =$name;
        return $this;
    }

    //Set Method
    public function setAge($age){
        $this->age =$age;
        return $this;
    }

    //Get Method
    public function getInfo(){
        return 'Welcome to '.$this->name.' and his age is '.$this->age;
    }
}

$obj = new Person;
echo $obj->setName('Khayrul')->setAge(27)->getInfo();
```

#####Magic method
```php
class Person {
    private $name;
    private $age;

    //Set Method
    public function __construct($name, $age){
        $this->name = $name;
        $this->age = $age;
        echo 'Hello<br/>';
    }


    public function person(){
        echo 'Show Person';
    }

    //delete Method
    public function __destruct(){
        echo "Bye Bye";
    }

    //Get Method
    public function getInfo(){
        echo 'Welcome to '.$this->name.' and his age is '.$this->age;
    }

}

$obj = new Person('Khayrul',32);
$obj->getInfo();
```

#####BD Connection
```php
class Db{

	private $conn;
	private $rows;
	private $table;

	public function __construct($host,$user,$pass,$db){
			$this->conn=new mysqli($host,$user,$pass,$db);
			if($this->conn->connect_errno){
				die("Connection Fail: ".$this->conn->connect_error);
			}
	}

	public function getAll($table,$cols){
		$sql="SELECT $cols FROM $table";
		$result=$this->conn->query($sql);
		if($result->num_rows>0){
			$this->rows= $result->fetch_all(MYSQLI_ASSOC);
			return $this;
		}
		return false;
	}

	public function getTable(){
		$this->table="<table border=\"1\" width=\"500\" cellpadding=\"5\">";
		$this->table.="<tr>";
			foreach($this->rows[0] as $col=>$val){
				$this->table.="<th>".ucfirst($col)."</th>";
			}
		$this->table.="</tr>";
		reset($this->rows);
		foreach($this->rows as $student){
			$this->table.="<tr>";
				foreach($student as $value){
					$this->table.="<td>$value</td>";
				}
			$this->table.="</tr>";
		}

		$this->table.="</table>";
		return $this->table;
	}
}

$db=new Db("localhost","root","","php86");
echo $db->getAll("users","*")->getTable();
```
##### Abstract Class
```php
abstract class Replica{
    abstract function getName($name);
    abstract function getInfo($age);
}


class Child extends Replica{

    public function getName($name)
    {
        return $this->name = $name;
    }
}


$obj = new Child();
echo $obj->getName(4545);
```

##### Interface 
```php
interface myInterface
{
    public function amethod($s);
    public function sum($x, $y);
}


interface yourInterface
{
    public function mul($m, $n);
}


class MyClass implements myInterface, yourInterface 
{
    public function amethod($s) 
    {
        return $this->name = $s;
    }

    public function sum($a, $b)
    {

    }

    public function mul($a, $b)
    {
        
    }
}


$obj = new MyClass;
echo $obj->amethod('Khayrul');
```

#####Method Over Loading 
```php
class MethodOverLoading{
    public function __call($methodName, $params){
        echo $methodName, '</br>';
        print_r($params);
    }

    public static function __callStatic($methodName, $params){
        echo $methodName, '</br>';
        print_r($params);
    }
 
}


$obj = new MethodOverLoading;
//$obj->sum(5,7,"helllo");
MethodOverLoading::test(4,5,3,'Hello');
```

##### Property Overloading 
```php
<?php

class PropertyOverLoading{

    private $data = [];

    public function __set($name, $value){
         echo "Your Property : $name</br>";
        echo "And yor value is: $value";
    }

    
    /**** Property over loading */   
    //property set ....
    // public function __set($name, $value){
    //     $this->data[$name] = $value;
    // }


    //Property get ....
    public function __get($property){
        if(array_key_exists($property, $this->data))
            return $this->data[$property];
    }


    //Property get ....
    // public function __get($property){
    //     if(array_key_exists($property, $this->data))
    //     return $this->data[$property];
    // }


    // Property exist Check .....
    public function __isset($prop){
        echo isset($this->data[$prop])?"Yes":"No";
    }

    
    // Property unset ....
    public function __unset($prop){
        unset($this->data[$prop]);
    }

}

$obj = new PropertyOverLoading;
$obj->jan=50;

unset($obj->jan);

$j= isset($obj->jan);
echo $j;

function pr($d){
    echo '<pre>';
    print_r($d).'';
    exit;
}

```

##### Autoload

```php

class Books{
    public $booksName;
    public $author;

    public function __construct()
    {
        echo "Welcome from books class ";
    }
}

class Member{
    public $name;
    public $email;

    public function __construct()
    {
        echo "Welcome from member class ";
    }
}




function loadClass($className){
    include_once("$className.php");
}

spl_autoload_register("loadClass");

$obj = new Member;
$obj->name = "Md. Khayrul Hasan";
echo $obj->name, '</br>';

$obj1 = new Books;
$obj1->booksName = "PHP";
echo $obj1->booksName, '</br>';

```

##### Clone 

```php
class coppy{

    public $name;
    private $mobile;

    public function __construct($name, $mobile){
        $this->name = $name;
        $this->mobile = $mobile;
    }

    
    public function __clone()
    {
        $this->mobile = "12121254";
    }

}


$obj = new coppy("Khayrul", "54545");

$obj1 = clone $obj;

$obj1->name = "Tarek";
echo '<pre>';
print_r($obj);

echo "<br/>";
echo '<pre>';
print_r($obj1);
```

#####Serialize Object
- Serialize : The process of converting a object to specific formatted string is called object serialized.
- Un serialize : The process of converting a specific formatted to object is called un serialized.
```php
class Member {

    public $username;
    public $age=15;
    public $logedIn= false;
    
    public function login(){
        $this->logedIn = true;
    }

    public function logout(){
        $this->logedIn = false;
    }

    public function isloggedIn()
    {
        return $this->logedIn;
    }

    // It call while call serialize() function
    public function __sleep()
    {
        return ["username", "age"];
    }

    // It call while call unserialize() function
    public function __wakeup()
    {
        return "check bangla";
    }

}


$obj = new Member();

$obj->username = 'Khayrul';

$obj->login();

$memberString = serialize($obj);

echo '<pre>';
echo $memberString;

echo '</br>';

$onstring = unserialize($memberString);

echo $onstring->username;
```

##### Trait 

- bar.php
```php
trait Bar{
	public function sayHello(){
		return "Hello";
	}

	public function sayWorld(){
		return "Hello bar";
	}
}
```
- index.php
```php

include("bar.php"); // file name
class foo{
	use bar; // trait name
	function sayWorld(){
		return "Hello Hiiiiii..........";
	}
}

$obj = new foo;
echo $obj->sayWorld();
```
##### Object or Array to convert to JSON
```php
class Fruits{
	public $a, $b, $c;
}

$obj = new Fruits;

$obj->a = "mango";
$obj->b = "banana";
$obj->c = "Jakefruit";

$alfa = ['a', 'b', 'c'];
$han = json_encode($alfa, JSON_FORCE_OBJECT); //php array, convert to json obj 
echo $han;

$str = json_encode($obj);

echo $str, '<br/>';

$obj2 = json_decode($str); // revert to php object

$obj3 = json_decode($str, true); // revert to php array by enable second parametter.
echo '<pre>';
print_r($obj2);

echo '<br>';

print_r($obj3);
```

#####  JSON convert to Object or Array

- student.json
```json
[
	{
		"name" : "Mamun",
		"mobile" : "019445545"		
	},{
		"name" : "Khayrul",
		"mobile" : "017454545"
	},{
		"name" : "Saniad Hossen",
		"mobile" : "01845"
	}
]
```
- index.php
```php
$data = file_get_contents('students.json');
echo '<pre>';
print_r(json_decode($data));
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>

<?php
// csv = comma seperated value

$str = "Hello Bangladesh I Love You, and I want you";
echo strlen($str);
echo "<br>";
// print_r(count_chars($str));
// print_r(count_chars($str, 1));

foreach(count_chars($str, 1) as $k=>$v){
    echo "<b>" . chr($k) . "</b> Character have " . $v . " times in the string <br>";
}

echo "<br>";
echo count_chars($str, 3); // jesob character use hoiche

echo "<br>";
echo count_chars($str, 4); // jesob character use hoinai

echo "<br>";
echo strlen(count_chars("", 4)); // 

echo "<br>"; 
echo str_word_count($str, 0); // word count of a string. it may be done by explode
echo "<br>";
echo count(explode(" ", $str));


echo "<br>";
print_r(str_word_count($str, 1)); // string to array convertion
echo "<br>";
print_r(explode(" ", $str)); // explode diye


echo "<br>";
print_r(str_getcsv($str));
echo "<br>";
print_r(str_getcsv($str, ","));
echo "<br>";
print_r(str_getcsv($str, " "));
print_r(str_word_count($str, 2)); // word ti joto number character theke shuru hoiche seta oi word er index hishabe dekhabe
echo "<br>";
print_r(str_split($str)); // array to string conversion by character
echo "<br>";
echo "<br>";
print_r(str_split($str,4)); // str_split er second parameter joto dibo toto character niye array  
echo "<br>";
echo wordwrap($str, 22, "<br>"); // ek line 20 character kore thakbe. 21 character hole last word ti niche chole jabe
echo "<br>";
echo "<br>";
echo wordwrap($str, 22, "<br>", true);
echo "<br>";
echo "<br>";

$strr = "This is a test is an is is";

echo substr_count($strr, "is"); // count in total string
echo "<br>";
echo "<br>";
echo substr_count($strr, "is", 8); // count after 8 character
echo "<br>";
echo substr_count($strr, "is", 8, 12); // count after 8 up to 12 character means after 8 character to 4


?>


</body>
</html>
```



```php
//string
echo '<pre>';

$str = "My sodnar bangla , I love you My sod-nar bangla , I love you My sodnar bangla ,I love you";

//echo strlen($str), '</br><pre>', print_r(count_chars($str));

// foreach(count_chars($str, 3) as $k =>  $v){
//     echo '<b>'.chr($k)."<br>char have ".$v."times <br>";
// }

//print_r(str_word_count($str, 1));

//print_r(str_word_count($str, 2));

//print_r(str_split($str));

//print_r(wordwrap($str, 20, '<br>'));

//print_r(wordwrap($str, 20, '<br>'));

//print_r(wordwrap($str, 20, '<br>', TRUE));

//print_r(wordwrap($str, 20, '<br>', TRUE));

//echo substr_count($str,'My');

echo substr_count($str,'My', 0, 12);

```

##### Password Hashing 
```php
// $bangla = sha1(1);
// $bangla1 = (1);

// echo strlen($bangla), '<br/>',strlen($bangla1), '<br/>';

// echo strlen($bangla), '<br/>',strlen($bangla1), '<br/>';

// hashing method... 
// $hased = crypt('12345', 'khayrul');

// if(hash_equals($hased, crypt('12345', 'khayrul'))){
//     echo "Mash";
// }else{
//     echo "Not Mashed";
//}


// Password hasing api================================
// echo password_hash("123456", PASSWORD_DEFAULT);

// $hased = '$2y$10$QjTSd2C3PtfkMyOmTpUi9.r4AzXf2TEdZguuyBE8F2t6OVn8YkDiy';

// if(password_verify('123456', $hased)){
//     echo "<br/>","varifiyed";
// }

$option = ['cost'=>20];
echo password_hash('12233', PASSWORD_BCRYPT, $option);
```

##### Encoding and decoding 


```php
<?php
/*
|---------------------------------------------------
| PHP String Class - 02
|---------------------------------------------------

1. diff freze -> all deleted after restart pc
2. extension=php_openssl.dll eta active thakte hobe. means er age semi clone thaka jabe na.
3. caesar cipher algorithm

*/

echo "<pre>";
//print_r(openssl_get_cipher_methods());

$str = "I love PHP";
$cipher = "aes-128-gcm";
//$cipher = "AES-128-XTS";
$lenth = openssl_cipher_iv_length($cipher);
echo $lenth;
echo "<br>";
$randByte = openssl_random_pseudo_bytes($lenth);
echo $randByte;
echo "<br>";
$key = "w3";
$cipherText = openssl_encrypt($str, $cipher, $key, $options = "0", $randByte, $tag);
echo $cipherText;
echo "<br>";

echo $original_text = openssl_decrypt($cipherText, $cipher, $key, $options="0", $randByte, $tag);

echo "<br>";
echo "<br>";

/*
|---------------------------------------------------
| Encoding decoding in PHP
|---------------------------------------------------

1. Blob

*/

$bas64 = base64_encode($str);
echo base64_decode($bas64);

echo "<br>";
$img = "legendit.jpg";
$type = mime_content_type($img);
//echo file_get_contents($img);
//echo base64_encode(file_get_contents($img));
$encode_img =  base64_encode(file_get_contents($img));
//echo base64_decode($encode_img);
$src = 'data: '.$type.';base64,'.$encode_img;

//echo $src;

//echo "<img src='". $src ."'>";

echo convert_uuencode("Hello mr. Habib Khan"); // another encoding system
echo "<br>";
echo convert_uudecode(convert_uuencode("Hello world"));
```







 




