


# ��� #

1. �ڵ��ϵ
2. �ڵ����
3. ����չʾ


# �������� #

## �ڵ��ϵ ##


DOM��
https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/Using_the_W3C_DOM_Level_1_Core

Document
https://developer.mozilla.org/zh-CN/docs/Web/API/Document


ԭ��JS���ṩ�Ľڵ��ϵ���٣�
childNodes��firstChild��lastChild��parentNode��nextSibling��previousSibling


����childNodesһ��Ҫ��ס��IE6��7��8�͸߼�������Ĳ�һ�£��߼�����������еĻ���Ϊ���ı��ڵ㣬��IE6��7��8����������ı��ڵ㡣
```
1		<div id="box">
2			<p></p>
3			<p></p>
4			<p></p>
5			<p></p>
6		</div>

```

1	oDiv.childNodes.length;   //chrome��ֵ��9   IE6��7��8��ֵ��4


��������������⡿-����

## �ڵ���� ##


HTML�ڵ�����ԭ����������Ǹĸ�HTML���ԣ�����src���Ըĸģ����߸ĸ�css��ʽ������.style����.css()��
���ڵ������ǣ�����Ҫ���ӽڵ㡢ɾ���ڵ㡢�ƶ��ڵ㡢�滻�ڵ㡣


### createElement()��appendChild() ###

```
1			var ul = document.getElementsByTagName("ul")[0];
2			//����һ��li��ǩ���ñ���oLi����ʾ�����������Ľڵ㲻���κνڵ�Ķ��ӣ�
3			//Ҳ����˵û����DOM���ϣ�
4			var oLi = document.createElement("li");
5			oLi.innerHTML = "DDDD";	//�ı�����ڵ����������
6	
7			//���´����Ľڵ㣬׷�ӵ�DOM����
8			ul.appendChild(oLi);

```

### insertBefore ###

���Ǹղ�˵��appendChild�ǰ��½ڵ��ڸ��׵����ж��Ӻ���ӣ�Ҳ����˵��ӵĽڵ���Ǹ��׵����һ�����ӡ�
���ǿ���������һ��λ����ӽڵ㡣
1	����.insertBefore(�¶���,ԭ�б�˶���);
����ԭ�б�˶���֮ǰ���롣


### removeChild() ###

1	����.removeChild(����);
���Ҫ��ɱ��ҲҪ�ҵ��ְ�
1	this.parentNode.removeChild(this);



### replaceChild() ###

�滻�ڵ�
1	����.replaceChild(�¶���, �϶���);



### �ڵ�Ŀ�¡ ###

��¡�ڵ㣬����true��ʾ��ƣ��ڵ��������������һͬ���ơ�
����֮��Ľڵ��Ǹ��¶��ڵ㣬����Ҳ��Ҫʹ��appendChild��inserBefore��replaceChild�������DOM����

1	ul.appendChild(lis[0].cloneNode(true));


HTML DOM cloneNode() ����
http://www.w3school.com.cn/jsref/met_node_clonenode.asp




## ����չʾ ##

### ����ƶ�Ԫ�� ###


### �������� ###

### ���ؽű� ###
��̬���� js �ű��ļ�



## ��ҵ ##

д��һ����������ı��,Ч���ο�ʾ��



