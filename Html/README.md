# HTML (HyperText Markup Language)

## 특징 🙌
- HTML 문서는 html이라는 태그로 시작해서 html 태그로 끝난다
- HTML은 계층적이다
- HTML은 tag를 사용해서 표현한다
  ```
  <tag class="title">안녕하세요</tag>
  ```
- JavaScript와 CSS는 html 여러군데 존재 가능
  - **JavaScript 코드는** 렌더링에 방해받지 않기 위해(JS 코드를 다운로드 받고 해석하느라 HTML 해석이 느려지지않게) **`body` 태그 닫히기 직전에 위치하는 것이 좋다**
  - **CSS 코드는** 렌더링 처리 시, 브라우저가 더 빨리 참고할 수 있게 **`head`안에 위치하는 것이 좋다.**

## 구조 🔩
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
  <script src="./main.js"></script>
  </body>
</html>
```
- `<!DOCTYPE html>`: 문서의 타입, HTML의 시작을 알림
- `html lang="en"`: html 언어는 en
- `meta`: 문서에 대한 정보
  - `meta charset="UTF-8"`: 문서의 Charset은 utf-8
  - `meta name="viewport content="width=device-width"`: 모바일의 경우 view를 어떻게 보여줄 지 정의
- `title`: title에 대한 정보
- `body`: 화면의 내용을 담고 있음
- `<script src="./main.js"></script>`
  - 브라우저에서 `main.js`파일만 서버로 요청을 보내서 받아옴
  - `main.js` 파일을 바로 해석
  - 바로 실행되어야 할 JavaScript 코드가 있는 경우, 먼저 실행
  - 실행이 끝난 경우, 다시 html 문서를 해석

## head ⚙️
- 어떤 문서에 대한 자세한 정보들이 포함되어 있음
- 눈에 보이는 것을 정의하지 않고 HTML 문서에 대한 추가적인 정보를 정의

## body ⚙️
- 화면에 그려질 태그들이 포함되어 있음

- - -
위의 내용은 Html을 공부하며 개인적으로 정리한 내용입니다.
## 출처 📝
- [부스트코스 - 웹 프로그래밍 강의](https://www.boostcourse.org/web316/lecture/16661?isDesc=false)