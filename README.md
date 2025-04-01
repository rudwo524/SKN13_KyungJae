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



#### import mypackage.weight_helper, mypackage.calculator
#### mypackage.weight_helper.check_bmi(1.7, 60)
#### mypackage.calculator.plus(10, 20)

에 비해 from 절을 쓰는게 더 편하다

#### from mypackage import weight_helper as wh, calculator as c
#### wh.check_bmi(1.9, 90)
#### c.plus(100, 200)




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

  Exception(예외) : 오류 중 처리가능한 것을
  
  Exception Handling : 그 예외를 처리하는 것


### try, except 구문

![image](https://github.com/user-attachments/assets/df82a14f-996e-4570-a8a0-e3ee7f2997b5)


### finally 구문
- 예외 발생여부, 처리 여부와 관계없이 무조건 실행되는 코드블록
    - try 구문에 **반드시 실행되야 하는 코드블록을 작성할때 사용한다.**
    - 보통 프로그램이 외부자원과 연결해서 데이터를 주고 받는 작업을 할때 마지막 연결을 종료하는 작업을 finally 블록에 넣는다.
- finally 는 except 보다 먼저 올 수 없다.
    - 구문순서
        1. try - except - finally
        2. try - except
        3. try - finally


### Call Stack Mechanism
Data Structure
  - Stack: First-In-Last-Out
  - Queue: First-In-First-Out

