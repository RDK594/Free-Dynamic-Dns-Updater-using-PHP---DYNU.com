How to Install.

 Requirements :
 For Raspbian OS/DEBIAN :
 1.Install Apache server.
 2.Install MYSQL server.
 3.Install PHP
 
 Install XAMPP for Windows :
 https://www.apachefriends.org/download.html
 
 XAMPP for Linux :
 https://www.apachefriends.org/download.html
 
 Install XAMPP for OS X :
 https://www.apachefriends.org/download.html
 
 
 
 How to Implement.
 Note : Kindly create Dynamic DNS account using dynu->  http://dynu.com
 After creating  DYNU account
 
 1. Create database with name "noti"
 2. Import .sql file (available in extra folder).
 3. Goto folder(functions) and edit file(connection.php), change your hostname, username and password.
 4. In functions folder open "func.php" and edit line 45 . -> CURLOPT_URL => 'https://api.dynu.com/nic/update?hostname=[Your_Host_Name eg google.com]&myip=$ip&password=[your DYNU password in MD5 format]',
 Edit Your Hostname eg google.com or youtube.com and insert your http://dynu.com password[should be in MD5 format] in password field
 Save and exit.
 
  How to Convert your DYNU password in MD5 hash  format -
  link to convert password -> http://www.md5.cz/
  
  Example-
  Password  = HELLO
  Password[HELLO] in MD5  = eb61eead90e3b899c6bcbe27ac581660
  
  
  How to Execute PHP script automatically ?
  - Install Cron jobs [Search on google]
  - Create  2 cron Jobs [for every minute & for every Boot].
  
    Example - >
	* * * * * /path/to/php /var/www/ip/index.php
	
	NOTE- Always set cron job for index.php .
	
	#sorry for bad English ;-)
	
	For any questions write an email to 'iamrajneesh594@gmail.com'
	
	
