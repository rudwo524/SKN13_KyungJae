# SKN13
SK Network 13기 과정 수업소스
수업코드는 여기서 공유합니다. 









# 2주차
## 0331




### 0401

모듈 - 패키지 - import(구문)    구조가 이루어져 있음

내장함수는 python에서 바로 쓸 수 있는 반면에 
모듈파일에 작성된 함수나 클래스들을 다른 python 프로그램에서 호출 하여 사용할 수 있다. (단 사용하기 위해서는 import 를 먼저 해야 함)4

모듈(Module)
- 표준 모듈 : 파이썬에 저장된 모듈
- 사용자 정의 모듈 : 개발자가 재사용을 위해 직접 만든 모듈
- 3rd party 모듈 : 특정 개발업자 or 개발자들이 만들어 배포하는 모듈
                   사용자 정의 모듈도 배포해서 다른 곳에서 사용하게 되면 3rd party모듈이 된다

패키지(Package) : 모듈들을 저장한 디렉토리
- python에서는 라이브러리를 패키지라고 함.
- root package : root directory와 비슷하게 최상위 패키지를 의미한다

%%writefile 파일경로 -> cell의 잘성한 내용을 경로의 파일에 작성(저장.) -> cell의 첫 줄에 넣어야함.

import : 사용할 모듈을 정의
import 구문: [from 사용할 것의 경로] import 사용할 것 [as 별칭] [, 사용할 것 [as 별칭], ...]
- []: 생략가능
사용할 것:
- 모듈, 모듈안에 정의된 variable, function, class



import mypackage.weight_helper, mypackage.calculator   
mypackage.weight_helper.check_bmi(1.7, 60)   
mypackage.calculator.plus(10, 20)   
에 비해 from 절을 쓰는게 더 편하다

from mypackage import weight_helper as wh, calculator as c   
wh.check_bmi(1.9, 90)   
c.plus(100, 200)




- import할때 이미 같은 이름의 함수가 있는 경우 덮어씌워짐



#### pip install pandas  // pandas 설치
  
pip show pandas : install 된 것의 license를 출력해줌

### 오류
1. 처리 가능한 오류:
- 실행 환경의 문제로 발생하는 오류
- 사용자가 매뉴얼대로 실행하지 않았거나 잘못된 환경에서 실행한 경우.
- 코드작성 할 때는 실행시 Exception 발생 할지 여부를 알 수 없다.
- 만약 발생할 경우 어떻게 처리할지를 구현해야 한다.

2. 수정해야 하는 오류:
- 코드 상 100% 발생하는 오류
- 코드를 잘못 작성한 경우로 코드를 수정해야한다.
- 보통 이런 오류는 컴파일 방식 언어의 경우 컴파일 때 에러를 내서 수정하도록 한다.

### Exception Handling(예외 처리)

  Exception: 함수나 메소드가 처리 도중 다음 명령문을 실행할 수 없는 상황   
  Exception(예외) : 오류 중 처리가능한 것   
  Exception Handling : 그 예외를 처리하는 것   

### try, except 구문

![image](https://github.com/user-attachments/assets/df82a14f-996e-4570-a8a0-e3ee7f2997b5)


### finally 구문
- 예외 발생여부, **처리 여부와 관계없이** 무조건 실행되는 코드블록
    - try 구문에 **반드시 실행되야 하는 코드블록을 작성할때 사용한다.**
    - 보통 프로그램이 외부자원과 연결해서 데이터를 주고 받는 작업을 할때 마지막 연결을 종료하는 작업을 finally 블록에 넣는다.
- finally 는 except 보다 먼저 올 수 없다.
    - 구문순서
      - try - except - finally
      - try - except
      - try - finally


### Call Stack Mechanism
Data Structure
  - Stack: First-In-Last-Out
  - Queue: First-In-First-Out

### 사용자 정의 Exception 클래스 구현


## 0402

### 어제 꺼 review(패키지 모듈, exception 처리)

모듈(python script file) -> 재사용가능한 코드들(class, variables, functions)


### 입출력/IO -> Input/Output

외부 --------> Program ---------> 외부
        Input                  Output

1. 연결
2. 읽기
3. 연결 닫기   

root node(directory) / .. / current directory / file





















           
가 ----------->(encoding) 2진수 ------------>(decoding) 가     



open(파일경로, "rb")   
a.read(): bytes


a = open(파일경로, "wb)
a.write(bytes)







## Database

DB - 지속적으로 유지, 관리되어야 하는 데이터들의 집합

RDB : Relational Database

DBMS : 

## SQL(Structured Query Language)



### Query문

#### DML(Data Manipulation Language)

INSERT : 

DELETE :  
 
UPDATE: 

SELECT :

#### DDL(Data Definition Language)

CREATE : 

ALTER:

DROP:

TRUNCATE(?) : Clear Data

#### DCL(Data Control Language)

GRANT:

REVOKE:


#### user_id 만들기

create 뭘만들지 나머지설정   
create user my_id@localhost identified by 1111


username: my_id
passwd:1111


계정 만들 수 있는 권한 필요



## 데이터 타입

- 문자열
   
   - CHAR(n)
    - varchar(n0
    - TINYNEXT
    - TEXT
    - MEDIUMTEXT(n)
    - LONGTEXT(n)

- Number
   
   -정수
         - TINYINT
         - BOOLEAN
         -SMALLINT
         -INT
         -BIGINT
   
   -실수
        - DECIMAL
        - FLOAT
        - DOUBLE

- 날짜

- DATE
    - TIME
    - DATETIME
    - YEAR

- 결측치

   
   -NULL
    -없는 값, 모르는 값, 수집되지 않은 값

## KEY값

- PRIMARY KEY

- FOREIGN KEY

- UNIQUE KEY





git에서 글로빙은
    - ?: 한 글자
    - *: 공백부터 여러 글자까지 가능

sql에서는
    - _: 한 글자
    - %: 여러 글자

## 함수

단일 행 함수
- 행 단위로 값을 처리하는 함수
- 단일행은 select, where 절에서 사용가능
- 함수에 함수를 넣어 여러 처리를 한번애 할 수 있다.
    - CHAR_LENGTH(CONCAT('A', 'B'))

다중 행 함수
- 여러 행의 값들을 묶어서  한번에 처리하는 함수
- 집계함수, 그룹함수라고도 한다.
- 다중행은 select, having 절에서 사용가능
- where절에서 사용 x(subquery 이용)

함수 - 조건 처리 함수

- if(조건수식, 참, 거짓)
    - 조건수식이 True이면 참, False이면 거짓 을 출력

- ifnull(기준컬럼(값), 기본값)
    - 





함수 - 날짜, 시간 처리 함수










