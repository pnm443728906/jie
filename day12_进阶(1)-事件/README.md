


# ��� #

1. �¼���
2. �¼���
3. �¼�����


# �������� #

## �¼��� ##

�¼�����
https://segmentfault.com/a/1190000003497939

���㵥����ĳ��Ԫ�أ������¼����������������Ԫ���ϣ���Ҳ���������ĸ�Ԫ�ء���Ԫ�صĸ�Ԫ�ء�������������Ԫ�أ���������������ҳ�档

### ���ļ�ʱ�༭ ###

### �¼�ί�� ###

����������ʱ�༭���

�����䡿�ַ����Ĵ�Сдת��


## �¼��� ##

### DOM0���¼��� ###
DOM��Ϊ����DOM0����1����2����3�����ǲ�ͬ�ı�׼����׼һֱ��������
����֮ǰѧϰ��
1	oDiv.onclick = function(){2	}
����ע�������д��������DOM0�����¼��󶨷��������ǰ�onclick����������Ӹ���oDivԪ�ء�


### DOM2���¼��� ###

ð���¼�


DOM1���淶�У�û�ж��¼����иĶ���
DOM2�������µĹ淶������on***���󶨼����ˣ�����ʹ��һ������
1	addEventListener();
add��ӣ�Event�¼���Listener����


����������������ʲô�¼����������Ƿ��������׶Ρ�

```
1	oBox.addEventListener("click",function(){
2		
3	},false);

```

��1���������¼�������дon��  click��mouseover ��mouseout
��2����������������������������Ҳ��������������
��3������������ֵ��true��ʾ��������false��ʾ����ð�ݽ׶�


#### �Ͱ汾IE���¼��� ####

IE��Զ�Ǹ����⣬��������20%���û���ʹ��IE8������ףԸ���ǽ����Ҹ���
IE6��7��8��֧��addEventListener()������֧��
1	oDiv.attachEvent(��onclick��,����);
û�е�����������Ҳ����˵������ѡ���������ð�ݡ�ֻ�ܼ���ð�ݡ�

```
1	 box1.attachEvent("onclick", function(){
2	 	alert("box1");
3	 });

```

��һ������������дon����addEventListener()��һ����
�ڶ��������������¼�������
û�е�����������ֻ�ܼ���ð�ݡ����Ժ�on***д��һ����


### ��ʱ�༭ ###

### �¼�ί�� ###

����������ʱ�༭���



## �¼����� ##


Event ��������¼���״̬�������¼������з�����Ԫ�ء����̰�����״̬������λ�á���갴ť��״̬��


�¼�ģ��JavaScript��׼�ο��̳�
http://javascript.ruanyifeng.com/dom/event.html


�¼�����ע���
https://segmentfault.com/a/1190000004290690


JavaScript Event�������
http://www.cnblogs.com/prince1988/archive/2009/04/04/1429525.html


�κε��¼������������ǵ��������JS�����Ĭ�������洫һ��ʵ�Σ������¼�����
ͨ�����β�event�����գ�
```
1	oDiv.onclick = function(event){
2		console.log(event);
3	}

```

### �¼����� ###
```

����¼���
	onclick:���
	onmouseover��������
	onmouseout������뿪
	ondblclick��˫���¼�  ��ע���� dbl��
	onmousedown����갴��
	onmouseup�����̧��
	onmousemove������ƶ�

���¼���
	onfocus����ý���
	onblur��ʧȥ����
	onsubmit���ύ�¼�
	onchange���������ı��ʱ��
	onreset�������¼�

�����¼���
	onkeyup������̧��
	onkeydown�����̰���
	onkeypress�����̰���һ��

�����¼���
    onload�¼�: ҳ��������֮������ִ�е��¼�

```


### ͨ���¼��������Ժͷ��� ###

�� event.type �����¼������ͣ�û��on�� ���硱click��
�� event.target ������������С���Ǹ�Ԫ�أ���ʹ���Ԫ������û�м�����Ҳ�Ƿ�����
�� event.currentTarget	�����Լ���thisһ����event.currentTarget��һ��Ԫ�أ������Լ�
�� event.bubbles	����һ������ֵ����ʾ����¼��Ƿ�ð��


```
1	oDiv.onmouseover = function(event){
2		console.log(event.bubbles); 
3	}

```

����onmouesover��event.bubbles����true;
����onmouseenter�� event.bubbles����false;
���onmouseoverð�ݣ�onmouseenter��ð�ݡ�
onmouseover��onmouseenter IE6��7��8��9��10ȫ����ݣ�������chrome30֮ǰ�����ݡ��������ڿ��Կ���ȫ�߼��ݣ������þ����¶��ˡ�


�� stopPropagation() ֹͣ�����¼���
1	event.stopPropagation();

�� preventDefault() ��ֹĬ���¼�
1	event.preventDefault();

### clientX��clientY��screenX��screenY ###

```
event.clientX
event.clientY
event.screenX
event.screenY

ȫ�߼��ݣ���ʾ�¼�������һ˲������λ�á�
clientX��ʾ����λ�ã����������������߱ߵľ���
clientY��ʾ����λ�ã���������������ϱ߱ߵľ���
screenX��ʾ����λ�ã�������Ļ��߱ߵľ���
screenY��ʾ����λ�ã�������Ļ�ϱ߱ߵľ���

```

![](1.png)

### IE�е�event ###

IE�������event������window��������ԣ��������¼���ʵ�Ρ�

```
2	document.onmousemove = function(event){
3	    event = event || window.event;
4	    document.innerHTML = event.clientX;
5	}
```

#### ��������������Ч�� ####

(��չ) ��������ʼ����ͼƬ���м�λ���أ�

```
// Firefox��chrome ����� ��ȡ�ڵ� bird ������ css ��ʽֵ
var obj = getComputedStyle(bird);

// "120px" ---> 120
var w = parseInt(obj.width);
var h = parseInt(obj.height);
```


### ��갴����� ###
event.button

//�����ǰevent������¼��������һ��button���ԣ�����һ������
//W3C �涨 event.button ȡֵ����:
```
0������갴�������
1�������˹���
2���������Ҽ�
```

�����ϰ汾��IE��û������W3C�Ĺ淶������button���Ժ�������

```
������ 1
����Ҽ� 2
����ͬʱ�� 3
���� 4
����ӹ��� 5
�Ҽ��ӹ��� 6
����ͬʱ 7

```

onmousedown: �����µ��¼�

### ���̰������ ###
������µ����������keyCode==37
������µ����ҷ������keyCode==39
������µ����Ϸ������keyCode==38
������µ����·������keyCode==40



**chrome���ߵ��Է�ʽ����Ҫ����Ҫ����Ҫ����**
F12 �򿪵��Թ���

1. ���öϵ㣺 �л��� sources ��ǩ�У�����������������ɫ��˵�����óɹ����ٴε������ȡ���ϵ�
2. ����ִ�У� F10 (��ݼ�)
3. ȫ��ִ�У� F8 (��ݼ�)

�м�����뿴������ֵ����������ƶ��������Ͼͻ�����ʾ


## ��ҵ ##

1. ���а���ȫ������дһ�顣

2. ģ��select�����˵�

![](hw1.png)

```
	<style>
		html,body{height:100%;overflow:hidden;}
		body,div,form,h2,ul,li{margin:0;padding:0;}
		ul{list-style-type:none;}
		body{background:#23384e;font:12px/1.5 \5fae\8f6f\96c5\9ed1;}
		#search,#search form,#search .box,#search .select,#search a{background:url(images/search.jpg) no-repeat;}
		#search,#search .box,#search form{height:34px;}
		#search{position:relative;width:350px;margin:10px auto;}
		#search .box{background-position:right 0;}
		#search form{background-repeat:repeat-x;background-position:0 -34px;margin:0 20px 0 40px;}
		#search .select{float:left;color:#fff;width:190px;height:22px;cursor:pointer;margin-top:4px;line-height:22px;padding-left:10px;background-position:0 -68px;}
		#search a{float:left;width:80px;height:24px;color:#333;letter-spacing:4px;line-height:22px;text-align:center;text-decoration:none;background-position:0 -90px;margin:4px 0 0 10px;}
		#search a:hover{color:#f60;background-position:-80px -90px;}
		#search .sub{position:absolute;top:26px;left:40px;color:#fff;width:198px;background:#2b2b2b;border:1px solid #fff;display:none;}
		#search .sub li{height:25px;line-height:24px;cursor:pointer;padding-left:10px;margin-bottom:-1px;border-bottom:1px dotted #fff;}
		#search .sub li:hover{background:#8b8b8b;}
	</style>


	<div id="search">
		<div class="box">
			<form>
				<span id="select" class="select">��ѡ����Ϸ����</span>
				<a href="javascript:;">����</a>
			</form>
		</div>
		<ul id="sub" class="sub">
			<li>���³�����ʿ</li>
			<li>ħ�����磨������</li>
			<li>ħ�����磨̨����</li>
			<li>��Ѫ����</li>
			<li>������II</li>
			<li>QQ��������</li>
		</ul>
	</div>
```

3. ������һ��Ч��

![](hw2.png)


