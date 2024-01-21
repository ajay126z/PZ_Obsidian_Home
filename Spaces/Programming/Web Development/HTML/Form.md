---
created: 2024-01-21T01:00
updated: 2024-01-21T01:06
---
Write a registration form in HTML.<!DOCTYPE html>
<html>
<head>
	<title>Registration Form</title>
</head>
<body>

	<h1>Registration Form</h1>

	<form action="#" method="POST">
		<label for="firstName">First Name:</label><br>
  		<input type="text" id="firstName" name="firstName"><br>

  		<label for="lastName">Last Name:</label><br>
  		<input type="text" id="lastName" name="lastName"><br>

  		<label for="email">Email:</label><br>
  		<input type="email" id="email" name="email"><br>

  		<label for="password">Password:</label><br>
  		<input type="password" id="password" name="password"><br>

  		<label for="confirmPassword">Confirm Password:</label><br>
  		<input type="password" id="confirmPassword" name="confirmPassword"><br><br>

	  	Gender:<br>
	  	<input type="radio" id="male" name="gender" value="male">
	  	<label for "male">Male</label><br>

	  	<input type ="radio"id ="female"name ="gender"value ="female">
	  	<label for "female">Female</label><br>

	  	Date of Birth:<br>
	  	  <input type = "date"name = "dob"><br><br>

	  <input type = "submit"value = "Submit">
	  <input type = "reset"value = "Reset">

   </form> 
</body> 
</html> 