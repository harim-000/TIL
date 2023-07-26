# Vue 시작하기

> Vue.js 시작하기 - Age of Vue.js - Captain Pangyo [링크](https://www.inflearn.com/course/vue-pwa-vue-js-%EA%B8%B0%EB%B3%B8/)

## Vue는 무엇인가?

* MVVM 패턴의 ViewModel 레이어에 해당하는 View 단 라이브러리
  * MVVM - 모델(MODEl) - 뷰(VIEW) - 뷰 모델(ViewModel)로 구조화
  * 모델과 뷰 사이에 뷰모델이 위치하는 구조
  * Model : 어플리케이션에서 사용되는 데이터와 그 데이터를 처리
  * View : 사용자에서 보여지는 UI.
  * View Model : View를 표현하기 위해 만든 View를 위한 Model입니다. View를 나타내 주기 위한 Model이자 View를 나타내기 위한 데이터 처리.
  * DOM이 변경됐을 때, 뷰모델의 DOM Listeners를 거쳐서 모델로 신호가 간다.
  * 모델에서 변경된 데이터를 뷰모델을 거쳐서 뷰로 보냈을 때, 화면이 reactive하게 반응이 일어난다.
  * Vue.js 는 이와 같이 reactive한 프로그래밍이 가능하게 끔 뷰단에서 모든 것을 제어하는 뷰모델 라이브러리.

## MVVM 패턴이란?
 * Backend 로직과 Client 의 마크업 & 데이터 표현단을 분리하기 위한 구조로 전통적인 MVC 패턴의 방식에서 나온 것.
 * ViewModel은 화면 앞단의 회면 동작 관련 로직과 뒷단의 DB 데이터 처리 및 서버 로직을 분리하고, 뒷단에서 넘어온 데이터를 Model 에 담아 View 로 넘어주는 중간 지점. 
 * 이러한 방식으로 개발하는 이유는 화면의 요소들을 제어하는 코드와 데이터 제어 로직을 분리하여 코드를 더 직관적으로 이해할 수 있어 유지보수가 편해지기 때문.

![](https://github.com/namjunemy/TIL/blob/master/Vue/img/01.PNG?raw=true)



* 데이터 바인딩과 화면 단위를 컴포넌트 형태로 제공하며, 관련 API를 지원하는데에 궁극적인 목적이 있음
* Angular에서 지원하는 2 way data bindings을 동일하게 제공
* 하지만 Component 간 통신의 기본 골격은 React의 1way data flow(부모 -> 자식)와 유사
* Virtual DOM을 이용한 렌더링 방식이 React와 거의 유사
* 다른 Front-End FW(Angular, React)와 비교했을 때 훨씬 가볍고 빠름
* 간단한 Vue를 적용하는데 있어서도 러닝커브가 낮고, 쉽게 접근 가능

## Hello Vue.js

* index.html

```vue
<html>
<head>
  <title>Vue Sample</title>
</head>
<body>
  <div id="app">
    {{ message }}
  </div>

  <script src="https://unpkg.com/vue@2.3.3"></script>
  <script>
    new Vue({
      el: '#app',
      data: {
        message: 'Hello Vue.js!!'
      }
    })
  </script>
</body>
</html>
```
