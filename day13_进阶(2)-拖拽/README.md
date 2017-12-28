
# ��� #

1. ���ھ�
2. ��ֹ�����Ĭ����Ϊ
3. ��ק


# �������� #

## ���ھ� ##

```

// ���ڸı���¼���ʡ����window����
onresize = onload = onscroll = move;

// ��ȡ��ǰ��������λ��
var iScrollTop = document.documentElement.scrollTop || document.body.scrollTop;
```

## ��ֹ�����Ĭ����Ϊ ##

### ��ֹ������ת ###

```
���У� evt Ϊ�¼�����

// ��ֹ�������Ĭ����Ϊ�ļ���д��
evt.preventDefault ? evt.preventDefault() : evt.retrunValue = false;


������ Firefox��chrome �����������֯��Ĭ����Ϊ
evt.preventDefault()


// ������ IE ���������ֹĬ����Ϊ
evt.retrunValue = false

```


### �Զ����Ҽ��˵� ###

1. �Ҽ�����ʾ�˵�
2. ����հ�λ��ȡ���˵�
3. ����˵����ݲ���ʧ




## ��ק ##

![](tz.png)


### ����������קЧ�� ###

����ƶ������У�Ҫ��ֹ��Ĭ�ϵ�ѡ��״̬

```
var offsetX = e.offsetX ? e.offsetX : e.clientX - box.getBoundingClientRect().left;
var offsetY = e.offsetY ? e.offsetY : e.clientY - box.getBoundingClientRect().top;
```


```
// ��ֹ�������Ĭ����Ϊ
evt.preventDefault ? evt.preventDefault() : evt.retrunValue = false;
```

### ����������������ק ###

ע�⣺ �ƶ�ʱҪ��� margin ������

```
layer.style.margin = "0px"; //margin��ʽ��Ӱ���˶�Ч��
```

### ���������й���������קЧ�� ###

������������ק

```
var offsetX = e.offsetX;
var offsetY = e.offsetY;


var scrollTop = document.body.scrollTop || document.documentElement.scrollTop;
var scrollLeft = document.body.scrollLeft || document.documentElement.scrollLeft;

document.onmousemove = function(e) {
	var x = e.clientX - offsetX + scrollLeft;
	var y = e.clientY - offsetY + scrollTop;
}
```


### ��������������ק ###

1. ��ס�������
2. �ط��˶��켣

�������ݵ������еķ���

```



// ����һ����Ŀն���
var point = {};

// �� point �����У�������һ�� x �����ԣ�ֵΪ x
point.x = x;
point.y = y;

// �� point ����ѹ�뵽 arr ������
// �൱�ڣ�ÿ�ƶ�һ�Σ����Ὣ������������
// ���ң���ӵĵ�����˳���
arr.push(point);
```

---------
�طŴ���

```
var i = 0;
var timer = setInterval(function() {
	var point = arr[i];

	box.style.top = point.y + "px";
	box.style.left = point.x + "px";

	i++;

	if (i >= arr.length) {
		// �Ѿ��������е����һ��Ԫ��
		clearInterval(timer);

		// �Ѿ���ɶ����ˣ������������
		arr = [];
	}

}, 10);
```


### ��������360��ȫ��չʾЧ�� ###

1. �����ק��ת
2. �Զ���ת

�����ק��ת: 

1. ���¼���mousedown ��ʼ��ק document.onmousemove , ��ʼ������� startX = e.offsetX
2. document.onmousemove  �¼��������У��õ� ��ֹ������� endX = e.offsetX
3. endX - startX �õ�ͼƬ�ı������� �����и�
     ���� ͼƬ�ı�� Խ��Խ��
	 ���� ͼƬ�ı�� Խ��ԽС
    ����ͼƬ

4. �ɿ�����ʱ�� document.onmousemove = null;


# ��ҵ #

1. ��������
![](hw1.png)

2. ������ק
�ɻط���ק�켣

