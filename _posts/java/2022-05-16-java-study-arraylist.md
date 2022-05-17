---  

layout: post  
title: "java study about ArrayList"  
image: javastudy.jpg  
categories: All java  

---  

# ArrayList  

ArrayList는 컬렉션 프레임 웍에서 가장 많이 사용되는 컬렉션 클래스일 것이다. 이 ArrayList는 List인터페이스를 구현하기 때문에 데이터의 저장순서가 유지되고 중복을 허용한다.  

ArrayList는 기존의 Vector를 개선한 것으로 Vector와 구현원리와 기능적인 측면에서 동일하다고 할 수 있다. 때문에 가능하면 Vector보다는 ArrayList를 사용하자.  

ArrayList는 Object배열을 순차적으로 저장한다. 예를 들면, 첫 번째로 저장한 객체는 Object배열의 0번째 저장되고 그 다음에 저장하는 객체는 1번째 위치에 저장된다. 이런식으로 계속 배열에 순서대로 저장되며, 배열에 더 이상 저장할 공간이 없으면 보다 큰 새로운 배열을 생성해서 기존의 배열에 저장된 내용을 새로운 배열로 복사한 다음에 저장된다.  

### ArrayList의 특징

> * 데이터 순서존재(index)  
> 
> * 연속적인 메모리 할당이 가능  
> 
> * LinkedList 보다 검색이 빠름  
> 
> * LinkedList 보다 데이터 추가 삭제가 느림  


<br>  

---  

<br>  


## 1. ArrayList의 메서드

|메서드|설명|  
|--|--|
|ArrayList()|크기가 0인 ArrayList를 생성  
|ArrayList(Collection c)|주어진 컬렉션이 저장된 ArrayList를 생성|  
|ArrayList(int initialCapacity)|저장된 초기용량을 갖는 ArrayList를 생성|  
|boolean add(Object o)|ArrayList의 마지막 개체를 추가. 성공하면 true|  
|void add(int index, Object element)|지정된 위치(index)에 객체를 저장|  
|boolean addAll(Collection c)|주어진 컬렉션의 모든 객체를 저장한다.|  
|boolean addAll(int index, Collection c)|지정된 위치부터 주어진 컬렉션의 모든 객체를 저장한다.|  
|void clear()|ArrayList를 완전히 비운다.|  
|Object clone()|ArrayList를 복제한다.|  
|boolean contains(Object o)|지정된 객체(o)가 ArrayList에 포함되어 있는지 확인한다.|  
|void ensureCapacity(int minCapacity)|ArrayList의 용량이 최소한 minCapacity가 되도록 한다.|  
|Object get(int index)|지정된 위치(index)에 저장된 객체를 반환한다.|  
|int indexOf(Object o)|지정된 객체가 저장된 위치를 찾아 반환한다.|  
|boolean isEmpty()|ArrayList가 비어있는지 확인한다.|  
|Iterator iterator()|ArrayList의 Iterator객체를 반환한다.|  
|int lastIndexOf(object o)|객체(o)가 저장된 위치를 끝부터 역방향으로 검색해서 반환한다.|  
|ListIterator listIterator()|ArrayList의 ListIterator를 반환한다.|  
|Object remove(int index)|지정된 위치(index)에 있는 객체를 제거한다.|  
|boolean remove(Object o)|지정한 객체를 제거한다.(성공하면 true, 실패시 false)|  
|boolean removeAll(Collection c)|지정한 컬렉션에 저장된것과 동일한 객체들을 ArrayList에서 제거한다.|  
|boolean retainAll(Collection c)|ArrayList에 저장된 객체 중에서 주어진 컬렉션과 공통된 것들만 남기고 나머지는 삭제한다.|  
|Object set(int index, Object element)|주어진 객체(element)를 지정된 위치(index)에 저장한다.|  
|in size()|ArrayList에 저장된 객체의 개수를 반환한다.|  
|void sort(Comparator c)|지정된 정렬기준(c)으로 ArrayList를 정렬한다.|  
|List subList(int fromIndex, int toIndex)|fromIndex로부터 toIndex사이에 저장된 객체를 반환한다.|  
|Object[] toArray()|ArrayList에 저장된 모든 객체들을 객체배열로 반환한다.|  
|Object[] toArray(Object[] a)|ArrayList에 저장된 모든 객체들을 객체배열 a에 담아 반환한다.|  
|void trimToSize()|용량을 크기에 맞게 줄인다.(빈 공간을 없앤다.)|  

<br>  

---  

<br>  

## 2. 예제  

---  

<script src="https://gist.github.com/nnlog/b5c5a15f60d84dec90267e3fae7826c6.js"></script>  

```
list1:[5, 4, 2, 0, 1, 3]
list2:[4, 2, 0]

list1:[0, 1, 2, 3, 4, 5]
list2:[0, 2, 4]

list1.containsAll(list2) : true
list1:[0, 1, 2, 3, 4, 5]
list2:[0, 2, 4, A, B, C]

list1:[0, 1, 2, 3, 4, 5]
list2:[0, 2, 4, AA, B, C]

list1.retainAll(list2) : true
list1:[0, 2, 4]
list2:[0, 2, 4, AA, B, C]

list1:[0, 2, 4]
list2:[AA, B, C]
```

---  





