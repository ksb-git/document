# 명명규칙

시스템을 개발하는데 있어 표준 명명규칙을 적용하여

개발자 및 운영자가 소스코드 파악을 용이하게 하는것을 목적으로 한다.

## 0. 공통규칙

#### java 의 표기법은 파스칼 표기법과 카멜 표기법을 기본으로 사용한다.

- 파스칼 표기법 : 모든 단어에서 첫번째 문자는 대문자이며 나머지는 소문자이다.(예: PascalCase)
- 카멜 표기법 : 최초에 사용된 단어를 제외한 첫번째 문자가 대문자이며 나머지는 소문자이다.(예: camelCase)

#### 명칭에 대한 약어는 가급적 사용을 지양한다. (약어가 보편적으로 널리 알려진 경우 사용한다.)

- PostOffice (O), PstOff (X)
- Education (O), edu(O)

## 1. 패키지 명명규칙

- 패키지명은 한 단어의 명사를 사용한다.
  - com.member.object (O)
  - com.memberObject (X)

## 2. 클래스, 인터페이스 명명규칙

- 클래스, 인터페이스 명은 파스칼 표기법을 사용하며 어떤 의도로 작성된 것인지 알 수 있도록한다.
  - CommonDateUtil.java (O)
  - MyDateUtil.java (X)
  
- java 파일 하나에 한개의 public class 만을 가지도록 하며 inner class 를 사용하지 않는다.

- 변수명은 반드시 소문자로 시작하며 카멜 표기법을 사용한다.

#### Endpoint 클래스

- 메소드 명칭은 카멜 표기법을 사용한다.
  - getCompany, getDept, getDepartment
  
- 메소드명은 어떤 행위를 위한 기능인지 prefix 로 명시하고 상세 행위를 postfix 로 사용한다.
  
  | http method | prefix | method name |
  |:-----------:|:------:|:-----------|
  |GET|get|**get**Company|
  |GET|get|**get**Company**List**|
  |POST|create|**create**Company|
  |PUT|update|**update**Company|
  |DELETE|delete|**delete**Company|
  
#### Service 클래스

  - 메소드 명칭은 카멜 표기법을 사용한다.
  - 특별한 경우가 아닌경우 endpoint 메소드와 service 의 메소드는 1:1의 관계를 갖는다.
  - 1:1 관계의 서비스 메소드는 endpoint 의 메소드명과 동인한 이름을 사용한다.
    - endpoint : getCompany 
    - service : getCompany
    
#### Repository, Mapper 인터페이스

  - DB 에 접근하여 수행할 작업을 메소드명에 prefix 로 명시한다.

| job | prefix | method name |
|:-----------:|:------:|:-----------|
|select|find|**find**Company|
|insert|create|**create**Company|
|update|update|**update**Company|
|delete|delete|**delete**Company|
