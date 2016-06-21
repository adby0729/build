#命名空间分类 
1.	非限定类、函数或常量名称

		<?php
		nanmespace A\demo;
		class Exception extends \Exception {}
		$a = new Exception();//$a 是A\demo\Exception 的一个对象
		?>

2.	完全限定类、函数或常量名称

		$a = new \Exception();//$a是\Exception 的一个对象 
