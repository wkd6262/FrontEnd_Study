# FrontEnd_Study

## 230821 ##

### git이란? ###

- 컴퓨터 파일의 변경사항을 추적하고 여러명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 스냅샷 스트림 기반의 분산 버전 관리 시스템.
또는 이러한 명령어들을 가리킨다.
- 매우 빠른속도,분산형 저장소 지원이 특징이다.
- 오프라인 작업도 가능하다.
- 로컬저장소를 이용하면 되기 때문에 서버장애가 있어도 개발이 가능하다.
- 나무 같은 프로그램 branch 가지치기 등등..

* 코딩특화 폰트 - D2coding 폰트를 사용하면 숫자 "1"과 소문자 "1" 을 구분할 수 있게 되고 이하 헷갈리는 기호들의 구분도 가능하다.
- 글꼴 및 크기 설정은 git 실행-마우스 우클릭-text클릭-변경

## git 기본명령어 ##
- cd 디렉토리변경
- repository 기록공간
- working    작업공간
- stage       임시공간
- branch     기준작업라인
- main(master)  기본,main branch
- commit      타임캡슐에다 넣고 커밋을 넣으면 소스코드가 쌓임, 언제든 과거로 돌아갈 수 있음
- git config --list명령어에서 오류가 뜨면 Q를 누르면 해결
- 방향키 위 - 직전에 썼던 명령어
- git add ""   파일추가
- git status   깃 상태
 git log 현재까지 진행 상태 확인
- git commit -am "" (add와 커밋메시지를 함께설정할 수 있음)*한번이라도 커밋이 되어야함


## git 명령어(Bash) 모음 ##
- Bash란? 깃에서 사용할 수 있는 리눅스 쉘shell / 명령어
* Home Directory 홈디렉토리 : 컴퓨터 로그인 한 후 사용자 디렉토리 
- 윈도우 C:\User\사용자이름
- MAC  /User/사용자이름

- cat "파일명.형식" (파일명 형식의 내용)
- pwd                (현재 디렉토리 위치)
- Is                    (현재 디렉토리 내에 존재하는 파일 보여줌)
- Is -all               (존재하는 파일을 다 보이고, 그 권한들까지 다 보여줌)
- Is -a                (숨김 파일 리스트 형태로 보임)
- clear                (현재 콘솔창 모든 내용 지움)
- Is -IR               (하위 폴더의 상세내용)
- cd 폴더명         (그 폴더로 들어감)
- cd /e              ("e"드라이브로 이동)
- cd ..               (현재 디렉토리에서 상위 디렉토리로 이동)
- cd -               (바로 이전 디렉토리 이동)
- touch 파일명    (파일생성)
- mkdir 폴더명    (폴더명으로 새로운 디렉토리를 만듦)
- shutdown        (시스템종료)
- reboot            (재부팅)
- mv 폴더명.형식 디렉토리명  ("폴더명.형식")을 "디렉토리 명"으로 옮김
- date               (현재시각)
- rm 파일          ("파일"을 삭제)
- rmdir 폴더명    (폴더명을 가진 디렉토리를 삭제.)
- file 파일명       ("폴더명"의 파일의 형식을 보여줌)
- kill                (현재 작동중인 어플리케이션 중지)
- vim 컴파일된 파일명.확장자 (확장자로 된 "컴파일 된 파일"을 엶)
- q                  (다양한 옵션이 존재하며 입력하게 되면 파일 밖으로 나감)
- e                   (편집모드)
- i                   (insert 모드로 들어가 글자를 삽입)
- ~                   (현재 폴더 위치 홈으로 *홈디렉토리)



## 2023-08-22 ##
- git branch "" 나무가지 추가.
- git branch --list 브랜치 리스트확인
-git switch "" ""의 브랜치로 바로 이동
- git log --oneline    log 간단하게보기
- git switch -c ""         ""의 브랜치를 생성후 바로 이동함.
- git branch -d ""       ""의 브랜치를 원격에 푸쉬되어 있고 병합되어있을때만 삭제
- git branch -D ""         ""의 브랜치를 강제삭제

## GIT과 GIT허브 연결 ##
- git에서 이름과 이메일 동일하게설정 *어떤파일이든 한 번은 커밋되어야함.
- github의 repositories 탭으로 넘어가 new -public-create

## 업로드 방법 ##
- git remote ad origin "나의주소"
- gir branch -M main (이름이 main이 아닐시)
- git push -u origin main    (푸시 - 업로드 오리진메인) 내용이 변경될 때 마다 입력

## 다운로드 방법 ##
- main브런치 : git pull (origin main)
- 다른 브런치 : git pull origin 브런치이름
- 로컬 파일에 덮어 씌움.

## 에러 ##
- error: remote origin already exists 에러가 뜰 경우

- git remote rm origin (연결된 온라인 저장소 정보 삭제) 입력
*작업을 갈아엎을 경우도 가능

- 마크다운 이미지 넣기
마크다운 파일에 이미지 issue 탭에 삽입 후 주소 복사.

- cd= 체인지 디렉토리

## 230823 ##

### 일반 ###
1.로컬 저장소 생성 후 만들고 싶은 곳에 git을 실행 후 아래의 명령어를 입력한다.

`git init`<br>

2.README.md 파일생성

`touch README.md`<br>
`git status를 입력해 변동사항을 확인한다.`<br>
`git add . 추가된 모든 파일을 등록한다`<br>
`git commit -m ""  ""메시지와 함께 커밋을 한다.`<br>

3.온라인 저장소 생성

`git remote add origin https://github.com/"아이디"/로컬저장소.git`<br>

4.README.md파일 온라인 저장소에 업로드

`git push -u origin main`<br>

### github에서 내려 받기 ###
`git pull origin main`

### clone과 pull 차이 ###
-clone : 로컬에 저장소가 없는 경우. 저장소 자체를 복사
-pull : 로컬에 연결된 저장소 있는 경우. 저장소 안에 있는 파일 내려받기

### 충돌(rejacted,conflict)시 해결 방법 ###
__충돌 이유__<br>
하나의 문서가 온라인과 로컬에 각 각 수정이 일어났기 때문

__해결__<br>
1.에러 메시지 확인 후 git pull을 이용해 전 버전으로 복구한다.<br>
2.복구 후 직접 내용을 추가한 후 commit을 한다<br>
3.git push -u origin main 을 입력해 오류가 안뜨면 성공.

## clone 과 pull ##
- clone : 로컬에 저장소가 없는 경우. 저장소 자체를 복사
- pull : 로컬에 연결된 저장소 있는 경우. 저장소 안에 있는 파일 내려받기

* rejected 오류 발생시 일단 git pull로 전 버전을 다운받고 해결한다.

## pull request
- 포크로 가져온 repository를 수정 및 원작자에게 수정 반영하는 과정
- 로컬에서 커밋 후 push
- 포크한 github repository의 pull requests 탭으로 이동
- new pull request 버튼 클릭
- 수정된 내용 확인 후 create pull request 버튼 클릭
- 커밋 메시지 작성 혹은 확인 후 create pull request클릭
- 전송이 되면 원작자의 repository pull requests 탭에서 확인 가능

## 230824 ##
## HTML 이란? ##
- 콘텐츠의 구조를 정의하는 마크업 언어이다.

## HTML요소의 구조 ##

![grumpy-cat-small](https://github.com/wkd6262/home/assets/142865132/332e8fd4-3f4b-4f89-aed9-7b41f24afa34)


- 여는 태그 <p> (Opening tag): 이것은 요소의 이름으로 구성되고 (여기에서는 p), 여닫는 꺾쇠괄호로 감싸집니다. 이것은 요소가 시작되는 곳, 또는 효과를 시작하는 곳

- 닫는 태그 </p> (Closing tag): 이것은 여는 태그와 같지만, 요소의 이름 앞에 전방향 슬래시가 포함된다는 점이 다릅니다.

- 내용(Content): 요소의 내용이며, 이 경우 단순한 텍스트이다.

- 요소(Element): 여는 태그, 닫는 태그, 내용을 통틀어 요소(element)라고한다.
## HTML 주석 처리 방법 및 HTML 구조 ##
![1](https://github.com/wkd6262/home/assets/142865132/d5c2d7e5-135d-4c71-a2af-0a2f8018bc7e)
## pull request Check
- pull request 버튼클릭
- 내용 검토
- 수정된 내용을 나의 github repository 반영하려면 Merge pull request 클릭

## 230901 ##
### 테이블 연습 ###
[listEx1]<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
  <h1>테이블 연습 1</h1>
  <table border="1">
    <caption>2023년 식비</caption>
    <tr>
      <th>월</th>
      <th>일</th>
      <th>금액</th>
    </tr>
    <tr>
      <th rowspan="2">3월</th>
      <td>1일</td>
      <td>1,000</td>
    </tr>
    <tr>
      <td>2일</td>
      <td>2,000</td>
    </tr>
    <tr>
      <th colspan="2">합계</th>
      <td>3,000</td>
    </tr>
  </table>
</body>
</html>
<hr>
[listEx2]<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
  <table border="1">
    <h1>여름이 온다 그림책 안내</h1>
    <tr>
      <th colspan="3">그림책 소개</th>
    </tr>
    <tr>
      <th colspan="3">여름이 온다</th>
    </tr>
    <tr>
      <td rowspan="3"><a href="https://www.yes24.com/Product/Goods/102965090" target="_blank"><img src="https://raw.githubusercontent.com/wkd6262/tableEx/03f1b94034e2ce87a0f0473c2ba956225abcd7e1/img.jpg" alt=""></a></td>
      <th>글</th>
      <td>이수지</td>
    </tr>
    <tr>
      <th>그림</th>
      <td>이수지</td>
    </tr>
    <tr>
      <th>가격</th>
      <td>27,000원</td>
    </tr>
  </table>
</body>
</html>
<hr>
[listEx3]
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
  <table border="1">
    <caption><h1>백종원의 '불고기 샌드위치' 레시피</h1></caption>
    <tr>
      <th colspan="2">레시피</th>
    </tr>
    <tr>
      <th rowspan="2"><img src="https://github.com/wkd6262/tableEx/blob/main/images/img02.jpg?raw=true" alt=""></th>
      <th>조리방법 1</th>
    </tr>
    <tr>
      <td>식빵에 상추를 원하는 만큼 푸짐하게 덮어주세유</td>
    </tr>
    <tr>
      <th rowspan="2"><img src="https://github.com/wkd6262/tableEx/blob/main/images/img03.jpg?raw=true" alt=""></th>
      <th>조리방법 2</th>
    </tr>
    <tr>
      <td>마요네즈를 듬뿍 올려유</td>
    </tr> 
    <tr>
      <th rowspan="2"><img src="https://github.com/wkd6262/tableEx/blob/main/images/img04.jpg?raw=true" alt=""></th>
      <th>조리방법 3</th>
    </tr>
    <tr>
      <td>그 위로 불고기를 싸악 올리구</td>
    </tr> 
    <tr>
      <th rowspan="2"><img src="https://github.com/wkd6262/tableEx/blob/main/images/img05.jpg?raw=true" alt=""></th>
      <th>조리방법 4</th>
    </tr>
    <tr>
      <td>다시 식빵으로 덮으면 끝!</td>
    </tr>
  </table>
</body>
</html>

## 230920 web Ex ##
💻https://wkd6262.github.io/kims/
- 프론트엔드 학원 과정으로 테이블을 이용한 웹 사이트 구조를 만들었습니다.

