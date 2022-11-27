# 코딩테스트 단골 Java 개념

> 코딩테스트에서 자주 활용되는 Java 개념 및 문법 정리

## 1. 문자열 다루기

### 1-1. String 클래스

## 2. 배열 다루기

### 2-1. Arrays 클래스

배열을 다루는데 유용한 **static 메서드**들이 정의된 클래스

* 배열 비교 : 반환타입 `boolean`
  
  배열의 모든 요소를 비교해서 같으면 true, 다르면 false 반환
  
  * 1차원과 다차원(2차원 이상) 배열의 메서드를 구별해서 사용해야함
    
    1. 1차원 배열 비교 : `Arrays.equals(arr1, array2)`
    
    2. 다차원 배열 비교 : `Arrays.deepEquals(arr1, arr2)`

* 배열 복사 : 반환타입 `Object[]`
  
  * 전체 복사 : `Arrays.copyOf(arr, length)`
  * 일부 복사 : `Arrays.copyOfRange(arr,startIdx,endIdx)`
    * 복사되는 범위는 startIdx <= element < endIdx

* 배열 채우기
  
  특정값으로 배열 초기화 시 사용하면 좋음
  
  * `Arrays.fill(arr, 특정값)`
  
  * `Arrays.setAll(arr, 람다식)`

* 배열 출력 
  
  * 1차원과 다차원 배열의 메서드를 구별해서 사용해야함
    1. 1차원 배열 출력 : `Arrays.toString(arr)`
    
    2. 다차원 배열 출력 : `Arrays.deepToString(arr)`

## 3. 수학

## 참고(Reference)

* [(기술 서적) Java의 정석 - 저자 남궁 성 / 출판사 도우출판]([Java의 정석 - YES24](http://www.yes24.com/Product/Goods/24259565))
