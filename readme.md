# 커넥션 풀(DBCP)
<Resource name="jdbc/myoracle" auth="Container"
  type="javax.sql.DataSource" driverClassName="oracle.jdbc.OracleDriver"
  url="jdbc:oracle:thin:@127.0.0.1:1521:xe"
  username="ezen" password="1234" maxTotal="20" maxIdle="10"
  maxWaitMillis="-1"/>
  
  
  #DB
DROP TABLE movie;
DROP SEQUENCE movie_seq;

CREATE SEQUENCE movie_seq INCREMENT BY 1 START WITH 1;

CREATE TABLE movie(
code number(4) PRIMARY KEY,
title VARCHAR2(50),
price NUMBER(10),
director VARCHAR2(20),
actor VARCHAR2(20),
poster VARCHAR2(100),
synopsis VARCHAR2(1000));

insert into movie values(movie_seq.nextval,
'베를린',  10000, '류승완', '하정우', 'movie1.jpg',
'거대한 국제적 음모가 숨겨진 운명의 도시 베를린.
 그 곳에 상주하는 국정원 요원 정진수는 불법무기거래장소를 감찰하던 중 국적불명, 지문마저 감지되지 않는 일명 ‘고스트’ 비밀요원 표종성의 존재를 알게 된다. 그의 정체를 밝혀내기 위해 뒤를 쫓던 정진수는 그 배후에 숨겨진 엄청난 국제적 음모를 알게 되면서 걷잡을 수 없는 위기에 빠진다.
 한편 표종성을 제거하고 베를린을 장악하기 위해 파견된 동명수는 그의 아내 연정희를 반역자로 몰아가며 이를 빌미로 숨통을 조이고, 표종성의 모든 것에 위협을 가한다. 표종성은 동명수의 협박 속에서 연정희의 무죄를 증명하기 위해서 그녀를 미행하게 되지만, 예상치 못한 아내의 비밀을 알게 되면서 혼란에 휩싸이게 되는데...');
insert into movie values(movie_seq.nextval,
'박수건달',  10000, '조진규', '박신양, 엄지원', 'movie2.jpg',
'건달로 사느냐, 무당으로 사느냐 그것이 문제로다!
보스에게 신임 받고, 동생들에게 사랑 받는 엘리트 건달 광호(박신양). 
남 부러울 것 없이 승승장구 하던 그의 건달 인생에 ‘그 분’이 태클을 걸었다?! 
호시탐탐 광호를 밟을 기회만 노리던 태주(김정태)의 칼에 맞고 순식간에 바뀐 운명선 때문에 
 낮에는 박수무당, 밤에는 건달의 투잡족이 되어버린 광호! ');
insert into movie values(movie_seq.nextval,
'레미제라블',  10000, '톰 후퍼', '휴 잭맨', 'movie3.jpg',
'빵 한 조각을 훔친 죄로 19년의 감옥살이를 한 장발장(휴 잭맨). 우연히 만난 신부의 손길 아래 구원을 받고 새로운 삶을 결심한다. 정체를 숨기고 마들렌이라는 새 이름으로 가난한 이들을 도우던 장발장은 운명의 여인, 판틴(앤 해서웨이)과 마주치고, 죽음을 눈앞에 둔 판틴은 자신의 유일한 희망인 딸 코제트(아만다 사이프리드)를 장발장에게 부탁한다. 그러나 코제트를 만나기도 전에 경감 자베르(러셀 크로우)는 장발장의 진짜 정체를 알아차리고, 오래된 누명으로 다시 체포된 장발장은 코제트를 찾아 탈옥을 감행하는데… ');
insert into movie values(movie_seq.nextval,
'7번방의 선물',  9000, '이환경', '류승룡, 갈소원', 'movie4.jpg',
'최악의 흉악범들이 모인 교도소 7번방에 이상한 놈이 들어왔다!
 그는 바로 6살 지능의 딸바보 용구! 
 평생 죄만 짓고 살아온 7번방 패밀리들에게 떨어진 미션은 바로 용구 딸 예승이를 외부인 절대 출입금지인 교도소에 반.입.하.는.것!
 2013년 새해, 웃음과 감동 가득한 사상초유의 합동작전이 시작된다!');

COMMIT;

select * from MOVIE;