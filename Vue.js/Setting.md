# Vue.js 세팅
> vue.js 환경설정을 위해 우선 [node.js](https://nodejs.org/en)를 설치한다.
>
> 권장 IDE : VsCdoe
> 권장사항 : VsCode에 vetur, vue3 snippets, html css support 확장자를 설치

## @vue/cli 설치
 ```Terminal
npm install -g @vue/cli
```
* 명령어 입력 시 설치 옵션 선택 문구 -> (please pick a preset ~)
default vue2
deafut vue 3
Manually select features : 직접 옵션들을 선택하겠다.
방향키로 vue3선택 후 엔터

##  프로젝트 생성
 ```Terminal
vue create 프로젝트명
 ```

## vue 프로젝트 기본 구조
* node_modules: 프로젝트에 쓰는 라이브러리 폴더
* public
  * index.html : 웹 브라우저는 .vue파일을 해석 불가
      * 실제로는 app.vue파일을 index.html파일에 모아 렌더링 => 이 때문에 뷰를 single page application이라고 부름
* src: 소스 폴더
* assets: 자산 파일 폴더(font, icons,images, style 등)
* components: 컴포넌트 폴더
* App.vue: 최상위 컨테이너 뷰
* main.js: 애플리케이션 진입점. App.vue 파일을 로드

### main.js 기본 형식
```javascript
import { createApp } from 'vue'
import App from './App.vue'
createApp(App).mount('#app')
``` 
