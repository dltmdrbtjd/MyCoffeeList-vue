# Vue-Practice
- Vue 공식문서를 참고하여 간단한 예제 연습 및 일기장 프로젝트 완성하기
- 추후에 최종적인 목표는 CRUD가 가능한 간단한 todo-list 형태의 프로젝트를 만드는 것이다.

## 프로젝트 기록
### 2021.10.13
- 구현한 내용
  - axios를 통해서 json-server에서 list를 받아와 data에 담기
  - 받아온 list를 통해서 v-for 디렉티브를 사용하여 화면에 뿌려주기
  - v-on 디렉티브를 사용하여 상세정보 모달로 보기
- 간단한 회고
  - 우선 axios를 모듈화해서 서버에서 데이터를 불러오는 기본적인 과정은 React를 공부했을때와 전혀 다른점이 없었다. 그래서 크게 어려움없이 json-server를 이용해서 서버에서 데이터를 불러오는 과정을 연습해볼 수 있었다.
  - React를 사용했을때 useEffect를 이용해 처음 렌더링시 서버에서 데이터를 불러오는 형태로 사용했었는데 Vue에서도 비슷한 개념이기는 하다. 우선 methods에서 서버에서 데이터를 받아오는 로직을 구현하고 created 라이프사이클 훅을 통해서 처음 Vue가 생성될 시점에 앞에서 만든 methods를 실행하는 방향으로 제작하였다.
  - v-for문을 이용한 반복문 사용에서 느낀 React와의 차이점은 React는 반복문을 여러가지 형태로 사용할 수 있다. 예를들면 map도 가능하고 forEach도 가능하고 for문 기타 등등이 존재하는데 Vue는 v-for라는 딱 정해진 방식이 있기때문에 좀 더 편하게 사용할 수 있다는 생각이 들었다. 실제로 v-for를 사용하는 문법은 python에서 반복문을 사용할때와 똑같다고 생각했다. 추가로 key를 강제적으로 사용하여야 한다는 점도있었다.
  - v-on을 이용해서 이벤트를 사용할 수 있고 v-bind를 이용해 데이터를 바인드할 수 있었다. 추가로 v-on은 '@'로 대체해서 사용할 수 있고 v-bind는 ':'로 대체해서 사용할 수 있다. 하지만 이번에는 기초적인 내용들을 다 집고 넘어가고 싶어서 단축해서 사용하지는 않았지만 앞으로 유용하게 사용하게 될 것 같다.
- 추가로 공부할 내용
  - VueX , Vue Router 사용방법
  - Vue에서 컴포넌트를 분리하는법
  - Vue에서 props의 이동 파악하기
  - 다른 라이프사이클 메소드 사용

### 2021.10.17
- 구현한 내용
  - vuex, vue-router, vuetify 셋팅완료
  - HomeContent 컴포넌트로 기본 content style
  - Main에서 기본 style 설정( 배경색, 폰트사이즈 등등 )
  - python flask를 이용해서 server생성 ( mongodb사용 )
- 간단한 회고
  - 일단 vue에 관해서 기초적인 내용들은 강의와 공식문서를 통해서 공부를 어느정도 끝낸것같다. 그래서 이제 직접 프로젝트를 개발해보면서 부딪히는 문제들을 해결해나가면 좀 더 vue와 가까워질 수 있을것 같다!
  - 추가적으로 crud를 모두 구현할 계획이라서 서버가 필요하여서 python flask를 이용해서 간단하게 서버를 만들어서 같이 개발할 계획이다.
  - 일단 composition api를 무조건 사용하냐?의 궁금이 많이있고 그리고 vuex의 모듈화를 어떤식으로 하면 좋을지 고민이다.
- 추가로 공부할 내용
  - vuex 모듈화하기
  - 이제 나머지 공부한 내용들을 토대로 까먹은 부분이나 새로운 부분들에 대해서 그때그때 부딪혀 나가면서 공부하면 될 것 같다.

### 2021.10.19
- 에러발생
  - express 설치후 에러 발생으로 인해서 vue가 실행되지 않았다. 롤백도 해보고 다시 설치해보고 패키지도 지웠다 다시 설치해도 도저히 해결할 방법을 못찾았다... 차라리 레포를 지우고 새로 하는게 빠를것 같아서 전체 삭제후 새로 작업하기로 결정.
  - 기존에 flask를 사용해서 서버를 만들었는데 환경설정이랑 패키지 쪽에서 자꾸 오류가 발생해서 express로 대체하여 개발할 계획이다. 우선 오늘 에러만 6시간 넘게 잡으려다가 실패해서 시간을 다날려버렸다. 일단 모두 삭제하고 새로 시작하는게 더 빠를것으로 판단.

### 2021.11.07
- Vue : 기본골격이랑 뷰는 모두 끝내었음 우선 데이터만 핸들링하면 끝. 우선은 추가로 nuxt공부후에 nuxt도 추가로 정리해야겠음.
- Golang : mongodb 연결도 되었고 server도 띄웠지만 도저히 mongodb find로 배열 반환시에 제대로된 json형태의 배열을 받아오는게 계속 실패해서 우선 잠정적으로 여기까지만 작업하고 추후에 제대로 숙지가 되면 그때 다시 해야겠음.

### 2021.12.01
- 아래 프로젝트들로 대체하여 원래 이 프로젝트에서 구현하려고 했던 내용을 go를 이용해서 구현 완료
backend : https://github.com/dltmdrbtjd/go-gin-gorm-prac
frontend : https://github.com/dltmdrbtjd/vue-todolist
