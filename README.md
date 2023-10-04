# 멀티미디어 실습

2023년 가을학기에 진행한 Git 수업 정리

## 2023-10-04
### 스테이지 영역
- IT프로젝트는 여러 파일을 동시에 다루게 된다.
- 일반 문서 수정과 같이 '저장' 버튼 클릭만으로 한번에 수정한 파일들을 저장하게 하면, 불필요한 파일들이 커밋에 포함되는 일들이 발생한다.
  - ex: 
    - '.vs': visual studio로 프로젝트 열었을 때 자동 생성되는 폴더

- 그래서 staging area라는 영역을 따로 두고, commit에 포함시킬 코드(파일)만 staging 영역에 추가하게 한 다음, commit을 만든다.
  - staging 영역에 파일을 추가할 때 쓰는 명령어: `git add 파일명`

### gitignore파일
- 루트 경로에 있는 `-gitignore` 파일은 버전관리 하지 않을 파일의 목록을 관리하는 용도로 쓰인다.
- 사용하는 운영체제, 에디터, 프로그래밍 언어, SDK, 라이브러리 등의 종류에 따라 사람이 의도하지 않은 파일이 생성되는데, 이런 파일들은 버전관리 대상이 아니므로 `-gitignore` 파일에서 관리한다.
  - ex: https://github.com/setchi/FancyScrollView/blob/master/.gitignore
- 처음 프로젝트 세팅하는 사람은 여러 틀을 사용해 자동으로 `-gitignore` 파일에 들어갈 내용을 생성한다.
  - 웹사이트:
    - 구글에서 "gitignore genertor"로 검색
      - https://www.toptal.com/developers/gitignore
    - VSCode 익스텐션:
      - gitignore by CodeZombie



## 2023-09-27
- commit이란?
  - git의 기본 단위로 논리적 변경이 있을 때 만든다. (사진찍기와 유사)
- commit 메시지
  - 코드 변경분을 한 마디로 설명함
- 명령어
  - git commit -m "커밋 메시지를 이곳에 입력"
  - git commit -message "커밋 메시지를 이곳에 입력"
- 얼마나 자주 commit을 만들어야 하나?
  - 너무 작지도, 크지도 않게 한다. (조직에 따라, 프로젝트 성격에 따라 다름)
  - 커밋 단위가 너무 작을경우 불필요한 commit들이 생성됨
  - 커밋 단위가 너무 클 경우 장애가 났을 때 빠른 대응이 힘듬
  - ex: 30분 안에 리뷰 가능하도록 commit 크기 조절