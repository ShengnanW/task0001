# task0001
ife/task0001-baidu




笔记：
:link伪类选择器是用来选中元素当中的链接。它将会选中所有尚未访问的链接，包括那些已经给定了其他伪类选择器的链接（例如:hover选择器，:active选择器，:visited选择器）。为了可以正确地渲染链接元素的样式，:link伪类选择器应当放在其他伪类选择器的前面，并且遵循LVHA的先后顺序，即：:link — :visited — :hover — :active。:focus伪类选择器常伴随在:hover伪类选择器左右，需要根据你想要实现的效果确定它们的顺序。




a:link {color: #FF0000}		/* 未访问的链接 */
a:visited {color: #00FF00}	/* 已访问的链接 */
a:hover {color: #FF00FF}	/* 鼠标移动到链接上 */
a:active {color: #0000FF}	/* 选定的链接 */


元素分类及特点：

           1.块级元素：

　　　　　在html中<div>、 <p>、<h1>、<form>、<ul> 和 <li>就是块级元素。设置display:block就是将元素显示为块级元素。块级元素特点：

 　　　　　（1）、每个块级元素都从新的一行开始，并且其后的元素也另起一行；（一个块级元素独占一行）

 　　　　　（2）、元素的高度、宽度、行高以及顶和底边距都可设置；

 　　　　　（3）、元素宽度在不设置的情况下，是它本身父容器的100%（和父元素的宽度一致），除非设定一个宽度。

　　    2.内联元素：

　　　　　 在html中，<span>、<a>、<label>、<input>、 <img>、 <strong> 和<em>就是典型的内联元素（行内元素）（inline）元素。当然块状元素也可 以通过代码display:inline将元素设置为内联元素。内联元素特点：

　　　　   （1）、和其他元素都在一行上；

 　　　　  （2）、元素的高度、宽度、行高及顶部和底部边距不可设置；

 　　　　  （3）、元素的宽度就是它包含的文字或图片的宽度，不可改变。

 　　　　　注意：为 a 元素设置了宽和高，但都没有起到作用，原因是a在默认的时候是内联元素，内联元素是不可以设置宽和高的。

 　　　 3.内联块状元素：

　　　　　　内联块状元素（inline-block）就是同时具备内联元素、块状元素的特点，代码display:inline-block就是将元素设置为内联块状元素。inline-block元素特点：

 　　　　　 （1）、和其他元素都在一行上；

 　　　　　 （2）、元素的高度、宽度、行高以及顶和底边距都可设置。

 　　　　　　注意：img是inline元素，但是他同时也是替换元素，他有着特殊的表现：

 　　　　　　　　　1. 可以设置width/height;

　　　　　　　　　 2. 默认的，img元素在屏幕占据的空间与其图片的实际像素一致，除非CSS有设置或者自身的width/height HTML 属性有设置；

　　　　　　　　　 3. 如果img标签的包裹元素为也为inline元素，则img的边界可以超出其直接父元素的边界，直到自己的宽、高达到最大或者设定值为止，而且文档流中img的兄弟元素也不能遮盖住img。最常见的就是<a>里面包含的<img>；

　　　　　　　　　 4. 所以从行为上看,img元素作为替换元素，有着类似于Inline-block的行为，尽管在SPEC里面，他的确是一个inline元素。

