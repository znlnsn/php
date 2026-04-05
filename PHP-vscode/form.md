```php
<form action="login.php" method="POST"> <label for="username">用户名：</label> <input type="text" id="username" name="username" required><br><br> <label for="password">密码：</label> <input type="password" id="password" name="password" required><br><br> <input type="submit" value="登录"> </form>
```
1. `<form>`: 这是我们的表单元素的容器。
2. `action="login.php"`: 这告诉表单提交时将数据发送到哪里。
3. `method="POST"`: 这指定了如何发送数据（POST对密码更安全）。
4. `<input>`: 这些是用户输入信息的字段。
5. `type="password"`: 这在输入时隐藏密码。
6. `required`: 这确保用户不能在不填写这些字段的情况下提交表单。