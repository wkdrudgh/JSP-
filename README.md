JSP를 이용한 게시판 만들기
=======
목차
- [프로젝트 소개](#프로젝트-소개)
- [프로젝트 설계 및 계획](#프로젝트-설계-및-계획)
- [주요 기능 및 설명](#주요-기능-및-설명)
- [외부 라이브러리](#외부-라이브러리)
- [마치며](#마치며)
- [추가](#추가)

프로젝트 소개
----
CRUD에 대한 기본개념과 JSP사용방법을 익히기 위해 만든 프로젝트입니다.


프로젝트 설계 및 계획
--------
이 프로젝트는 Jsp를 기반으로 만들어진 게시판 사이트입니다.<br>
부트스트랩3를 이용해 전체적인 디자인을 구현했고 톰켓을 사용해 서버를 구축했습니다.<br>
데이터베이스는 MySql를 사용했습니다.

메인페이지
-----
![스크린샷(41)](https://user-images.githubusercontent.com/67408846/103606618-3af94e00-4f5a-11eb-89af-c7e154306a52.png)&nbsp;
<br/>
<br/>
<br/>
주요 기능 및 설명
-----
![스크린샷(42)](https://user-images.githubusercontent.com/67408846/103607361-0dad9f80-4f5c-11eb-9767-0cf6a8a4d098.png)&nbsp;
-----
- 로그인
 1. 사용자 아이디와 비밀번호를 이용해 로그인이 가능합니다.
 - 경고 alert창 뜨는 조건
 1. 아이디가 DB에 없을 경우
 2. 아이디를 입력안했을 때
 3. 비밀번호를 입력안했을 때
 4. 로그인을 이미 했을 때(강제로 주소를 login폼으로 가서 로그인시 나옴.)

-----
![스크린샷(43)](https://user-images.githubusercontent.com/67408846/103614599-4bb2bf80-4f6c-11eb-8ad1-c6ed85140442.png)
-----
- 게시판 목록페이지
 1. 한 페이지당 8개에 게시글만 보여집니다.
 2. 처음페이지는 다음 버튼만 있고 마지막 페이지는 이전 버튼만 있습니다.
 3. 중간에 있는 페이지는 이전 다음 버튼이 존재합니다.

-----
![스크린샷(44)](https://user-images.githubusercontent.com/67408846/103614331-b0214f00-4f6b-11eb-82a8-273514619cab.png)
-----
- 게시판 글등록
 1. 게시글 제목과 내용을 등록 할 수 있습니다.
 2. 로그인이 되어있지 않으면 게시글을 등록할 수 없고 자동으로 로그인페이지로 이동합니다.

-----
![스크린샷(45)](https://user-images.githubusercontent.com/67408846/103615017-2c686200-4f6d-11eb-98d2-f0863c728b05.png)
-----
- 게시판 상세페이지
 1. 게시글에 내용을 볼 수 있습니다.
 2. 목록가기, 수정하기, 삭제하기, 글쓰기 버튼이 있습니다.

-----
![스크린샷(46)](https://user-images.githubusercontent.com/67408846/103615640-422a5700-4f6e-11eb-8039-3ceea2a5190d.png)
-----
- 게시판 글수정
 1. 게시글 제목과 내용을 수정할 수 있습니다.
 2. 본인이 작성하지 않은 글을 수정이 불가능 합니다.

-----
![스크린샷(46)](https://user-images.githubusercontent.com/67408846/103615640-422a5700-4f6e-11eb-8039-3ceea2a5190d.png)
-----
- 게시판 글삭제
 1. 게시글을 지울 수 있습니다.
 2. 본인이 작성하지 않은 글은 삭제가 불가능 합니다.

외부 라이브러리
-----
1. mysql-connector-java-8.0.21.jar
> jdbc드라이버, 데이터베이스 접속을 위해 사용

마치며
-----
JSP를 이용해서 많은 기능을 넣고 싶었지만 거의 기본적이고 CRUD를 익히기 위해 해본 프로젝트여서 많은 아쉬움이 남았습니다.<br/>
다음에 추가, 수정해보고 싶은 것들
1. 다양한 외부라이브러리를 사용하는 것<br/>
2. 검색기능 구현하기 <br/>
3. 다양한 부트스트랩 디자인 구현<br/>
4. 게시글 삭제시 고유번호가 사라져서 그 번호를 사용못하는 점<br/> 
-----
