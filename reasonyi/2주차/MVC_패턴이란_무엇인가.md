# MCV 패턴이란 무엇인가?

## MVC 패턴이란?

model-view-controller를 뜻하는 것으로, 소프트웨어 디자인 패턴이다.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ea7e2bec-58fd-407d-ace0-0294caef4726/0aa03279-2a2a-427d-bd7a-a4c56a215d07/Untitled.png)

사용자가 Controller를 조작하면, Controller는 Model을 통해 데이터를 가져오고, 그 데이터를 바탕으로 View를 통해 시각적 표현을 제어하여 사용자에게 전달한다.

### Controller

클라이언트의 요청을 받았을 때, 실제 업무를 수행할 Model을 호출한다. 

클라이언트에서 데이터를 보낸 경우 Model에 전달하기 쉽도록 가공한다. 

Model에서 나온 결과를 View에 전달한다.

### Model

Controller가 호출할 때, 요청에 맞는 역할을 수행한다. 

데이터를 처리하는 부분으로, DB에 연결하고 데이터를 추출, 저장, 삭제, 업데이트, 변환 등의 작업을 수행한다.

### View

Controller로부터 받은 모델의 결과값을 가지고 사용자에게 출력할 화면을 만든다. 

만들어진 화면을 웹브라우저에 전송하여 웹브라우저가 출력하게 한다.

MVC 패턴 방식에는 모델1 방식과 모델2 방식이 있다. 

- 모델1 방식: Controller 영역에 View를 같이 구현하는 방식이며, 사용자의 요청을 JSP가 전부 처리한다.
- 모델2 방식: HTML소스와 JAVA소스를 분리하여 모델1에 비해 확장과 유지보수가 쉽다.

|  | Model1 | Model2 |
| --- | --- | --- |
| 장점 | 빠르고 쉽게 개발 가능 | 디자이너와 개발자의 분업 가능, 유지보수 및 확장이 쉬움 |
| 단점 | JSP파일이 너무 비대해지며 Controller와 View가 함께 있어 유지보수가 어려움 | 설계가 어렵고 개발 난이도가 높음 |

대부분 Model2방식을 사용한다.

## MVC 패턴을 사용해야 하는 이유

- 비즈니스 로직과 UI 로직을 분리하여 유지보수를 독립적으로 수행 가능
- Model과 View가 다른 컴포넌트에 종속되지 않아 프로그램의 확장성, 유연성에 유리함
- 중복 코딩의 문제점을 제거함

 

참고자료

https://cocoon1787.tistory.com/733

http://asfirstalways.tistory.com/180
