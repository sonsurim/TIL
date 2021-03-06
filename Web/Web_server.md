# 웹 서버
<img src="./images/server2.png" width="600">

- 클라이언트와 서버 간에는 보통 HTTP를 통해서 통신을 하게 됨
  > URL 주소가 HTTP로 시작되는 이유: HTTP를 사용한다는 것을 의미

  - 웹 브라우저를 실행한 후 주소 입력창에 URL 주소를 입력하면 그 URL주소에 해당하는 결과물이 화면에 보임

  - 현실에서 주소를 보고 집을 찾아가는 것처럼 웹 브라우저는 URL 주소로 해당하는 웹 서버에 연결하고 해당 주소에서 볼 수 있는 내용을 읽어 들여 보여주게 됨

## 정의 📋
- **하드웨어**
  - 웹 서버가 설치되어 있는 컴퓨터

- **소프트웨어**
  - 웹 브라우저 클라이언트로부터 HTTP 요청을 받아 정적인 컨텐츠를 제공하는 컴퓨터 프로그램

## 특징 🙌
- 일반적으로 소프트웨어를 가리킴
- 웹 서버의 가장 중요한 기능은 클라이언트(웹 브라우저)가 요청하는 HTML문서나 각종 리소스를 전달하는 것
  1. `웹 브라우저, 웹 크롤러`가 웹 서버에게 HTTP에 맞도록 리소스를 요청
  2. `웹 서버`는 요청한 리소스를 반환하며 리소스가 존재하지 않거나 전송할 때 문제가 발생되는 경우, 에러메시지를 전송

- 웹 브라우저나 <u>웹 크롤러</u>가 요청하는 리소스는 컴퓨터에 저장된 <u>정적 데이터</u>이거나 <u>동적인 결과</u>가 될 수 있음
  > **웹 크롤러**? 네이버, 구글 같은 검색 사이트에서 다른 웹 사이트 정보를 읽어갈 때 사용하는 소프트웨어

  > **정적인 데이터**? 이미지, HTML 파일, CSS 파일, JS 파일 같은 컴퓨터에 저장되어 있는 파일들을 의미

  > **동적인 결과**? 웹 서버에 의해서 실행되는 프로그램을 통해서 만들어진 결과물

## 웹 서버가 필요한 이유 🤔
Ex. 클라이언트 (웹 브라우저)에 이미지 파일(정적 컨텐츠)을 보내는 과정

- 정적인 파일들은 웹 문서(HTML)가 클라이언트로 보내질 때 함께 가지 않음
- 클라이언트는 HTML 문서를 먼저 받음
- HTML문서에 필요한 이미지 파일을 다시 서버로 요청하고 받아옴
- 웹 서버를 통해 정적인 파일들을 애플리케이션 서버까지 가지 않고 앞단에서 빠르게 전송 가능

→ **정적 컨텐츠만 처리하도록 기능을 분배하여 서버의 부담 감소**


## 웹 서버 소프트웨어의 종류 🔩
- **Apache**
  - 오픈 소스 소프트웨어
  - 거의 대부분 운영체제에서 사용 가능
- **Nginx**
  - 차세대 웹 서버로 불리움
  - 오픈 소스 소프트웨어
  - 더 적은 자원으로 더 빠르게 데이터를 서비스하는 것을 목적으로 만들어진 서버
- **Microsoft**
- **Google Web Server**

## 네이버로 알아보는 웹 브라우저 - 웹 서버의 통신 🌐
<img src="./images/naver.png" width="600">
<img src="./images/naver2.png" width="600">

1. 웹 브라우저는 `www.naver.com`이라는 웹 서버에 접속
2. 해당 주소에 기본으로 보여지는 HTML 문서를 요청
3. 웹 서버는 사용자가 요청한 HTML문서를 웹 브라우저에게 전달
4. 웹 브라우저는 웹 서버로부터 전송받은 HTML 문서를 읽어들인 후 해석
5. HTML 문서를 알맞게 보여주기 위해 필요한 이미지, CSS, JavaScript와 같은 리소스들에 대해 URL을 추출
6. 해당 URL로 웹 서버에게 동시에 여러 개의 리소스를 요청
7. 웹 서버는 동시에 요청한 여러 개의 요청을 받아들여 그 결과를 브라우저에 전송
8. 웹 브라우저는 아까 해석했던 HTML 문서와 읽어들인 여러 개의 응답을 하나로 합쳐서 그 결과를 화면에 출력 (렌더링)


- - -
위의 내용은 Web을 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [부스트코스 - 웹 프로그래밍 강의](https://www.boostcourse.org/web316/lecture/16661?isDesc=false)
- [블로그 - gmlwjd9405](https://gmlwjd9405.github.io/2018/10/27/webserver-vs-was.html)