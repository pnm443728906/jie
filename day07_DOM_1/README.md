

# ��� #

1. DOM(�ĵ�����ģ��)
2. �ڵ����
3. �¼�����


# �������� #


## ���� ##
Markdown �� ����

## DOM(�ĵ�����ģ��) ##

Document Object Model �ĵ�����ģ��

DOM �� Document Object Model�ĵ�����ģ�ͣ����е�HTML��ǩ���Ƕ��󣬷ǳ�����õ������������ǲ����ַ��������ǲ�������

```
��ǩ <span> <div>     (css ��)
Ԫ�� <div id="div1">  (js ��)
�ڵ� <div> <span>     (DOM ��)
```

### ��ȡ�ڵ� ###

�շ�����������

document.getElementById




### �ڵ������Ԥϰ�� ###
	
����Ԫ��,���Ԫ�أ�ɾ��Ԫ�أ��滻Ԫ�أ���¡Ԫ��	

createElement appendChild insertBefore removeChild replaceChild cloneNode

�ο��˽�
https://developer.mozilla.org/zh-CN/docs/Web/API/Document/createElement


## ����HTML���� ##

HTML��ǩ�кܶ����ԣ�����src��href��title�ȵȡ�
JS���Ը���HTML���κ����ԣ����������֣����﷨ �� setAttribute()��getAttribute()��

#### �������� ��ҳ���� ####

css ��ʽ���� css �ļ���
```
<link id="link" href="css/css1.css" rel="stylesheet" type="text/css" />


<dl id="message">
	<form>
		<dt>
			<strong>���Ի������ύ��</strong>
			<input type="button" value="Ƥ��1" data-css="css1" />
			<input type="button" value="Ƥ��2" data-css="css2" />
		</dt>
		<dd>����������<input class="text" type="text" /></dd>
		<dd>�������룺<input class="text" type="password" /></dd>
		<dd>�������ԣ�<textarea></textarea></dd>
		<dd class="center"><input class="btn" type="submit" value="�ύ" /></dd>
	</form>
</dl>

```

#### ����Ԫ���е�ͼƬ ####

### ����Ԫ����ʽ ###

ͨ�����﷨.style�ܹ��õ�������ʽ�ķ�װ  ע�⣬ֻ�ܵõ�������ʽ������д��css��Ƕ�ġ������ģ�һ�ɲ��ܵõ�����Ҫ���Ǻ���ѧϰ��֪ʶ���õ��������ʽ��




### ������ ###

```
<style>
	#progress{
		position: relative;
		margin: auto;
		top: 200px;
		display: block;
		width: 200px;
		height: 20px;
		border-style: dotted;
		border-width: thin;
		border-color: darkgreen;
	}
	#filldiv{
		position:absolute;
		top: 0px;
		left: 0px;
		width: 0px;
		height: 20px;
		background: blue;
	}
	#percent{
		position: absolute;
		top: 0px;
		left: 200px;
		
	}
</style>


<div id="progress">
	<div id="filldiv"></div>
	<span id="percent">0</span>
</div>

```


## �¼����� ##

JavaScript��������Ч�����벻���¼�����ν���¼��������û���ĳ����Ϊ���ܹ�����һ��������ִ��


��������ֻѧϰDOM��׼�е�0�����¼��󶨷�����

```
	// �õ����box
	var oDiv = document.getElementById("box");
	
	//�¼�
	oDiv.onclick = function(){
		alert("��ã����Ҹ���ҷ����أ���");
	}

```

Ҳ���ԣ�

```

	oDiv.onclick = fun;
	
	function fun(){
		alert("��ã����Ҹ���ҷ����أ���");
	}


```

������������˸������ˣ�ԭ��������Ҫһ������ִ�У���������������������fun();
����������֪���ˣ�һ���������Ե���һ���¼��Ĵ�������������¼�������ʱ�򣬺���Ҳ��ִ���ˡ�

```

onclick 		����
onmouseover	������
onmouseout		����뿪
ondblclick		˫��
onfocus			�õ�����
onblur			ʧȥ����
onmousedown		��갴��
onmouseup			��갴��̧��

onload 		��ҳ����ȫ���سɹ�
window.onload ��ʾҳ���е����еĴ��붼�Ѿ���������ˡ�

```


### ���� ###

#### ���������ť������ ####

```
// Ϊʲôû��д���ĵ�����֮��Ϊʲô allBtn ��Ϊ��
// ��Ϊ getElementsByTagName �����ڵò���Ԫ�ص�����£�
// ��Ȼ�᷵��һ������, ֻ��������������е�Ԫ�ظ���Ϊ 0
// alert(allBtn);
```


```
// �±�Ϊ i �Ķ��� �����˺ܶ����� �� �ܶ෽���������ǿ���������������������ԣ�����
// ���±�Ϊ i �İ�ť���� ��������һ������ xxx���������е�ֵ����Ϊ i
allBtn[i].xxx = i;
```


�����ѡ�ͨ�� �հ����� ��ʵ��

ͨ���󶨺����ĵķ���������ȡ�����ť���±�
```
function bind(obj, pos) {
	obj.onclick = function() {
		alert(pos);
	}
}

bind(allBtn[i], i);
```


```
	<button>��ť1</button>
	<button>��ť2</button>
	<button>��ť3</button>
	<button>��ť4</button>
	<button>��ť5</button>
	<button>��ť6</button>
```

#### tab��ǩ�л� ####

```
#tab span{display:inline-block;padding:5px 15px;background-color:#ddd;margin:0 3px;border:1px solid #ddd;border-bottom:none;}
.content{padding:15px;border:1px solid #ddd;font-size:24px;background-color:#efefef;}



<div id="tab"><span>����</span><span>����</span><span>������</span><span>�����׷�</span></div>
<div class="content">��ϲ��������</div>
<div class="content">���궹��������</div>
<div class="content">ϲ��ȥ�����󷽱���</div>
<div class="content">�����׷�����������</div>

```

#### �������� ####

����ĳ����ť����ʾ�����ж�Ӧ����Ϣ

```
<style type="text/css">
* { padding: 0; margin: 0; }
li { list-style: none; }
body { background: #f6f9fc; font-family: arial; }

.calendar { width: 210px; margin: 0 auto; padding: 10px 10px 20px 20px; background: #eae9e9; }
.calendar ul { width: 210px; overflow: hidden; padding-bottom: 10px; }
.calendar li { float: left; width: 58px; height: 54px; margin: 10px 10px 0 0; border: 1px solid #fff; background: #424242; color: #fff; text-align: center; cursor: pointer; }
.calendar li h2 { font-size: 20px; padding-top: 5px; }
.calendar li p { font-size: 14px; }

.calendar .active { border: 1px solid #424242; background: #fff; color: #e84a7e; }
.calendar .active p { font-weight: bold; }

.calendar .text { width: 178px; padding: 0 10px 10px; border: 1px solid #fff; padding-top: 10px; background: #f1f1f1; color: #555; }
.calendar .text h2 {font-size: 14px; margin-bottom: 10px; }
.calendar .text p { font-size: 12px; line-height: 18px; }

</style>


	var arr=['������ˣ���ҿ���������ȥ����ɡ�',
		'��Һú�ѧϰ��222222~~~',
		'��Һú�ѧϰ��222222333~~~',
		'��Һú�ѧϰ��222444222~~~',
		'��Һú�ѧϰ555��222222~~~',
		'��Һú�ѧϰ��666222222~~~',
		'��Һú�ѧϰ��227772222~~~',
		'��Һú�ѧϰ��28888822222~~~',
		'��Һú�ѧϰ��99999222222~~~',
		'��Һú�ѧϰ10000000��222222~~~',
		'��Һú�ѧϰ��111111222222~~~',
		'��Һú�ѧϰ��22222200000000000~~~']



<div id="tab" class="calendar">

    <ul id="ul">
        <li class="active"><h2>1</h2><p>JAN</p></li>
        <li><h2>2</h2><p>FER</p></li>
        <li><h2>3</h2><p>MAR</p></li>
        <li><h2>4</h2><p>APR</p></li>
        <li><h2>5</h2><p>MAY</p></li>
        <li><h2>6</h2><p>JUN</p></li>
        <li><h2>7</h2><p>JUL</p></li>
        <li><h2>8</h2><p>AUG</p></li>
        <li><h2>9</h2><p>SEP</p></li>
        <li><h2>10</h2><p>OCT</p></li>
        <li><h2>11</h2><p>NOV</p></li>
        <li><h2>12</h2><p>DEC</p></li>
    </ul>
    
    <div class="text" id="txt">
        <h2>1�»</h2>
        <p>������ˣ���ҿ���������ȥ����ɡ�</p>
    </div>

</div>
```




#### ���ڵ��Ӧ�� ####

```
<style>
  a {cursor: pointer;}
</style>

<h1> ����ͷ�� </h1>

<ul id="ul1">
	<li>�һ�Ѳ���Ϻ��ͷ��ش��ź� ��6��ͻ������������  <a>&times;</a></li>
	<li>�������Լ��ſ�����ɮ����NBA����Τ�°ݷ�Ĳ�������... <a>&times;</a></li>
	<li>���ǿ̸������+���������Ƿ�չ�¾��ã�����������ͳ.. <a>&times;</a></li>
	<li>��λ85�����У�Ҫʵ��APP֮����������  <a>&times;</a></li>
	<li>���������ñ�ӹر� ���²�  <a>&times;</a></li>
</ul>

```


#### �ַ��� ####


```
<style>
		.hide{display:none;}

		#div1{border:1px solid #ddd;padding:1px;}
		#div1 h4{margin:1px;background-color:#ddd;padding:15px;}
		#div1 .content{display:none;height:120px;padding:15px;}
</style>

	<div id="div1">
		<h4>����1</h4>
		<div class="content">#����1</div>
		<h4>����2</h4>
		<div class="content">#����2</div>
		<h4>����3</h4>
		<div class="content">#����3</div>
		<h4>����4</h4>
		<div class="content">#����4</div>
		<h4>����5</h4>
		<div class="content">#����5</div>
	</div>


```



# ��ҵ #


1�� ���������ʮ�������½���ͻ��лƿ���֣��뿪����ʧ��

2�� ���ֲ�ͼ����ʦ���㲼�֣��Լ�д����

3�� �ֺŵı仯��

![](hw3.png)





## ѡ�� ##


1. ȫѡ�ͷ�ѡchecked


```
	<table id="dataList">
		<thead>
			<th><input type="checkbox" name="all" id="all"></th>
			<th>����</th>
		</thead>
		<tbody>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>��ë��</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>��ɽ</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>��Ӿ</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����Ӱ</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
			<tr>
				<td><input type="checkbox" name="hobby"></td>
				<td>����</td>
			</tr>
		</tbody>
	</table>
```


2. �ַ���

3. ��������

4. ���������ʮ�������½���ͻ��лƿ���֣��뿪����ʧ




