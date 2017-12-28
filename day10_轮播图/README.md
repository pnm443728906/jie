


# ��� #

1. �첽�ͻص�����
2. �����˶�
3. �����ֲ�ͼ


# �������� #

## �첽�ͻص����� ##

Javascript�첽��̵�4�ַ���
http://www.ruanyifeng.com/blog/2012/12/asynchronous%EF%BC%BFjavascript.html

JavaScript���������ͬ�����첽���¼�ѭ��(Event Loop)
https://segmentfault.com/a/1190000004322358



�����������forѭ�����ǳ��ķ�ʱ�䣬����ϵͳ���á�ͬ�����ķ�ʽ���У�

```
1			console.log(1);
2			console.log(2);
3			console.log(3);
4			for (var i = 0; i < 10000; i++) {
5				console.log("��");
6			}
7			console.log(4);

```


��ͬ��������˼��forѭ���ܺķ�ʱ�䣬���ǳ������ɵ�ȣ�ɵɵ�ĵȴ�10000�����������Ȼ�����4��
��������ȥ�Ӷ��ӵķɻ�����Ҫ�Ⱥܳ�ʱ�䣬�ȴ���ʱ�����ɵ�ȣ���ͬʱ��������顣


�첽Asynchronous

```
1			console.log(1);
2			console.log(2);
3			console.log(3);
4			setInterval(function(){
5				console.log("��");
6			},1000);
7			console.log(4);

```
���첽������˼��������һ���ر�ķ�ʱ������飬���򲻻�ɵ�ȣ�������ִ�к������䡣


### �ص����� ###

�첽�����������ˣ������������ʲô�¶����Ǵ�ʱ��ô���أ�
�ص������� �첽���������֮��Ҫ��������





JavaScript�ص�����
https://cnodejs.org/topic/564dd2881ba2ef107f854e0b


ǳ̸ javascript �ص�����
http://wiki.jikexueyuan.com/project/brief-talk-js/callback-function.html


����ʹ�� JavaScript �еĻص�����
http://blog.csdn.net/luoweifu/article/details/41466537


### apply��call������ ###

������ͼ�ڻص������У���this��ʾoDiv���������о�ˬ��

```
1	animate(oDiv,{"left":600},2000,function(){
2		this.style.backgroundColor = "red";
3	});

```
���ǲ��У��ص�������this����oDiv��


Function.prototype.call()
https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/call



## �����˶� ##
һ��������3000����ʱ�䣬��100��700����һ�������ٵġ�
ʱ�侫ȷ���ƶ��ı仯��Ҳ��ȷ�����ǲ�һ�������ٵġ�
����һ��Сʱ�������죬����55�룬���10m��С��������55��׼ȷ������10m���ˣ����ǣ��㶮�á�

���������ٵġ������ȿ��������������أ�����ǻ��壬Ӣ�����tween��



1. �ٶȱ仯����
2. �����˶�

## �ֲ�ͼ ##


1. ��ͳ�ֲ�
2. ��λ�ô�ͳ�ֲ�ͼ
3. �����ֲ������浭�뵭���ֲ���
4. ���ι���

### setTimeout()�ͺ������� ###

setTimeout clearTimeout
setInterval�����ü������
setTimeout��������ʱ����
1	window.setTimeout(����,ʱ��);
��ָ��ʱ��֮��ִ�к���һ�Σ�����ִ��1�Ρ�
ͬ���ģ���Ҳ��window����ķ��������Բ�дwindow


��ʱ��Ҳ�ܱ����������ʱ��û��ִ�е�ʱ�򣬾Ϳ��������������ᴥ��������
1	clearTimeout();


#### �������� ####

javaScript ��������
http://imweb.io/topic/577aa790ea7bb9b760c7adc3


ν�ĺ�����������������ϣ��һЩ������Ҫ�����Ĵ����������ڹ涨�����������������С����Ƕ���ʱ�䡣
������Ǻ���������
����1��
����ĺ�������ģ�ͣ�
```
1	
2	var lock = true;
3	input.onclick = function(){
4		if(!lock) return;
5		lock = false;
6		setTimeout(function(){
7			lock = true;
8		},1000);9	}

```
����2��
�ı����ǵ��˶���ܣ����˶�����������һ���߼����˶���ʼ�ˣ��͸�elem����һ������isanimated����ʾ�Ƿ����˶�����Ϊtrue��Ȼ���˶�ֹ֮ͣ��ͣ��֮�󣬰�elem.isanimated��Ϊfalse

```
1	.onclick = function(){
2		if(m_unit.isanimate) return;   //��������ť��ʱ���˶������ڶ�����ôreturn3	}

```



#### ��Ъģ�Ͱ��� ####

1. �������ֵ�Ч��
2. �������ֵ�Ч��
3. �ֲ���Ч��


#### �����ֲ� ####

˼·��

1. �ı�͸����
2. �л�


#### �����ֲ� ####

1. ���ι����������1-ԭ���ʾ
2. ���ι����������2-����Ļ��JSON
3. ���ι����������3-��2�ε��
4. ���ι����������4-�����Զ��ֲ�

## ��ҵ ##

1. �޷���������
2. ��ͳ�ֲ�
3. �����ֲ�
4. ��Ъģ��



