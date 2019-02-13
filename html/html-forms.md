# HTML 表单和输入
HTML 表单用于收集不同类型的用户输入。
## HTML 表单
单是一个包含表单元素的区域。  
表单元素是允许用户在表单中输入内容,比如：文本域(textarea)、下拉列表、单选框(radio-buttons)、复选框(checkboxes)等等。  
表单使用表单标签 `<form>` 来设置:
```html
<form>
.
input 元素
.
</form>
```
## HTML 表单 - 输入元素
多数情况下被用到的表单标签是输入标签（`<input>`）。  
输入类型是由类型属性（type）定义的。大多数经常被用到的输入类型如下：
### 文本域（Text Fields）
文本域通过`<input type="text">` 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域。
```html
<form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>
```
浏览器显示如下：  
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">  
**注意:**表单本身并不可见。同时，在大多数浏览器中，文本域的缺省宽度是20个字符。
### 密码字段
密码字段通过标签<input type="password"> 来定义:
```html
<form>
Password: <input type="password" name="pwd">
</form>
```
浏览器显示效果如下:  
Password: <input type="password" name="pwd">  
**注意:**密码字段字符不会明文显示，而是以星号或圆点替代。
### 单选按钮（Radio Buttons）
`<input type="radio">` 标签定义了表单单选框选项
```html
<form>
<input type="radio" name="sex" value="male">Male<br>
<input type="radio" name="sex" value="female">Female
</form>
```
浏览器显示效果如下:  
<input type="radio" name="sex" value="male">Male<br>
<input type="radio" name="sex" value="female">Female
### 复选框（Checkboxes）
`<input type="checkbox">` 定义了复选框. 用户需要从若干给定的选择中选取一个或若干选项。
```html
<form>
<input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
<input type="checkbox" name="vehicle" value="Car">I have a car 
</form>
```
浏览器显示效果如下:  
<input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
<input type="checkbox" name="vehicle" value="Car">I have a car 
### 提交按钮(Submit Button)
`<input type="submit">` 定义了提交按钮.  
当用户单击确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接收到的输入数据进行相关的处理。
```html
<form name="input" action="html_form_action.php" method="get">
Username: <input type="text" name="user">
<input type="submit" value="Submit">
</form>
```
浏览器显示效果如下:  
<form name="input" action="html_form_action.php" method="get">
Username: <input type="text" name="user"><input type="submit" value="Submit">
</form>  
假如您在上面的文本框内键入几个字母，然后点击确认按钮，那么输入数据会传送到 "html_form_action.php" 的页面。该页面将显示出输入的结果。

