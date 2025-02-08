PHP - Hypertext Preprocessor - Server side scripting language designed for web development.

It allows to create dynamic and interactive web pages by embedding PHP code within html.

PHP is an open source language.

Syntax is similar to C, Java and Perl.

PHP was created by Rasmus Ledorf in the 1990s.

Purpose of PHP is to process hypertext or web pages.

Main Features of PHP is its integration with HTML.

PHP has a vast and comprehensive standard library, known as the PHP Extension and Application Repository(PEAR).

PHP has cross-platform compatibility.

It can run on various operating systems, including Windows, macOS, and Linux.

PHP can handle form data, validate user input, perform actions based on user interactions

PHP can connect to different databases to retrieve or store data, making it easy to create dynamic and interactive webistes.

PHP allows you to manage sessions.

PHP provides functions to handle files, such as uploading, downloading and manipulating the data stored in files.

PHP has built-in error handling mechanisms, allowing developers to identify and handle errors.

Popular PHP frameworks are Laravel, symphony, and CodeIgniter.

PHP has builtin security features to help protect websites from SQL injections and XSS attacks.

JavaScript is a client side scripting language used to add interactivity, validate forms, handle events, and perform various actions on the users web browser.

**How to connect PHP with a MYSQL DATABASE:**

1) USING MYSQLI Object-Oriented:

```
<?php
$servename = "localhost";
$username = "username";
$password = "password";
$db = "your_database_name";

//Create a connection
$conn = new mysqli($servername, $username, $password, $db);

//check connection
if ($conn->connect_error){
  die("Connection failed: ".$conn->connect_error);
}
echo "Connected Successfully";
?>
```
2) USING  MYSQLI PROCEDURAL:

```
<?php
$servename = "localhost";
$username = "username";
$password = "password";
$db = "your_database_name";

//Create a connection
$conn = mysqli_connect($servername, $username, $password, $db);

//check connection
if ($conn->connect_error){
  die("Connection failed: ".$conn->connect_error);
}
echo "Connected Successfully";
?>
```
3) USING PDO:

```
<?php
$servername = "localhost";
$username = "username";
$password = "password";
try {
  $conn = new PDO("mysqk:host=$servername; dbname=myDB", $username, $password);
  // set the PDO error mode to exception
  $conn->setAtrribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
  echo "Connected Successfully";
}catch(PDOException $e) {
  echo "Connection Failed: ". $e->getMessage();
}
?>
```

**TO CLOSE THE CONNECTION:**

1) USING MYSQLI OBJECT-ORIENTED:

```$conn->close();```

2) USING MYSQLI PROCEDURAL:

   ```mysqli_close($conn)```

3) USING PDP:

   ```$conn = null```
   
PHP work with MYSQL database using:
1) MYSQLi extension (the "i" stands for imporved)
2) PDO (PHP Data Objects)

**HOW TO INCLUDE INFORMATION OF A PHP FILE IN ANOTHER PHP FILE:**

1) INCLUDE: This statement takes all the text/code that exists in the specified file and copies it into the file that uses the include statement.

2) REQUIRE: The require() function performs same as the include() function. It also takes the file that is required and copies the whole code into the file from where the require() function is called.

**Difference between INCLUDE() and REQUIRE():**

If we dont have file named what we included in the include() and require() function then 

1) require will produce a fatal error (E_COMPILE_ERROR) and stop the script.

2) include will only produce a warning (E_WARNING) and the script will continue

