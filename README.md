
<!DOCTYPE html>
<html>
<head>
Store form data in .txt file
</head>
<body>
  <form method="post">
    Enter Your Text Here:<br>
    <input type="text" name="textdata"><br>

<input type="submit" name="submit">
    
  </form>
  <?php

if(isset($_POST['textdata']))
{
$data=$_POST['textdata'];
$fp = fopen('data.txt', 'a');
fwrite($fp, $data);
fclose($fp);
}
?>
</body>
</html>

