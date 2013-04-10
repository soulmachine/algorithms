这个notes文件夹下面，是我的一些算法笔记。

##刘汝佳，算法竞赛入门经典
###C/C++判断浮点数是否相等
P85 在判断两个浮点数a和b是否相等时，不要用`a==b`，应该判断二者之差的绝对值`fabs(a-b)`是否小于某个阀值，例如`1e-9`。

###三角形的有向面积
	double area(double x0,double y0,double x1,double y1,double x2,double y2){
	    return x0*y1+y0*x2+x1*y2-x2*y1-x0*y2-x1*y0 ;
	}
上面得到的即是顶点为A(x0,y0),B(x1,y1),C(x2,y2)的三角形的有向面积S的两倍；

上面的公式比较难记，可以记它的行列式形式  
|x0 y0 1|  
|x1 y1 1| = x0*y1+y0*x2+x1*y2-x2*y1-x0*y2-x1*y0  
|x2 y2 1|  

* 如果`area > 0`，则说明ABC三点呈现逆时针排列；
* 如果`area == 0`，则ABC三点共线；
* 如果`area < 0`，则说明ABC三点呈现顺时针排列。

这个定理：

* 计算三角形的面积。
* 判断点是否在三角形的内部。设待判断点为O，则点O在三角形ABC内部或边界上，当且仅当 S<sub>△ABC</sub>=S<sub>△OAB</sub>+S<sub>△OBC</sub>+S<sub>△OCA</sub>



