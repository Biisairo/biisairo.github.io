# ft_transcendence

# 목표

- 퐁 게임 만들기
- 채팅
- 실시간 멀티 게임

일반 - 백앤드는 NestJS - 프론트는 TS 를 사용하는 아무 프레임워크 - 원하는 라이브러리를 사용할 수 있음 - 무조건 최신 안정버전을 사용할 것 - DB 는 postgresSQL - Single-page application 일것 - 브라우저의 앞으로 가기, 뒤로가기를 사용할 수 있을 것 - chrome 의 최신 안정버전과 추가로 하나의 브라우저를 사용해 확인 - 사용자가 웹 서비스를 이용할 때 처리되지 않은 오류나 경고가 있으면 안됨 - 모든것은 `docker-compose up --build` 로 실행이 되어야함

보안 - 모든 비밀번호는 hashed 되어야 한다 - SQL 인젝션으로 부터 안전해야 한다 - 모든 form 및 유저 입력에 대해 서버측의 유효성 검사가 있어야 한다 PS. 보안상의 이유로 모든 인증서, API key, 환경변수들은 .env 파일에 로컬로 저장하고 git 에서 무시되어야 한다

유저 계정 - 42 OAuth 를 이용해 로그인한다 - 사용자는 unique 한 이름으로 표시된다 - 유저는 아바타(프사?)를 업로드 할 수 있어야 하며, 업로드 하지 않은 경우 기본 이미지가 세팅되어야 한다 - 유저는 2단계 인증을 하여야 한다 - 구글 인증기(google authenticator) 이나 핸드폰 메세지를 사용 - 다른 유저를 친구로 등록할 수 있어야 하며 친구의 현재 상태(online, offline, 게임중 등)를 알 수 있어야 한다 - 스텟(승,패, 래더레벨, 도전과제 등)이 유저 프로필에 표시 되어야 한다 - 각각의 사용자는 1 대 1 경기, 래더경기, 이외의 모든 경기 기록을 가지고 있어야 하며 로그인한 사용자라면 누구나 확인할 수 있어야 한다

채팅 - 사용자가 방을 공개, 비공개, 혹은 비밀번호를 설정할 수 있는 방을 만들 수 있어야 한다 - 다른 사용자에게 DM 을 보낼 수 있어야 한다 - 다른 사용자를 차단할 수 있으며 차단한 계정의 메세지는 볼 수 없어야 한다 - 새 채널을 만든 사용자는 채널을 떠날때 까지 채널의 소유주가 된다 - 채널 소유자는 채널에 들어오는데 필요한 비밀번호를 생성, 변경, 삭제 할 수 있어야 한다 - 채널 소유자는 채널 관리자이다. 관리자는 다른 유저를 관리자로 만들 수 있다. - 채널 관리자는 (제한된 시간동안) 다른 유저를 kick, ban, mute 할 수 있으며 채널 소유자는 그렇지 못하다 - 사용자는 채팅 인터페이스를 통해 다른 사용자를 PONG 게임에 초대할 수 있어야 한다 - 사용자는 채팅 인터페이스를 통해 다른 사용자의 프로필을 확인할 수 있어야 한다

게임 - 사용자는 웹사이트에서 실시간으로 다른 사용자와 퐁 게임을 할 수 있어야 한다 - 메치메이킹 시스템이 있어야한다 - 사용자는 자동적으로 다른 사용자와 메치될 때 까지 대기열에 들어가게 된다 - 게임 그래픽이 어떻든 일단 1972년에 나온 퐁 게임에 충실해야 한다 - 게임에 사용자 추가 옵션을 설정할 수 있어야 하며 원하지 않을 경우 기본 게임을 할 수 있도록 해야 한다 - 게임은 반응성이 좋아야 한다 - 사용자가 다른 사용자들의 경기를 실시간 플레이를 방해하지 않고 관람할 수 있어야 한다