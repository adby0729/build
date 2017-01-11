#引用计数的概念

1.	变量的本质
2.	变量分离机引用 copy on write  && chang on write
3.	变量计数增减

#PHP回收周期


<?php 
class Person{ 
} 
function sendEmailTo(){ 
} 

$haohappy = new Person( );   
// 建立一个新对象:  引用计数    Reference count = 1 
$haohappy2 = $haohappy;       
// 通过引用复制:  Reference count = 2 
unset($haohappy);           
// 删除一个引用： Reference count = 1 
sendEmailTo($haohappy2);      
// 通过引用传递对象：   
// 在函数执行期间：
//  Reference count = 2 
// 执行结束后: 
// Reference count = 1 

unset($haohappy2);           
// 删除引用: Reference count = 0 自动释放内存空间

?>
