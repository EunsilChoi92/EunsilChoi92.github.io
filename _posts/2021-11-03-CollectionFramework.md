---
title: "컬렉션 프레임워크(Collection Framework)"
categories: ['Java']
---



# 컬렉션 프레임워크(Colleciton Framework)



## 컬렉션이란?

사전적 의미로 요소를 수집해서 저장하는 것을 말하는데, 자바 컬렉션은 객체를 수집해서 저장하는 역할을 한다. 주요 인터페이스로는 `List`, `Set`, `Map`이 있다.



## 배열의 문제점

배열은 쉽게 생성하고 사용할 수 있지만, 저장할 수 있는 객체 수가 배열을 생성할 때 결정되기 때문에 불특정 다수의 객체를 저장하기에는 문제가 있다. 

```java
// 길이가 10인 배열 생성
Product[] array = new Product[10];
// 객체 추가
array[0] = new Product("Model1");
array[1] = new Product("Model2");
// 객체 검색
Product model1 = array[0];
product model2 = array[1];
// 객체 삭제
array[0] = null;
array[1] = null;
```

게다가 객체를 삭제했을 때 해당 인덱스가 비게 되어 새로운 객체를 저장하려면 어디가 비어 있는지 확인하는 코드가 필요하다.



## 컬렉션 프레임워크

자바는 배열의 이러한 문제점을 해결하고, 널리 알려져 있는 자료구조(Data Structure)를 바탕으로 객체들을 효율적으로 추가, 삭제, 검색할 수 있도록 `java.utill` 패키지에 컬렉션과 관련된 인터페이스와 클래스들을 포함시켜 놓았다.

이들을 총칭해서 컬렉션 프레임워크(Collection Framework)라고 부른다.

![collection](https://raw.githubusercontent.com/EunsilChoi92/EunsilChoi92.github.io/main/assets/images/collection.png)



`List`와 `Set`은 객체를 추가, 삭제, 검색하는 방법에 많은 공통점이 있기 때문에 이 인터페이스들의 공통된 메소들만 모아 Collection 인터페이스로 정의해 두고 있다. `Map`은 키와 값을 하나의 쌍으로 묶어서 관리하는 구조로 되어 있어, `List` 및 `Set`과는 사용 방법이 완전히 다르다.

![collection2](https://raw.githubusercontent.com/EunsilChoi92/EunsilChoi92.github.io/main/assets/images/collection2.png)

