### 一，这是个什么玩意？
这是一个复选框选择插件，基于jQuery，方便开发者在管理后台的信息列表页实现自动选、全选、反选、全不选、shift选等功能。
### 二，到底怎么使用
很简单，第一步，引入jQuery类库，第二步引入本插件，第三步，指定实现按钮（+回调函数）
###三，给我个示例代码看看
####  1，js代码
```javascript
	<script src="js/jquery-1.11.3.min.js"></script>
	<script src="js/jquery.check.js"></script>
	<script type="text/javascript">
	;$(function(){
		$('[data-check]').check('input[name=id]');
	});
  	</script>
  ```
####  2，html代码
  ```html
	<a href="" data-check="yes">全选</a>
	<a href="" data-check="no">全不选</a>
	<a href="" data-check="reverse">反选</a>
	<hr />
	<input type="checkBox" data-check="" />自动选择
	<input type="button" data-check="" value="自动选择" />
	<hr />
	<input type="button" value="全选" data-check="yes" />
	<input type="button" value="全不选" data-check="no" />
	<input type="button" value="反选" data-check="reverse" />
	<hr />
	
	<ul>
		<li><input type="checkbox" name="id" value="0" />这是第 0 条信息</li>
		<li><input type="checkbox" name="id" value="1" />这是第 1 条信息</li>
		<li><input type="checkbox" name="id" value="2" />这是第 2 条信息</li>
		<li><input type="checkbox" name="id" value="3" />这是第 3 条信息</li>
		<li><input type="checkbox" name="id" value="4" />这是第 4 条信息</li>
		<li><input type="checkbox" name="id" value="5" />这是第 5 条信息</li>
		<li><input type="checkbox" name="id" value="6" />这是第 6 条信息</li>
		<li><input type="checkbox" name="id" value="7" />这是第 7 条信息</li>
		<li><input type="checkbox" name="id" value="8" />这是第 8 条信息</li>
	</ul>

  ```
###这到底是什么意思
####  用法1
$(按钮选择符).check(被操作input选择符);
如：
```javascript
	$('#div1 input:button').check('#form1 input[name=id]');
```
####  用法2
$(按钮选择符).check(被操作复选框选择符,回调匿名函数);
```javascript
	$('#div1 input:button').check('#form1 input[name=id]',function(checkbox){
		alert('你当前操作的按钮是' + $(this));
		alert('被操作的复选框总计' + checkbox.length + '个');
	});
```
####  其他
在响应的按钮上添加自定义属性data-check，并为其设定不同的属性值来区分该按钮的作用
如：
  ```html
	<input type="button" value="全选" data-check="yes" />
	<input type="button" value="全不选" data-check="no" />
	<input type="button" value="反选" data-check="reverse" />
	<input type="button" value="自动选择" data-check="" />
  ```
###你是干什么的？
别问我是谁，请叫我偶喷讷，具体联系方式请查阅：http://www.xuqingkai.com
