# CRUD Twitter Clone Coding

### 프로젝트 목적

---

### 주요 기능

---

### 실행 결과

---

### 개념 정리

- Firebase

  - firebase는 처음엔 database에서 시작, 지금의 firebase는 back-end 기능을 포괄하고 그 기능들을 제공해주는 것

- Cloud firestore

  - 백엔드의 cloud firestore 사용, 데이터베이스 관련 코드없이 데이터베이스를 사용하게 해준다.

- Cloud storage

  - cloud storage는 aws의 s3과 비슷하다.
    기본적으로 업로드의 기능(사진을 업로드)

- Hosting

  - hosting 배포하기 위한 기능

- Authentication
  - firebase의 중요한 핵심 기능, 이미 구현된 authentication을 이용하면 짧은 시간에 구현 가능

---

### 진행하는 과정

#### App.js

1. 유저의 상태가 변화하면 그 변화된 정보로 유저를 변경해준다. (update)
2. `<AppRouter/>` 컴포넌트는 3개의 인자값을 가지게 된다.
   - refreshUser : 유저의 정보를 갱신해주는 함수
   - isLoggedIn : 로그인이 되었는지 판별하기 위한 값
   - userObj : 유저의 정보를 담고 있는 객체 (state 값)

#### Router.js

1. isLoggedIn 이 true면

- Navigation 컴포넌트 실행
- 홈 아이콘을 클릭하면 Home 컴포넌트 실행 , 프로필 아이콘을 클릭하면 Profile 컴포넌트 실행

2. isLoggedIn 이 false면

- Auth 컴포넌트를 실행

#### Navigation.js

1. 홈 아이콘과 프로필 아이콘을 작성한다 (FontAwesomeIcon)

#### NweetFactory.js

1. 텍스트와 사진을 함께 작성할 수 있게 틀을 작성한다

### Nweet.js

1. 작성된 트윗들을 보여주고 그 트윗을 수정할 수 있게 해준다.

#### Auth.js [로그인 화면]

1. 이메일, 비밀번호로 로그인

- 계정을 생성하여 Firebase에 저장할 수 있다
- 이메일이나 비밀번호에 에러가 있으면 에러메세지가 표시된다

2. Google 아이디를 이용하여 로그인
3. Github 아이디를 이용하여 로그인

#### Home.js [메인 화면]

1. 트윗을 작성하거나 삭제한다
2. NweetFactory 컴포넌트 실행
3. Nweet 컴포넌트 실행

#### Profile.js [프로필 화면]

1. 프로필을 수정할 수 있고 로그아웃 기능이 있다.

---

#### Fbase.js [Firebase 설정]

### firebase 설정들을 모아놓은 컴포넌트

- firebaseConfig
- firebase
- firebase.auth()
- firebase.firestore()
- firebase.storage()
