# User Authentication Module for PHP & MySQL
This is a secure user authentication module for PHP applications. Making integration and configuration as easy and secure as possible. 

The inline comments will make sure you have all the information you need on what is happening in the code.

## How to integrate
First thing is to configure your database settings.
1. Create a database called 'tlauth'. If you want to change the name of the database, make sure to also change the name of the database in 'includes/db_config.php' file as well.
2. Import the sql script inside ‘includes/db_config/create.sql’ into your database to create the table with its respected attributes. If you create the table manually, again make sure you match what is in that sql file.
3. Go to ‘includes/db_config.php’ and set up your connection strings to your database management system.
4. If you have an email server, go to ‘includes/config.php’ and change your app url and email sender address.
5. Once you are finished setting up your database, put the following code down at the top of all the pages you want accessed by logged in users only
```php
session_start();
if (!isset($_SESSION['email'])) {
    header('Location: signin.php');
}
```
6. Just keep an eye on the in-line comments to get more clarity.
7. If you still have problems setting up this module, email me at omaops@gmail.com and I’ll see if I can help.

## File Structure
#### activate.php
#### forgot_password.php
#### index.php
#### README.md
#### reset.php
#### signin.php
#### signup.php
#### /images/loading.gif
#### /js/jquery-1.7.1.min.js
#### /js/jquery-1.7.1.min.js
#### /includes/db_config/create.sql
#### /includes/checkEmailExist.php
#### /includes/config.php
#### /includes/db_config.php
#### /includes/fnts.php
#### /includes/forgot_password.php
#### /includes/logout.php
#### /includes/reset.php
#### /includes/signin.php
#### /includes/signup.php