인트라넷 SNS
=======
목차
- [프로젝트 소개](#프로젝트-소개)
- [프로젝트 설계 및 계획](#프로젝트-설계-및-계획)
- [주요 기능 설명](#주요-기능-설명)
- [외부 라이브러리](#외부-라이브러리)
- [버전 변경 사항](#버전-변경-사항)
- [마치며](#마치며)
- [추가](#추가)


프로젝트 소개
--------
조직 또는 단체 내에서만 우리끼리만의 SNS가 있다면???? 이라는 아이디어로 시작한 프로젝트입니다.
우리 프로젝트는 이런 요구사항을 만족시킬 수 있는 좋은 프로젝트라고 생각합니다.
회사 안에서 단순히 정보 전달과 정보 공유만 하는 것이 아니라
그룹 채팅으로 부서 내 회의도, 오픈 채팅으로 다른 부서의 사람들과도 소통할 수 있습니다.
거기다 게시판 기능으로 커뮤니티 활동도 가능합니다.

프로젝트 설계 및 계획
--------
우리 프로젝트는 Java를 기반으로 만들어진 윈도우 응용 프로그램입니다.
JavaFX를 이용해 UI를 구현했고 라즈베리파이를 사용해 서버를 구축했습니다.
데이터베이스는 mariaDB를 사용했습니다.

팀장 최문석을 필두로 김도엽, 심대훈 3명으로 프로젝트를 진행했습니다.
- 책임 : 최문석
- UI구성 및 디자이너 : 심대훈
- 서버 구축 및 데이터베이스 구축 : 최문석
- 기능 구현 및 코더 : 최문석, 심대훈

주요 기능 설명
------
<img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/login.PNG" width="200px">&nbsp;
<img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/signUp.PNG" width="200px">&nbsp;
<img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/findAccount.PNG" width="200px"><br>
- Login
> 로그인 모듈에서는 로그인 관리, 사용자 등록, 계정 찾기를 실행할 수 있습니다.<br>
> 사용자 번호와 비밀번호를 이용해 로그인이 가능합니다.<br>
> 계정이 없다면 사용자 등록을 통해 계정 등록이 가능하고 계정을 분실했을 경우<br>
> 계정 찾기를 통해 이메일로 사용자 번호와 비밀번호를 전송받을 수 있습니다.<br>

<br><img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/main.PNG" width="250px">&nbsp;
- Notice
> 알림 탭에서는 가장 최근 내용을 리스트로 출력합니다.<br>
> 가장 최신 공지사항을 최상단에 보여줍니다. 접거나 펼쳐서 내용을 확인할 수도 있습니다.<br>
> 리스트에는 공지사항과 해당 사용자의 소속의 게시판 및 전체 게시판의 가장 최신글,<br>
> 해당 날짜의 개인이 등록한 일정 및 단체 일정을 출력해 가장 최신의 내용을 확인할 수 있습니다.<br>

<br><img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/userInfo.PNG" width="250px">&nbsp;
<img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/myProfile.PNG" width="250px"><br>
- User Info
> 사용자의 상세 정보를 확인할 수 있습니다.<br>
> 화면 상단에는 자신의 프로필을 출력하고 여기에서는 자신의 상태 메시지를 변경할 수 있습니다.<br>
> 리스트에는 사용자들이 탭 형식으로 소속별로 구분되어 있습니다.<br>
> 리스트에서 사용자를 선택하면 해당 사용자의 자세한 정보를 확인할 수 있습니다.<br>
> 사용자의 이름과 소속을 이용해 검색이 가능합니다.<br>

<br><img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/chat.PNG" width="250px">&nbsp;
<img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/chatroom.PNG" width="300px">&nbsp;
- Chatting
> 사용자는 2개의 채팅방을 선택해 입장할 수 있습니다.<br>
> 모든 구성원들이 소속에 구분없이 접속이 가능한 전체 채팅방과 각 소속별로 구분되어 있는 그룹 채팅방입니다.<br>

<br><img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/boardRead.PNG" width="250px"><br>
- Board
> 게시판은 모든 소속을 포함하는 '전체'리스트와 각 소속별로 구분된 리스트를 제공합니다.<br>
> 사용자는 해당 게시판을 선택해 글을 작성할 수 있으며 파일 첨부도 가능합니다.<br>
> 게시물 수정이나 삭제는 작성한 사용자가 아니라면 불가능합니다.<br>

<br><img src="https://github.com/ColossusCMS/IntranetSNS/blob/master/Screenshot/scheduleEntry.PNG" width="400px">
- Schedule
> 일정관리는 달력 형태로 새로운 창이 생성됩니다.<br>
> 일정을 등록하려면 해당 날짜를 선택하고 개인 일정을 등록하면 됩니다.<br>
> 해당 날짜에 개인 일정이 등록되어 있다면 빨간색으로, 단체 일정이 등록되어 있다면 파란색으로,<br>
> 개인 일정과 단체 일정이 모두 등록되어 있다면 녹색으로 표시됩니다.<br>
> 상단의 라디오 버튼으로 원하는 일정만 표시할 수도 있습니다.

외부 라이브러리
------
1. mysql-connector-java-5.1.47.jar
> jdbc드라이버, 데이터베이스 접속을 위해 사용

2. javax.mail-1.4.7.jar
> smtp 서버에 접속해 메일을 송신하기 위해 사용

3. jsch-0.1.55.jar
> SFTP 서버에 접속해 업로드와 다운로드를 하기 위해 사용

4. commons-io-2.6.jar
> 파일명에서 확장자만 추출하기 위해 사용
> String exp = FilenameUtils.getExtension(file)을 이용하면 파일명에서 확장자만 저장이 가능

버전 변경 사항
-------
`1.0.0`
> 프로그램이 완성되었습니다.


마치며
-------
Java라는 프로그래밍 언어를 배우면서 습득했던 지식들을 최대한 많이 사용하기 위해서 이 프로젝트를 진행했습니다.<br>
부족한 부분도 많이 있고 계획대로 구현하지 못한 부분도 많이 있습니다.<br>
댓글 기능의 부재, 개인 간의 채팅기능 등 어쩌면 기본이라고 할 수도 있는 부분들이 없는 것이 굉장히 아쉬웠습니다.<br>
JSP, Javascript 등의 웹 개발 언어를 사용하지 않고 JavaFX로 만든 응용 프로그램이기 때문에<br>
좀 더 다양한 플랫폼으로 개발하지 못한 것 또한 아쉬운 부분입니다.<br>
분명 아쉬운 부분들이 많이 존재하지만 가지고 있는 지식을 최대한 담아내기 위해서 팀원들과 많이 노력했습니다.<br>
프로젝트 일정은 종료되었지만 좀 더 좋은 프로그램이 될 수 있도록 업데이트할 수 있도록 노력하겠습니다.<br>

추가
-------
해당 소스에는  데이터 베이스와 서버에 접속하기 위한 계정을 담고 있는 클래스가 없는 관계로<br>
해당 소스만으로는 프로그램 실행이 불가능합니다.<br>
Java 응용 프로그램이기 때문에 JDK와 JRE가 설치되어 있어야 합니다.<br>
