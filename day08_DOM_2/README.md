

# ��� #

1. getElementsByTagName
2. Ӧ�ð���
3. �������ʽ


# �������� #

## getElementsByTagName ##

getElementsByTagName����ͨ����ǩ���õ�Ԫ�أ��õ�����ҳ�������и��ֱ�ǩԪ�أ��õ��������飬����������±꣬��ʼ��0�����һ����.length-1


```
1	var ops = document.getElementsByTagName("p");
2	ops[0].style.backgroundColor = "rgb(111,222,123)";
3	ops[3].style.backgroundColor = "rgb(111,222,123)";
4	ops[ops.length - 1].style.backgroundColor = "rgb(111,222,123)";
```

### ѭ����� ###
ѭ�����������е�Ԫ��

### ����������get ###

��ȥѡ��һ��HTML��ǩ��Ȼ��ѡ�����HTML��ǩ�е�����p��ǩ��
```
var ps = document.getElementById("box2").getElementsByTagName("p");

```

��������������
```
document.getElementsByTagName("div")[1].getElementsByTagName("p")[2].getElementsByTagName("span")[1].style.color = "red";

```


## Ӧ�ð��� ##

#### ���б�ɫ ####

��ȥѡ��һ��HTML��ǩ��Ȼ��ѡ�����HTML��ǩ�е�����p��ǩ��
	var ps = document.getElementById("box2").getElementsByTagName("p");

��Ҫ��дһ��document
	var ps = document.getElementById("box2").document.getElementsByTagName("p");


```
<style>
.red{background:red;}
</style>


<ul id="ul01">
	<li>A</li>
    <li>B</li>
    <li>C</li>
    <li>D</li>
    <li>E</li>
    <li>F</li>
</ul>

```

#### ȫѡ��ѡ�� ####

```

<div id="box">
  <p><input type="checkbox">�Է�</p>
  <p><input type="checkbox">�Է�</p>
  <p><input type="checkbox">�Է�</p>
  <p><input type="checkbox">�Է�</p>
  <p><input type="checkbox">�Է�</p>
  <p><input type="checkbox">�Է�</p>
</div>

<input type="button" value="ȫѡ" id="btn">
```


#### ������Ӽ��� ####

��������ɫ

```
  <style>
    p{
      width: 60px;
      height: 60px;
      float: left;
      margin-right:20px;
      background-color: yellowgreen;
    }
  </style>

<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>

```

##### ��Ӧģ�� #####

##### ����ģ�� #####

### �����ж�ɫ��С��Ϸ�� ###



## �������ʽ ##

��������ֻ�ܵõ����ڵ���ʽ����ʵ��DOM�ṩ�˿ɿ���API���õ���������ʽ��


W3C�ƶ��ı�׼API�������ִ������������IE9����������֮ǰ�İ汾����ʵ����window.getComputedStyle()���÷�������һ��Ҫ������ʽ�����Ԫ�أ�������һ����ʽ������ʽ�����ṩ��һ����ΪgetPropertyValue()�ķ��������ڼ����ض���ʽ���Եļ�����ʽ��getPropertyValue��������css�������ƣ��������շ�ʽ�����ơ�getPropertyValue()���Բ�д��ֱ���÷���������������Ҳ���ԡ�

get�õ���computed�����style��ʽ
get�õ���property���ԣ�vauleֵ
���磺
	window.getComputedStyle(oDiv).getPropertyValue("width")




### ������� ###

����ʹ��ͨ�÷�����ʵ�ڲ����ٿ����������ⷽʽ��ʵ��


#### �������� ####

����������
http://www.jianshu.com/p/fd11fda302c4

��������
http://xhyujian.blog.51cto.com/1582574/1123490

�ͻ��˼��
http://www.cnblogs.com/egger/archive/2013/04/26/3045285.html



### ͸���� ###

����IE8�����ڰ汾��֧��opacity��ͨ��style.opacity����ele.currentStyle.opacity����ȡֵʱ�����ص���Ȼ��opacityֵ����ʹ�������ȫ������opatityֵ������һ�����¶����������ܹ���֤opactiy��filter�����õ�������һ�µģ���JavaScript��ȡopactiyֵ�����Ǽ��ݵġ�


http://www.cr173.com/html/7817_1.html


```
	<style type="text/css">
		div{
			width: 200px;
			height: 200px;
			background-color: black;
			opacity: .2;
			filter:alpha(opacity=20);
		}
	</style>
```
# ��ҵ #
1. �ѽ����ص㰸����д��
	���ֲ�ͼ��ѡ��������б�ɫ��ȫѡ���������ʽ�����ӣ�

2. ����Ч��
    ![](hw1.jpg)



### ѡ�� ###

�����ж�ɫ ��С��Ϸ��

����չ�� ���ʱ�༭

