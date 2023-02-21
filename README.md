# STUDY_JS
Java Script 학습 내용 정리


---

## Event

<details><summary><h4>Selectors</h4></summary>

- `document.querySelector("element");`  
  - 해당 JS 문서를 참조하는 HTML 문서 `document` 에 대하여,
  - 메소드 `querySelector` 은 `document` 의 요소 `element` 를 지목함
  
  - `element` 작성 형식은 다음과 같음
    - 전체 지목 시 `*` 을 기입함
    - 특정 태그 지목 시 해당 태그명을 기입함
    - 특정 클래스값 `className` 지목 시 `.className` 를 기입함
    - 특정 아이디값 `idName` 지목 시 `#idName` 을 기입함

- `document.querySelector("element0, element1, element2, ...");`
  - 해당 JS 문서를 참조하는 HTML 문서 `document` 에 대하여,
  - 메소드 `querySelectorall` 은 `document` 의 요소 `element0`, `element1`, `element2`, ... 를 지목함
  - `querySelectorall` 과 달리 여러 요소를 동시에 선택할 수 있음

- `document.getElementsByTagName("tagName");`  
  - 해당 JS 문서를 참조하는 HTML 문서 `document` 에 대하여,
  - 메소드 `getElementsByTagName` 은 `document` 의 태그 `tagName` 을 지목함
  
- `document.getElementsByClassName("className")[idx];`
  - 해당 JS 문서를 참조하는 HTML 문서 `document` 에 대하여,
  - 메소드 `getElementsByClassName` 은 `document` 의 클래스값 `className` 을 지목함
  - 특정 순번만 선택하고자 하는 경우 해당 순번을 `idx` 에 기입함
  
- `document.getElementsById("idName");`
  - 해당 JS 문서를 참조하는 HTML 문서 `document` 에 대하여,
  - 메소드 `getElementsById` 는 `document` 의 아이디값 `idName` 을 지목함

</details>

<details><summary><h4>Event Listener</h4></summary>
  
- `element.addEventListener("event", function);`  
  - Selector 을 통해 지목된 HTML 요소 `element` 에 대하여,
  - 메소드 `addEventListener` 은 이벤트 `event` 발생 시 함수 `function` 을 발생시킴
  - 이벤트 목록은 아래와 같음

    <table>
  <tr>
    <th>이벤트</th>
    <th>내용</th>
  </tr>
  <tr>
    <td>click</td>
    <td>해당 HTML 요소 클릭 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>mouseover</td>
    <td>마우스 포인터가 HTML 요소 위에 위치할 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>mouseout</td>
    <td>마우스 포인터가 해당 HTML 요소 범위에서 벗어났을 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>mousedown</td>
    <td>해당 HTML 요소를 클릭한 상태에서 손을 떼지 않고 드래그할 시 이벤트 발생</td>
  </tr>  
  <tr>
    <td>mouseup</td>
    <td>해당 HTML 요소를 클릭한 상태에서 드래그 후 손을 뗐을 때 이벤트 발생</td>
  </tr>
  <tr>
    <td>mousemove</td>
    <td>마우스 포인터 이동 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>focus</td>
    <td>해당 HTML 요소에 초점을 맞췄을 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>blur</td>
    <td>해당 HTML 요소에서 초점이 벗어났을 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>keypress</td>
    <td>키를 누르는 순간 이벤트 발생 및 지속</td>
  </tr>
  <tr>
    <td>keydown</td>
    <td>키를 누를 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>keyup</td>
    <td>키를 눌렀다가 떼는 순간 이벤트 발생</td>
  </tr>
  <tr>
    <td>load</td>
    <td>웹페이지에서 다운로드할 모든 파일을 다운로드 완료했을 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>resize</td>
    <td>브라우저 창 크기 조절 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>scroll</td>
    <td>웹페이지에 스크롤바가 존재할 경우, 스크롤바를 드래그하거나 키보드, 마우스 등을 활용하여 스크롤할 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>unload</td>
    <td>다른 웹페이지로 이동하거나 브라우저 탭 혹은 창을 종료할 시 이벤트 발생</td>
  </tr>
  <tr>
    <td>change</td>
    <td>Form 태그의 상태 변경 시 이벤트 발생</td>
  </tr>
  
</table>

</details>

---

## AJAX

<details><summary><h4>AJAX</h4></summary>

- **정의**
  - **A**synchronous **J**avaScript **a**nd **X**ML
  - `JavaScrpit` 와 `XML` 을 활용하는 비동기적 정보 교환 기법
  - 최근에는 서버와 클라이언트 간 교환할 데이터 양식으로서 `XML` 보다는 `JSON` 을 선호하는 추세임
  
- **JSON**  
  - **J**ava**S**cropt **O**bject **N**otation
  - 정보(value)에 대한 속성(key)을 쌍따옴표로 감싸는 객체(object)
  - 객체(object) : 속성과 정보가 쌍을 이루는 자료구조로서 python 의 dictionary 와 유사함
 
  - `JSON.stringify(object)`
    - 임의의 객체 `object`에 대하여,
    - `JSON` 의 메소드 `stringify` 는 `object` 의 자료형을 `JSON` 으로 변환한 값을 반환함
  
  - `JSON.parse(json)`
    - 임의의 json `json`에 대하여,
    - `JSON` 의 메소드 `parse` 는 `json` 의 자료형을 객체로 변환함

- 동기와 비동기  
  
</details>

<details><summary><h4>Request</h4></summary>

</details>

<details><summary><h4>State</h4></summary>

<table>
  <tr>
    <th>Value</th>
    <th>State</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>0</td>
    <td>XMLHttpRequest.UNSENT</td>
    <td>객체가 생성된 상태</td>
  </tr>
  <tr>
    <td>1</td>
    <td>XMLHttpRequest.OPENED</td>
    <td>메소드 open 이 호출된 상태</td>
  </tr>
  <tr>
    <td>2</td>
    <td>XMLHttpRequest.HEADERS_RECEIVED</td>
    <td>메소드 send 가 호출된 상태로서 응답 데이터를 받을 준비가 완료됨</td>
  </tr>
  <tr>
    <td>3</td>
    <td>XMLHttpRequest.LOADING</td>
    <td>요청 데이터를 처리 중인 상태로서 응답 데이터를 받는 중임</td>
  </tr>
  <tr>
    <td>4</td>
    <td>XMLHttpRequest.DONE</td>
    <td>응답 데이터를 모두 받아 응답할 준비가 완료된 상태</td>
  </tr>
  
</details>
