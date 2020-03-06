# Blended Frontend Small Project (ReactNative)

# Movies & Series

현재 인기 있는 영화, 가장 최신의 영화 목록을 보여주고 선택한 영화 및 캐스팅의 상세 내용을 표시하는 앱을
만듭니다.

## 요구 사항

- ReactNative를 사용하여 구현합니다.
  - 프로젝트 시작 시 CLI 혹은 Expo 모두 사용할 수 있습니다.
- 필요한 부분에 적절히 외부 라이브러리를 사용할 수 있습니다.
  - 네비게이션
  - LinearGradient
  - 기타 필요하다고 판단되는 경우
- 각 화면 별로 준비된 [목업](https://www.figma.com/file/7Tr5BCjrIvIsBxxCFJjdDj/movies-app-davor-naumoski?node-id=0%3A583)에 맞게 유저 스토리를 구현합니다.
  - 구현된 기능은 iOS 시뮬레이터에서만 구동이 가능하면 됩니다. (Android 호환 불필요)
  - 폰트는 시스템 기본 폰트를 사용하면 됩니다.

## 유저 스토리

### Landing

- 앱을 처음 켰을 때 보이는 화면입니다.
- 하단의 Explore Collection 버튼을 누르면 Discover 페이지로 이동합니다.

### Discover

- 가로로된 두 개의 목록을 표시합니다 - Most Popular, Most Recent
- 각각의 목록은 API에서 한 번에 반환하는 만큼만 표시하면 됩니다. (더 불러오기 기능 불필요)
  - [Most Popular](https://developers.themoviedb.org/3/movies/get-popular-movies)
  - [Most Recent](https://developers.themoviedb.org/3/movies/get-now-playing)
- 목록 내의 영화 카드를 누르면 Movie Details 페이지로 이동합니다.
- 하단의 탭은 목업과 같이 구현 하되 Genres와 Artists 탭을 누르면 빈 페이지를 표시합니다.
- 상단 우측의 돋보기 아이콘은 눌렀을 때 아무 작동도 하지 않아도 됩니다.

### Movie Details - Cast

- 영화 상세 페이지를 목업에 맞게 구현합니다.
- 영화에 대한 상세 정보는 아래 API에서 얻을 수 있습니다.
  - [movie](https://developers.themoviedb.org/3/movies/get-movie-details)
  - [credits](https://developers.themoviedb.org/3/movies/get-movie-credits)
- 영화의 상영 날짜는 API가 보내준 형식 그대로 표시하여도 됩니다.
- overview는 3줄만 표시하다가 view all을 누르면 전체 내용을 표시합니다.
- rating에 사용되는 별의 스타일은 Symbols -> Rating Card 2에서 더 자세히 확인할 수 있습니다.
- Cast 탭에는 해당 영화에 출연하는 배우를 최대 3명까지 화면 너비에 맞게 보여줍니다(스크롤 불필요).
- Cast 탭에 표시된 배우 카드를 누르면 Artist Detail 페이지로 이동합니다.
- 상단의 플레이 아이콘과 더 보기 아이콘은 아무 작동도 하지 않아도 됩니다.
- 하단의 Reviews, More 탭은 아무 작동도 하지 않아도 됩니다.

### Artist Detail

- 배우의 상세 페이지를 목업에 맞게 구현합니다.
- 배우에 대한 상세 정보와 사진 정보는 아래 API에서 얻을 수 있습니다.
  - [person](https://developers.themoviedb.org/3/people/get-person-details)
  - [person - images](https://developers.themoviedb.org/3/people/get-person-images)
- 배우 상세 페이지에서 더 이상의 이동은 하지 않아도 됩니다.
- 각 이미지나 탭 버튼을 눌렀을 때에 대한 구현은 하지 않아도 됩니다.

## 기타 주의사항

- 모든 기능이 완벽하게 구현되지 않아도 좋습니다만 너무 적은 양이 구현되었을 경우 코드에 대한 판단을
  내리기 어려울 수도 있습니다.

## 보너스 기능

- 애니메이션을 통한 적절한 마이크로 인터렉션 구현
- unit, functional, e2e 테스트 작성
- typescript 사용
- styled-components 사용
- mobx 혹은 mobx-state-tree 사용
- data loading 중 상태에 대한 처리
- API 호출 실패시에 대한 적절한 처리
- lint, prettier 등 코드 정리 도구 사용

## 주요 평가 영역

- 요구사항과 유저스토리에 맞게 구현되었는가?
- 함수/컴포넌트/파일 등이 역할에 따라 적절히 분할되어 있는가?
- 적절한 단위로 커밋을 나누고 의미 있는 메세지를 사용했는가?
- 필요한 곳에 constant를 적절히 사용했는가?
- 개발환경에서 불필요한 에러/경고 메세지가 발생하지 않도록 했는가?

## Resources

### Mockup

- [Movies & Series mock up](https://www.figma.com/file/7Tr5BCjrIvIsBxxCFJjdDj/movies-app-davor-naumoski?node-id=0%3A583)

### API

- [MovieDB Api](https://developers.themoviedb.org/3)
  - apiKey : 844dba0bfd8f3a4f3799f6130ef9e335
    - ex) https://api.themoviedb.org/3/movie/popular?api_key=844dba0bfd8f3a4f3799f6130ef9e335&language=en-US&page=1

## 제출 방법

- Github 나 Gitlab 에 private repository 를 만들어주세요.
- 모든 코드의 변경 과정을 잘 정리해서 commit 해주세요.
  - commit message 도 잘 적어주세요.
- 실행 방법 및 프로젝트 소개를 README.md 파일에 정리해 주세요.
- 제한 시간 안에 마무리하신 후 해당 repository 에 recruit@cosmochain.io 계정을 collaborator(github), members(gitlab, reporter 이상의 권한 필요)로 추가해주신 후, Contact 중인 담당자 이메일로 repository 의 https 주소를 공유해주세요.
