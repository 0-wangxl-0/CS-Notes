<!-- GFM-TOC -->
* [����](#����)
    * [1. List](#1-list)
    * [2. Set](#2-set)
    * [3. Queue](#3-queue)
    * [4. Map](#4-map)
    * [5. Java 1.0/1.1 ����](#5-java-1011-����)
* [�����е����ģʽ](#�����е����ģʽ)
    * [1. ������ģʽ](#1-������ģʽ)
    * [2. ������ģʽ](#2-������ģʽ)
* [ɢ��](#ɢ��)
* [Դ�����](#Դ�����)
    * [1. ArraList](#1-arralist)
    * [2. LinkedList](#2-linkedlist)
    * [3. Vector](#3-vector)
    * [4. HashMap](#4-hashmap)
    * [5. LinkedHashMap](#5-linkedhashmap)
    * [6. ConcurrentHashMap](#6-concurrenthashmap)
* [�ο�����](#�ο�����)
<!-- GFM-TOC -->

# ����

![](https://github.com/CyC2018/InterviewNotes/blob/master/pics/ebf03f56-f957-4435-9f8f-0f605661484d.jpg)

������Ҫ���� Collection �� Map ���֣�Collection �ְ����� List��Set �Լ� Queue��

## 1. List

- ArrayList��ʹ�����鷽����֧��������ʣ�

- LinkedList��ʹ������ʵ�֣�ֻ��˳����ʣ����ǿ��Կ��ٵ����м�����ɾ��Ԫ�ء�������ˣ�LinkedList ����������ջ�����к�˫�˶��С�

## 2. Set

- HashSet��ʹ�� Hash ʵ�֣�֧�ֿ��ٲ��ң�����ʧȥ�����ԣ�

- TreeSet��ʹ����ʵ�֣��������򣬵��ǲ���Ч�ʲ��� HashSet��

- LinkedListHashSet������ HashSet �Ĳ���Ч�ʣ����ڲ�ʹ������ά��Ԫ�صĲ���˳����˾��������ԡ�

## 3. Queue

ֻ������ʵ�֣�LinkedList �� PriorityQueue������ LinkedList ֧��˫����С�

## 4. Map

- HashMap��ʹ�� Hash ʵ��

- LinkedHashMap����������˳��Ϊ����˳������������ʹ�ã�LRU��˳��

- TreeMap�����ں����ʵ��

- ConcurrentHashMap���̰߳�ȫ Map�����漰ͬ������

## 5. Java 1.0/1.1 ����

���ھɵ����������Ǿ���Ӧ��ʹ�����ǣ�ֻ��Ҫ�����ǽ����˽⡣

- Vector���� ArrayList ���ƣ��������̰߳�ȫ��

- HashTable���� HashMap ���ƣ��������̰߳�ȫ��

# �����е����ģʽ

## 1. ������ģʽ

�Ӹ���ͼ���Կ�����ÿ�������඼��һ�� Iterator ���󣬿���ͨ��������������������������е�Ԫ�ء�

[Java �еĵ�����ģʽ](https://github.com/CyC2018/InterviewNotes/blob/master/notes/%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F.md#92-java-%E5%86%85%E7%BD%AE%E7%9A%84%E8%BF%AD%E4%BB%A3%E5%99%A8)

## 2. ������ģʽ

java.util.Arrays#asList() ���԰���������ת��Ϊ List ���͡�

```java
 List list = Arrays.asList(1, 2, 3);
 int[] arr = {1, 2, 3};
 list = Arrays.asList(arr);
```

# ɢ��

ʹ�� hasCode() ������ɢ��ֵ��ʹ�õ��Ƕ���ĵ�ַ��

�� equals() �������ж����������Ƿ���ȵģ���ȵ���������ɢ��ֵһ��Ҫ��ͬ������ɢ��ֵ��ͬ����������һ����ȡ�

��ȱ�����������������ʣ�

1. �Է���
2. �Գ���
3. ������
4. һ���ԣ���ε��� x.equals(y)��������䣩
5. ���κβ��� null �Ķ��� x ���� x.equals(nul) �����Ϊ false

# Դ�����

�������Ķ� [�㷨-����](https://github.com/CyC2018/InterviewNotes/blob/master/notes/%E7%AE%97%E6%B3%95.md#%E7%AC%AC%E4%B8%89%E7%AB%A0-%E6%9F%A5%E6%89%BE) ���֣��Լ�����Դ�������кܴ������


Դ�����أ�[OpenJDK 1.7](http://download.java.net/openjdk/jdk7)

�����Ķ���[7u40-b43](http://grepcode.com/snapshot/repository.grepcode.com/java/root/jdk/openjdk/7u40-b43/)

## 1. ArraList

- ʹ������ʵ��

- ���ж�̬�������ԣ�Ĭ������Ϊ 10�����������Ԫ��ʱʹ�� ensureCapacity() ��֤�����㹻���������������������Ϊԭʼ������ 1.5 times + 1.

[ArraList.java](https://github.com/CyC2018/InterviewNotes/blob/master/notes/src/ArrayList.java)


## 2. LinkedList

- LinkedList �ǻ���˫��ѭ������ʵ�֣�ͷ��㲻�������ݡ�

![](https://github.com/CyC2018/InterviewNotes/blob/master/pics/d40c90ad-7943-4574-98a8-8027e5523d53.jpg)

- ���������������Ҫ��������LinkedList �� Entry entry(int index) ��������������������������һ���Ż��Ĳ������������ index ������ǰ�棬��ô�ʹ�ͷ�������������ں���ʹӺ���ǰ������

[LinkedList.java](https://github.com/CyC2018/InterviewNotes/blob/master/notes/src/LinkedList.java)

## 3. Vector

Vector �ĺܶ�ʵ�ַ�����������ͬ����䣬������̰߳�ȫ�ġ�

[Vector.java](https://github.com/CyC2018/InterviewNotes/blob/master/notes/src/Vector.java)

## 4. HashMap

- ʹ���������������ͻ��

[Vector.java](https://github.com/CyC2018/InterviewNotes/blob/master/notes/src/HashMap.java)


## 5. LinkedHashMap

- ʹ��˫���������������Ľڵ㣬�Ӷ�ά��һ������˳��
- ע��Դ���е�accessOrder��־λ������falseʱ����ʾ˫�������е�Ԫ�ذ���Entry����LinkedHashMap���е��Ⱥ�˳�����򣬼�ÿ��put��LinkedHashMap�е�Entry������˫�������β������������˫������ʱ��Entry�����˳���Ͳ����˳��һ�£���Ҳ��Ĭ�ϵ�˫������Ĵ洢˳�򣻵���Ϊtrueʱ����ʾ˫�������е�Ԫ�ذ��շ��ʵ��Ⱥ�˳�����У����Կ�������ȻEntry���������˳����Ȼ�ǰ�����put��LinkedHashMap�е�˳�򣬵�put��get�������е���recordAccess������put������key��ͬ������ԭ�е�Entry������µ���recordAccess���������÷����ж�accessOrder�Ƿ�Ϊtrue������ǣ��򽫵�ǰ���ʵ�Entry��put������Entry��get������Entry���Ƶ�˫�������β����key����ͬʱ��put��Entryʱ�������addEntry���������creatEntry���÷���ͬ�����²����Ԫ�ط��뵽˫�������β�����ȷ��ϲ�����Ⱥ�˳���ַ��Ϸ��ʵ��Ⱥ�˳����Ϊ��ʱ��EntryҲ�������ˣ�������ʲôҲ���������˵˵LinkedHashMap�����ʵ��LRU�ġ����ȣ���accessOrderΪtrueʱ���ŻῪ��������˳�������ģʽ����������ʵ��LRU�㷨�����ǿ��Կ�����������put��������get���������ᵼ��Ŀ��Entry��Ϊ������ʵ�Entry����˱�Ѹ�Entry���뵽��˫�������ĩβ��get����ͨ������recordAccess������ʵ�֣�put�����ڸ�������key������£�Ҳ��ͨ������recordAccess������ʵ�֣��ڲ����µ�Entryʱ������ͨ��createEntry�е�addBefore������ʵ�֣�������������ʹ���˵�Entry���뵽��˫������ĺ��棬��β�����˫������ǰ���Entry�������û��ʹ�õģ��������ڵ��������ʱ��ɾ������ǰ���Entry(head������Ǹ�Entry)�����������ʹ�õ�Entry��

[LinkedHashMap.java](https://github.com/CyC2018/InterviewNotes/blob/master/notes/src/HashMap.java)

## 6. ConcurrentHashMap

[̽�� ConcurrentHashMap �߲����Ե�ʵ�ֻ���](https://www.ibm.com/developerworks/cn/java/java-lo-concurrenthashmap/)

[ConcurrentHashMap.java](https://github.com/CyC2018/InterviewNotes/blob/master/notes/src/HashMap.java)

# �ο�����

- Java ���˼��
