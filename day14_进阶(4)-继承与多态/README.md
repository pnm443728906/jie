
# ��� #

1. ԭ��
2. �̳�
3. ����


# �������� #

## ԭ�� ##

��JavaScript�У��κ�һ������������һ��prototype���ԣ�ָ��һ���������������һ��������prototype���ԣ���ᷢ����һ���ն���������prototype�����ͣ�������object���͡�
prototype����Ӣ�ԭ�͡�����˼��ÿ����������ԭ�ͣ�ԭ����һ������
һ��������ԭ�ͣ�������ͨ������˵��û�κ����á��������������һ�����캯������ô������ԭ�ͣ��ô�����
```
1	//���캯�������캯������û���κ���䣬Ҳ����˵��������캯����ִ�е�ʱ�򣬲�������������Ķ�������κ����ԡ�
2	function People(){
3	
4	}
5	//���캯����ԭ�ͣ����Ǹ����˹��캯����ԭ�ͣ�Ϊһ���µĶ���
6	People.prototype = {
7		name : "����",
8		sex : "��",
9		age : 18
10	}
11	
12	//��һ������new������ʱ�򣬲�����ִ���˹��캯���������䣬Ҳ������������__proto__ָ���캯����prototype��
13	var xiaoming = new People();
14	
15	console.log(xiaoming.__proto__);
16	console.log(xiaoming.__proto__ == People.prototype);
17	
18	//��������ͼ����name��sex��age���Ե�ʱ������û�С���ô��ȥ����ԭ�ͣ�ԭ�������У��͵������Լ������Է����ˡ�
19	console.log(xiaoming.name);
20	console.log(xiaoming.sex);
21	console.log(xiaoming.age);

```


prototypeһ���Ǻ��������ԣ������������һ�����캯����ʱ����ô��new�����Ķ��󣬽�������ԭ���Ǹ�����Ϊnew������ʵ����ԭ�Ͷ���

ע�⣬�κ�һ�����󣬶���__proto__���ԣ����������Chrome�Լ������ԣ��������������ݣ����Ǳ�������Ҳ��ԭ�Ͷ���ֻ��������ͨ��__proto__���з��ʶ��ѡ�
��������ָ���Լ���ԭ�Ͷ���
���ǵ�JavaScript��һ���ǳ�ţ�ƵĻ��ƣ�ԭ�������ҡ�
��������ͼ����һ���������ϵ����Ե�ʱ������������������������ԣ��򷵻�����ֵ�����������û��������ԣ���ô����������ԭ�Ͷ��󣬼������ԭ�Ͷ��������Ƿ������ֵ������з�����ԭ�Ͷ������ϵ����ֵ��

Ҳ����˵�����ǸղŽ�����2�������һ�������Ĺ��¡��κ�һ����������ԭ�ͣ�ԭ����һ��������prototype�����ʡ�����������ǹ��캯����ʱ��new�����Ķ������ǵ�ԭ�Ͷ������������캯����ԭ�͡�
prototype���ǳ�Ϊ��ԭ�͡���ֻ�к�����ԭ��
__proto__���ǳ�Ϊ��ԭ�Ͷ��󡱣��κζ�����ԭ�Ͷ���

### JavaScriptԭ�������� ###

ͼ��JavaScriptԭ���� 
http://blog.rainy.im/2015/07/20/prototype-chain-in-js/




## �̳� ##

JavaScript�̳з�ʽ���
https://segmentfault.com/a/1190000002440502

JavaScript�е���̳�
http://javascript.crockford.com/zh/inheritance.html

�������JavaScript��������ԭ�ͼ̳�
https://github.com/norfish/blog/wiki/%E6%B7%B1%E5%85%A5%E7%90%86%E8%A7%A3JavaScrip%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E5%92%8C%E5%8E%9F%E5%9E%8B%E7%BB%A7%E6%89%BF

```

���ˡ��� �� ��Сѧ�����ࡣ Сѧ��Ҳ���ˣ�ֻ�������ḻ�ˡ��ˡ�
���ˡ����е����ԣ���Сѧ�������У��������������䡢�Ա�
���ˡ����еķ�������Сѧ�������У�������к����Է���˯����
����֮�⣬
��Сѧ�������ḻ��һЩ���ԣ�ѧ�š��༶��С�컨�������Ƿ����ȶ�Ա
��Сѧ�������ḻ��һЩ������ѧϰ��lol���Ͽ�

```


Сѧ���࣬�̳������ࡣһ˵�̳У�ǧ��Ҫ�뵽�������Ų��̳У��о�Сѧ���������٣�������ľֲ���ǧ��Ҫ��ô�롣�ڼ���������У��̳��ǡ��ḻ�����Ǳ�ԭ������Ҫ�ණ����
Сѧ���̳������࣬ Сѧ�����ḻ��

˵���ˣ�People��Student�����࣬Student���ʵ����ӵ�� People��ȫ���������ԡ�������
���ڣ����Ӧ���������ʵĸо�������ԭ������ʵ�֡�JavaScript��û��extends��
People�������ࡢ���ࣻ Student�������ࡣ


```
 function People(name,age,sex){
2				this.name = name;
3				this.age = age;
4				this.sex = sex;
5			}
6			People.prototype.sayHello = function(){
7				alert("���������" + this.name);
8			}
9			People.prototype.chifan = function(){
10				alert("�ҳԷ��ˣ�mia mia");
11			}
12	
13	
14			function Student(name,age,sex,xuehao,xiaohonghuageshu){
15				this.name = name;
16				this.age = age;
17				this.sex = sex;
18				this.xuehao = xuehao;
19				this.xiaohonghuageshu = xiaohonghuageshu;
20			}
21			//������䣬�̳е�ʵ��ȫ����������ˣ�
22			Student.prototype = new People();
23			
24			Student.prototype.sayHello = function(){
25				alert("�������Сѧ�����ҵ�ѧ����" + this.xuehao);
26			}
27			Student.prototype.study = function(){
28				alert("�ú�ѧϰ����������");
29			}
30			Student.prototype.lol = function(){
31				alert("���Ӣ�����˰���");
32			}
33	
34			var xiaohong = new Student("С��",11,"Ů",20160001,4);
35			//xiaohong.lol();
36			//xiaohong.chifan();
37			xiaohong.sayHello();

```

![](1.png)

###  in����� ###

����һ������ֵ����ʾ��������ǲ��Ƕ�������ԡ�
```
1			var obj = {
2				a : 1,
3				b : 2,
4				c : false
5			}
6	
7			console.log("a" in obj);	//true
8			console.log("b" in obj);	//true
9			console.log("c" in obj);	//true
10			console.log("d" in obj);	//false

```

in����������Ƕ����Լ���û��������ԣ����ԭ��������������ԣ���ôҲ�᷵��true������ԭ�������û��������ԣ��ͷ���false��Ҳ����˵��in�����������ԭ�������ҡ�

for in ���ѭ�������ԭ���������еĿ�ö�ٵ������г�����
```
1	for(var k in obj){
2		console.log(k);
3	}

```

ʲô�ǿ�ö�٣�ϵͳĬ�ϵ����ԣ�����constructor�����ǲ���ö�ٵġ�for inѭ���ܹ����Լ���ӵ��������г��������еĲ��������Լ����ϵ����ԣ�����ԭ�����ϵ��������ԡ�

### hasOwnProperty���� ###

���������������Object.prototype�������棬�����κ�һ��Object���ܹ�ӵ�����������
�����������true��false����ʾ�Լ��Ƿ�ӵ��������ԣ�������ԭ�������Ϳ��Լ�������û��������ԣ�������ԭ�������ҡ�
```
1			var obj = {
2				a : 1,
3				b : 2,
4				c : 3
5			}
6			obj.__proto__ = {
7				d : 4
8			}

9			console.log(obj.hasOwnProperty("a")); //t
10			console.log(obj.hasOwnProperty("b")); //t
11			console.log(obj.hasOwnProperty("c")); //t
12			console.log(obj.hasOwnProperty("d")); //f

```

for����in����ԭ�������������ǿ�����Ƕһ���жϣ����Լ����ϵ����������
```
1	for(var k in obj){
2		obj.hasOwnProperty(k) && console.log(k);
3	}

```
 
### ����ֱ�Ӵ����֤ĳ�������Ƿ���� ###
������������ԣ�����֮ǰ�Ŀγ��Ѿ�����������ԭ���������ԾͿ��Կ����������Ƿ����Լ����ϡ�ԭ�����ϡ�����ڣ��ͷ���ֵ��������ھͷ���undefined.


### instanceof����� ###

����Ӣ���������class��ʵ����Ӣ���������instance��
instaceof�������
1	A instaceof B
��֤A�����ǲ���B���ʵ����


```

1			//�࣬���캯��
2			function Dog(){
3	
4			}
5			//ʵ����һ������
6			var d = new Dog();
7			//��֤d�ǲ���Dog��һ��ʵ��
8			console.log(d instanceof Dog);

```

���Ϊ true

instanceof ������Ļ��� ���hellokitty��������ԭ�����ϵ�ÿ��ԭ�Ͷ��������õ����ԭ�Ͷ�����ĳ�����캯����prototype����ô����Ϊhellokitty��������캯����ʵ��������true��


��instanceof������ܹ����ɽ�������ʶ��
```
1	var arr = [];
2	console.log(arr instanceof Array);

```

## ���� ##


### ��ק ###
����


## ��ҵ ##

1. ��дө�������ק����
