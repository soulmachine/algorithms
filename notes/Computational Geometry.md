#计算几何

##简单多面体
**定义**：对于一个多面体，如果它的表面能够连续地变形为一个球面，那么这样的多面体就叫做简单多面体，如长方体、棱柱等。

**欧拉公式**：对于简单多面体，有  
<center>**V-E+F=2**</center>
其中，V表示多面体的顶点数，E表示棱数，F表示面数。

##三角形的有向面积
	double area(double x0,double y0,double x1,double y1,double x2,double y2){
	    return x0*y1+y0*x2+x1*y2-x2*y1-x0*y2-x1*y0 ;
	}
上面得到的即是顶点为A(x0,y0),B(x1,y1),C(x2,y2)的三角形的有向面积S的两倍；

上面的公式比较难记，可以记它的行列式形式  
![](images/triangle.jpg?raw=true)

* 如果`area > 0`，则说明ABC三点呈现逆时针排列；
* 如果`area == 0`，则ABC三点共线；
* 如果`area < 0`，则说明ABC三点呈现顺时针排列。

这个定理：

* 计算三角形的面积。
* 判断点是否在三角形的内部。设待判断点为O，则点O在三角形ABC内部或边界上，当且仅当 S<sub>△ABC</sub>=S<sub>△OAB</sub>+S<sub>△OBC</sub>+S<sub>△OCA</sub>


