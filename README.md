<?php
echo date("Y/m/d") . "\n";
echo date("y.m.d") . "\n";
echo date("d-m-y")."\n";
?>



 1] How can we get second of the current time using date function?

  ans:
  <?php 
  echo date("s");
  echo "second includes this cureent time";
  ?>

 2]  What are the usase of explode() & Implode()functions? give examples?
 ans :
      
<?php  
$arr=array ('I','am','simple','boy!');  
echo implode(" ",$arr);  // I am simple boy!
?>  

<?php  
$str="I am simple boy!";  
print_r(explode(" ",$str)); // Array([0]=>I [1]=>am [2]=>simple [3]=>boy!) 
?>  

3] What is the deffernce between unset and unlink?
ans: Both the function are used to do some undo operations but used in different situations cause both acts differently.
The unlink() function is used when you want to delete the files completely. 
The unset() Function is used when you want to make that file empty and so on variable,araray etc.
 
 4] what is str_replace()?
 ans:
 <?php
 Input:  $subjectVal  = "It was nice meeting you. May you shine brightly."
        str_replace('you', 'him', $subjectVal)
Output: It was nice meeting him. May him shine brightly.

Input:  $subjectVal  = "You eat fruits, vegetables, fiber every day."
        $searchVal = array("fruits", "vegetables", "fiber")
        $replaceVal = array("pizza", "beer", "ice cream")
        str_replace($array1, $array2, $str)
Output: You eat pizza, beer, ice cream every day.
 
 ?>
 
 5] How can we change the time zones in PHP?
 ans:
 <?php 
  
// Set timezone 
date_default_timezone_set('Asia/Kolkata'); 
  
// Create  
$timezone_object = date_default_timezone_get(); 
  
// Compare the timezone with ini-set timezone 
if (strcmp($timezone_object, ini_get('date.timezone'))){ 
    echo 'Script timezone differs from ini-set timezone.'; 
} else { 
    echo 'Script timezone and ini-set timezone match.'; 
} 
?> 

6] Write the PHP code which will print sum of digit? {eg. 123=6,596=20}
ans:
<?php  
$num = 14597;  
$sum=0; $rem=0;  
  for ($i =0; $i<=strlen($num);$i++)  
 {  
  $rem=$num%10;  
   $sum = $sum + $rem;  
   $num=$num/10;  
  }  
 echo "Sum of digits 14597 is $sum";  
 ?>  
 
 7] What is the syntax to send the mail in PHP?
 ans: 
 <?php
         $to = "xyz@somedomain.com";
         $subject = "This is subject";
         
         $message = "<b>This is HTML message.</b>";
         $message .= "<h1>This is headline.</h1>";
         
         $header = "From:abc@somedomain.com \r\n";
         $header .= "Cc:afgh@somedomain.com \r\n";
         $header .= "MIME-Version: 1.0\r\n";
         $header .= "Content-type: text/html\r\n";
         
         $retval = mail ($to,$subject,$message,$header);
         
         if( $retval == true ) {
            echo "Message sent successfully...";
         }else {
            echo "Message could not be sent...";
         }
      ?>
      
      8] what will be the output
       
$num = 10;
function multiply()
{
$num = $num * 10; 
}
multiply();
echo $num;
       ans: 10
       
9] What is the output
$str1="devloper@letsknowit.com";
$str2=strchar($str1,'@',true); //this is wrong function
$str2=strchr($str1,'@',true); // this is the right function
echo $str2;
ans: devloper    //before string print  for @

10] What is the differenc between PRIMARY KEY and UNIQUE KEY?
ans:
Primary key will not accept NULL values whereas Unique key can accept one NULL value. 
 A Clustered index automatically created when a primary key is defined whereas Unique key generates the non-clustered index.
  
11] Which are Aggregate function in mysql?
ans : An aggregate function performs a calculation on multiple values and returns a single value. (e.g -avg())

12] write my sql query to fetch employee names having salary greater than 10000 and less than 25000 table employee

13] write mysql query to display top 20 records display on table employee
ans : 
SELECT *  
    FROM employees  LIMIT 20;

14] write mysql query to fetch employee names  from employee table in upper case 
ans : SELECT UPPER(first_name) 
   FROM employees;
   
15] write mysql query to fetch unique mobile from table employee  
 ans :
 SELECT DISTINCT emp_mobile 
	FROM employees;
