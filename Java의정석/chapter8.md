# 1
- 정의 : 프로그램 실행 시 발생할 수 있는 상황을 예외로 따로 대비한 코드
- 목정 : 비정상 종료를 막고, 정상적인 실행상태 유지하는 것

# 2
d : method1 - method2 순서이다

# 3
d, e : 상위 클래스의 메서드보다 수가 적어야 한다.

# 4
c : 모든 예외를 저장하는 Exception은 마지막에 처리해야 한다.

# 5
1  
3  
5  
1  
2  
5  
6  


# 6
3  
5

# 7
1

# 8
try-catch 문을 추가한다.
```java
try {
	input = new Scanner(System.in).nextInt();
} catch(Exception e) {
	System.out.println("다시 입력");
	continue;
}
```

# 9
2  
4  
7
