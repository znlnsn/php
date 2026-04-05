```php
<?php

$username = $_POST['username'];;

$pw =$_POST['pw'];;

$conn = mysqli_connect("localhost", "root", "root", "znlnsn");

  

// 检查连接是否成功

if (!$conn) {

    // 输出具体的错误信息

    die('数据库连接失败: ' . mysqli_connect_error());

}

  

// user，pass数据库内，username和pw是HTML

$sql = "INSERT INTO info (user, pass) VALUES ('$username', '$pw')";

$result = mysqli_query($conn, $sql);

  

if($result) {

    echo "<script>alert('数据插入成功');</script>";

}

else {

    // 修正错误输出方式

    echo "<script>alert('数据插入失败: " . mysqli_error($conn) . "');</script>";

}

mysqli_close($conn);

?>
```