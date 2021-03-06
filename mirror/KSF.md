## Contents

    

1. [Kick it up](Kick%20it%20up.md) Step File 
    

1.1. 문법

    

1.1.1. 구 문법

1.1.2. 신 문법

1.2. KSF 커뮤니티의 역사

1.3. 관련 사이트

    

1.3.1. 운영중인 사이트

    

1.3.1.1. DropNote

    

1.3.1.1.1. 5kNote

1.3.1.2. Creative Rhythm World

1.3.2. 운영중단된 사이트

    

1.3.2.1. Forhythm

1.3.2.2. KSF.net

1.3.2.3. The Rhythm

2. 그 외 
3. 각종 협회및 연맹의 약자 
4. 코리아 스피드 페스티벌(Korea Speed Festival) 

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=1)]

# 1. [Kick it up](Kick%20it%20up.md) Step File ¶

[킥잇업](%ED%82%A5%EC%9E%87%EC%97%85.md), [Direct Move](Direct%20Move.md),
[Stepmania](Stepmania.md)에서 구동되는 파일이다.

  

1999년에 'mahalo'라는 필명을 쓰던 개발자 노기태가 만든 구동기`[1]`인
[킥잇업](%ED%82%A5%EC%9E%87%EC%97%85.md)에서 처음으로 사용된 파일 형식이다.

  

이 파일의 문법은 [안다미로](%EC%95%88%EB%8B%A4%EB%AF%B8%EB%A1%9C.md)의 [펌프 잇업](%ED%8E%8C%ED%94%84%20%EC%9E%87%20%EC%97%85.md)의 초기버전에서 유래한 문법이며`[2]` 킥잇업
초기에는 그와 유사한 문법으로 나갔으나 현재는 그 문법에 살이 더해졌다.

  

현재 사용되는 KSF 포맷은 구 문법에 'Kiho'라는 필명을 쓰는 김기호가 개발한 [DirectMove](Direct%20Move.md)에 기반한 새로운 문법을 같이 사용한다.

  

[Stepmania](Stepmania.md)에서는 5.0 이전까지 [Direct Move](Direct%20Move.md)에
기반한 문법을 읽지 못하였는데, 5.0 이후로는 읽을 수 있다.

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=2)]

## 1.1. 문법 ¶

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=3)]

### 1.1.1. 구 문법 ¶

구 문법을 근간으로 한 KSF파일의 기초형식은 다음과 같다.  
{{|  
#TITLE: title;  
#BPM: 128;  
#STARTTIME: 100;  
#PLAYER: SINGLE;  
#TICKCOUNT: 4;  
#STEP:  
1000000000000  
0100400000000  
0010400000000  
0000400000000  
0000000000000  
2222222222222  
|}}

  

구 문법에 대한 옵션에 대한 설명은 다음과 같다.

  

#TITLE : KSF파일의 이름을 지정해준다. 프로그램이 이 항을 읽어 이 파일의 제목을 띄어주는데 없으시 아무것도 없는 공백상태로 나오게
된다.  
#BPM : KSF파일의 [BPM](BPM.md)을 지정해준다. 수의 범위는 1이상의 실수범위.  
#STARTTIME : KSF파일이 몇초부터 시작되는지 지정해준다. 수치 100는 1초와 같다. 예로들면 이 수치가 25이면 이면
0.25초를 뜻한다. 수치의 범위는 0부터 소수점 2자리까지이다.  
#PLAYER : 싱글모드, 더블모드를 설정해준다. 만약 스텝파일을 다 작성해놓고도 Single로 작성시 1p쪽의 스텝파일만 나오게 된다.
옵션은 Single과 Double.  
#TICKCOUNT : 스텝파일의 박자를 나타낸다. 4라는 수치는 1/4박이며 이렇게 될 시 스텝파일의 4줄씩 1박자로 계산하게 되어 나오게
된다. 수치의 범위는 1 이상의 정수이다.`[3]`

  

이 양식은 Kickiup 등에서 읽을 수 있게 기본적으로 작성해야 하는 옵션이고 추가로 다른 옵션을 추가 할 수 있다.

  

#INTROFILE: 인트로 파일의 위치를 지정한다. 미 지정시 KSF파일이 있는 폴더내의 Intro.*을 읽어온다. 프로그램 상에서
KSF파일이 있는 폴더내의 mp3파일이나 Wav을 읽어온다.  
#SONGFILE : 배경음 파일의 위치를 지정한다. 미 지정시 KSF파일이 있는 폴더내의 Song.*을 읽어온다. 프로그램 상에서
KSF파일이 있는 폴더내의 mp3파일이나 Wav를 읽어온다.  
#DISCFILE : 디스크 이미지의 위치를 지정한다. 미 지정시 폴더내의 Disc.*을 읽어온다. 프로그램 상에서 KSF파일이 있는
폴더내의 bmp이나 png파일을 읽어온다.  
#TITLEFILE : 배경 이미지의 위치를 지정한다. 미 지정시 폴더내의 Title.*을 읽어온다. 프로그램 상에서 KSF파일이 있는
폴더내의 bmp이나 png파일을 읽어온다.  
#DIFFICULTY : 패턴의 난이도를 지정한다. 작성안해도 무방하며 작성의 보통은 '이정도 난이도가 돼요'정도의 의미. 값은 미기입하거나
정수로서 입력하며 [Kick it up](Kick%20it%20up.md) 당시에 지원하던 난이도의 최대값은 10이다.

  

요 5가지는 따로 작성할 필요가 없었는데 프로그램이 폴더내에 Intro.mp3, Song.mp3, Disc,bmp, Title.bmp만
제대로 넣어주면 알아서 읽어줬기 때문이다. 그리고 #DIFFICULTY 항목은 제작자 맘대로하면 되니까.

  

문제는 이 파일 형식에서 [변속](%EB%B3%80%EC%86%8D.md)을 시킬 때 쓰는 옵션인데 많이 골치아프다.  
#BPM2, #BPM3 : 1차변속, 2차변속시 사용되는 BPM수치 입력옵션이다.  
#BUNKI, #BUNKI2 : 1차변속, 2차변속시 변속을 할 시간을 곡이 시작된 기점으로 부터 1/100초 단위로 작성한다.  
#STARTTIME2, #STARTTIME3 : 1차변속, 2차변속시 패턴이 재개될 때까지 기다릴 시간을 1/100초 단위로 지정한다.

  

예로들면 곡이 120초(수치12000)이면 1차변속을 38.5초에서 하고싶다면 '3850'이라고 써주고 2차변속을 99.23초에서 하고싶으면
'9923'이라고 쓰면된다. 스타트타임은 변속이 시작되면서 그 부분을 기준으로 몇초 후에 스텝파일이 나오나는 소리.

  

이러다보니 옛날 문법으로 쓴 KSF파일들 자세히 들어다보면 온통길고 당시에 쓰이던 KSF EDITOR나 KSF MAKER, 그리고 KSF
CREATOR에서 작성하려면 스텝파일 작성후 TXT파일로 짜 붙여야 하는 구조이다. 또한 잘만 조절하면 순간변속이 가능하며 반대로 원
BPM보다 저속으로 변속도 가능하다. 그래서 구문법을 사용하던 시절에는 이 변속을 잘 이용하여 만드는 사람을 비유하자면 '고급문법'을 다루는
사람이라고 인식하였다.`[4]`

  

#STEP : 실질적으로 스텝이 어떻게 구성되어 있는지 되어있는 파일이다.  
파일의 구조는 다음과 같다.  
{{|AAAAABBBBBCCC|}}  
이 파일을 쉽게 설명하자면 다음과 같다.  
{{|↙↖▣↗↘↙↖▣↗↘◎◎◎|}}

  

A항목은 1p부분을 담당하고 B항목은 2P부분을 담당한다. C항목은 펌프잇업 스텝 데이터 파일에 유래된것으로 원래 이 부분은 펌프기계
모니터에 달려있는 ◎모양의 스피커형 램프를 점등 유무를 나타낸 것이다. 프로그램 구동 상 이 부분이 없어도 전혀 구동에 지장이 없기 때문에
에디터형 프로그램에서는 자동적으로 CCC부분을 제외시켰다.

  

각 항목의 숫자가 배정되어 있는데 숫자를 넣을 수 있는 항목은 0, 1, 2, 4이다.  
'0' 같은 경우 그 부분에 스텝이 없는거고 '1' 같은경우 그 부분에 스텝이 있는거다. 예로들면 '00011100000'은
'□□□↗↘↙□□□□□'라는 스텝을 작성한것이다.

  

그리고 '2'는 KSF파일의 종결어미로서 '2222222222'라고 작성한다. 또한 0.5.589 버전에 추가된 '4'는 롱노트 파일로서
4의 개수만큼 롱노트가 만들어진다.

  

이렇게 되면 KSF 구 문법의 옵션을 모두 **적용**한 파일의 구조는 다음과 같다.  
{{|  
#TITLE: title;  
#BPM: 128;  
#BPM2: 150;  
#BPM3: 200;  
#BUNKI: 2000;  
#BUNKI2: 6000;  
#STARTTIME: 100;  
#STARTTIME: 150;  
#STARTTIME: 0;  
#PLAYER: SINGLE;  
#TICKCOUNT: 4;  
#INTROFILE: intro.mp3;  
#SONGFILE: song.mp3;  
#DISCFILE: disc.bmp;  
#TITLEFILE: title.bmp;  
#DIFFICULTY: 22;  
#STEP:  
1000000000000  
0100400000000  
0010400000000  
0000400000000  
0000000000000  
2222222222222  
|}}

  

**길다.** 다이렉트 무브 나오기 이전에 변속적용된 KSF은 Introfile항부터 Titlefile항을 뺀 나머지 부분을 적용하였다.

  

또한 Kickitup 프로그램의 한계상 2048줄 이상의 KSF파일은 더 이상 읽지 못하는 경우가 발생한다. 2048줄 이상 데이터는 그냥
공백과 같다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=4)]

### 1.1.2. 신 문법 ¶

신 문법은 다이렉트 무브 한정에서만 적용되는 파일로 파일의 기본적 문법은 구 문법과 동일하다.

  

그러나 여기서 나머지 옵션이 바뀌는데 다음과 같다.

  

#TICKCOUNT: 정수; (또는 |T정수|) : #TICKCOUNT 값을 처음에 지정하거나 스텝 중간에서 바꾼다.  
#BPM: 실수; (또는 |B실수|) : #BPM 값을 처음에 지정하거나 스텝 중간에서 바꾼다.  
#DELAY: 정수; (또는 |D정수|) : 해당 위치에서 올라오는 스텝을 지정한 시간(1/1000초 단위)만큼 중단한다.  
#DELAYBEAT: 정수; (또는 |E정수|) : 해당 위치에서 올라오는 스텝을 박자만큼 중단한다.

  

특히 눈여길것은 BPM의 수 범위가 [실수](%EC%8B%A4%EC%88%98.md)가 되었는데 다이렉트 무브에서 음수범위로 적용하면
스텝의 스크롤이 아래에서 위가아닌 위에서 아래로 스크롤되는 버그가있다. 물론 이 때 박자맞춰서 눌러도 인식도 되지 않고 판정도 없어서
게이지가 깎이지 않는다. 그래서 일부러 KSF제작자들은 낚시 목적으로 작성하는 경우도 있다.

  

(|옵션|)항목은 스텝파일 중간에 적용이 가능하다.

  

참고로 문서를 작성하는데 [Guide to understand KSF
format](http://sparcs.kaist.ac.kr/~tokigun/article/ksfguide.php)을 참고하여 재
작성하였다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=5)]

## 1.2. KSF 커뮤니티의 역사 ¶

초기에는 [펌프 잇 업](%ED%8E%8C%ED%94%84%20%EC%9E%87%20%EC%97%85.md) 게임의 채보 파일을
구동하는 정도에서 그쳤으나, 본격 KSF가 알려지기 시작하면서 서서히 창작 채보들이 만들어지기 시작했으며 이후 WKM, DDM, 후에 FOR
등 KSF를 전문적으로 다루는 커뮤니티들이 본격적으로 성장세를 이루게 된다.

  

최초에는 Kickitup! 0.001 버전부터 시작했는데 0.004버전까지는 KSF파일이 아닌 stp라는 확장자의 파일로 스텝이
구동되었으며, 음악 재생기능도 없어 사실상 인지도가 거의 없었다. 그 후 0.2버전부터 본격 KSF 파일이 가동되었고, 이후 차츰 업데이트를
거치며 0.4a 버전에서는 mpg파일로 BGA 삽입이 가능한 수준까지 이른다.`[5]` 바로 다음 버전인 0.4b에서는 변속 기능까지
추가되었다.`[6]` 추후 이런 저런 버그들의 수정과 업데이트를 거치며, 최종적으로는 0.5 589의 개발을 마지막으로 노기태의 개발은
사실상 중단된다.

  

그 후 도라에몽과 몇몇 프로그래머들의 노력으로 BGA기능을 다시 되살린 버전을 내놓았으며, 여기에 롱노트 기능이 더해진 버전이자 KIU의
명실공한 마지막 버전인 KIU LN이 탄생한다. 그 전에도 KIU프로그램에 외전급으로 마우스 커서 지원 및 난이도 표시, Ez2DJ처럼
옆으로 게이지가 올라가는 등, 다양한 버젼이 존재하긴 하였다.

  

그 후 프로그래머이자, 채보 제작자인 Kiho가 제작한 다이렉트 무브로 옮겨가며, 변속의 3번 제한이 사라지고, 급변속 또한 지원하게 된다.

  

KSF의 역사는 펌프 잇 업 커뮤니티와 밀접한 관계를 갖고 있는데, KIU가 알려지지 않은 초창기`[7]`의 펌프 커뮤니티는 단순히 PIU
게임 수록곡의 채보 제공과 몇몇 정보만을 나열한 사이트가 대부분이었던지라, KIU를 비롯한 KSF의 인지도는 전무한 수준이었다.

  

하지만, 당시 펌프 유저였던 ⓩino`[8]`의 사이트가 펌프 채보 및 음악, KSF를 체계적이고 깔끔히 정리하여 제공하면서 본격적으로
유명세를 알리기 시작했고, 펌프와 KIU 전용사이트인 P.K World(Pump it up & Kick it up World)를
오픈하고,`[9]` 창작채보 자료실을 열면서부터 본격적인 자작 KSF 커뮤니티의 부흥기가 이루어지게 된다.`[10]` 그외에도 몇몇 당시에
이름을 널리 알리던 몇몇 유명한 KSF 메이커들의 개인 사이트가 오픈되면서 KIU는 펌프의 전성기와 더불어 더없는 호황기를 누린다.

  

하지만 추후 ⓩino의 입대 사정으로 P.K World는 KSF 데이터들만 남긴채 커뮤니티 기능은 봉쇄된 사실상 동결상태가 되고, 몇 개월
후, KSF 자료실의 호스팅 담당자이자`[11]` KIU의 개발자인 노기태마저 킥잇업 개발을 중단하고 안다미로사에 취직, KSF 자료실의
자료마저 소실되면서, KSF 커뮤니티의 독보적인 위치를 확립하고 있던 P.K World는 폐쇄되었다.`[12]`  
이후, P.K World라는 거대한 커뮤니티와 자료실이 사라지자, KSF계는 전반적으로 침체기를 맞게된다.`[13]` 하지만, 펌프
Rebirth 버전의 채보 작업을 진행중이던 몇몇 유저와 ⓩino에서 KSF 메이킹으로 유명세를 알리던 몇몇 유저들이 뭉쳐 차세대 KSF
커뮤니티인 D.D.M이 탄생하게 되었는데, 여기에서 커뮤니티의 운영방침이나 멤버들의 성격 차이에 기인하여 약간의 크고 작은 트러블이 생긴
후, 유명 KSF 유저 TOPNova를 중심으로 W.K.M이라는 팀으로 분열이 되고, KSF계는 사실상 D.D.M & W.K.M이라는
투톱체제를 이루게 되었다. 그 와중에서도 추후 펌프 공식 채보를 제작하는 Kang2나 EzPump, 희동이, ⓕlycu 등 몇몇 유명
유저들의 개인 사이트도 따로 운영되기도 하였다.

  

그리고 이 때부터가 사실상 KSF의 두 번째 전성기.`[14]` 펌프 잇 업이 Rebirth 이후 국내에 차세대 버전이 등장할 기미가 보이질
않자, KSF 커뮤니티를 비롯한 유저들은 서서히 펌프 잇 업 채보작업에서 발길을 돌리게 되었고, 본격적인 KSF 창작에 한 층 더 가속화를
진행하게 되었다.`[15]` 그리고 이 때 Kiho의 KIU 다음 세대의 KSF 구동기인 다이렉트 무브가 개발되었으며, 3번의 변속밖에 할
수 없던 KIU의 한계를 벗어난 무한대의 변속을 강점으로 삼아, 본격 낚시 채보 및 변태성 채보들 등 다양한 스타일의 KSF들이 제작되었다.

  

이후의 커뮤니티들은 Homepy 및 클럽박스를 이용 등 다양한 방식으로 운영되기도 하였지만, 카페와 블로그라는 당시엔 파격적이었던 커뮤니티
도구들이 생겨나고, 개인 홈페이지와 펌프의 유행의 하락, 또 다른 차세대 리듬게임들이 생겨나면서 KSF의 인지도 자체는 점점 저조해지기
시작, 자작 KSF의 제작과 제작자들의 수 또한 점차 감소하게 된다. D.D.M과 W.K.M은 이 시기에 F.O.R이라는 하나의 팀으로
통합하여 운영하게 되었는데, 대부분의 사이트가 폐쇄되어, 사실상 KSF 사이트의 구심점을 이루게 되었다. 하지만 도중에 펌프 Prex3
PC버전을 불법으로 개조하다 안다미로에게 고소크리를 먹을 뻔한 사건이 터져버린다. 이 일로 인해 F.O.R은 펌프 관련 KSF들을 모조리
삭제했으며, 이후에 관련 자료나 다이렉트 무브 랭킹에서 펌프 관련한 기록들이 올라오면 삭제하고 영구정지까지 먹이는 병크마저
터뜨린다.`[16]` 덕분에 사실상 펌프곡들을 즐기려고 KSF를 찾던 사람들의 발길은 뚝 끊겨버렸으며,`[17]` 이후의 F.O.R 내부의
커뮤니티 문제<del>라 쓰고 병크라 읽는다</del>들과 악재들이 겹치면서 F.O.R 또한 폐쇄. 현재는 극소수의 인원만이 남아 운영하는
DropNote가 유일한 KSF 커뮤니티의 구심점이 되었다. 하지만 이곳 또한 인원이 많은 스텝 매니아 쪽으로 넘어가게 되면서 사실상
KSF의 역사는 막을 내린 셈이 되었다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=6)]

## 1.3. 관련 사이트 ¶

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=7)]

### 1.3.1. 운영중인 사이트 ¶

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=8)]

#### 1.3.1.1. DropNote ¶

2007년, Forhythm의 주요 회원이었던 '타스'와 '말랑이(Whitecoma)'가 개설했으며, 초기의 이름은 TMKP(Tass &
Mallang-ee KSF Project)였다. 2009년 사이트명을 현재의 이름인 'Dropnote'로 변경하였다.

  

Forhythm이 없어지면서, 사실상 KSF을 대표하는 공식 사이트이다. Dropnote는 운영되고 있는 타 커뮤니티들과의 지속적인 교류를
하며 매년 합동 KSF에디션 제작을 주도하고 있다. 그러나 2012년 말부터 KSF의 비중이 줄고 스탭매니아의 비중이 늘기 시작하였다.

  

대표주소는 <http://www.dropnote.co.kr>이다. Forhythm의 주소인
<http://www.forhythm.com>으로도 접속이 가능하고, 한글 도메인인
[http://드놋.한국](http://%EB%93%9C%EB%86%8B.%ED%95%9C%EA%B5%AD)으로도 접속이 가능하다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=9)]

##### 1.3.1.1.1. 5kNote ¶

2011년 9월 11일 DropNote의 운영진인 '타스'가 개설한 카페. 기존의 KSF을 다루는 Dropnote와는 달리 스탭매니아만
다루기 위해서 만든 카페이다.

  

종래의 커뮤니티에서는 DirectMove를 KSF구동 프로그램으로 이용해왔지만 KSF포멧에 대한 인식률이 상당히 개선되고 네트워크 플레이가
가능해진 Stepmania-SSC를 다루는 커뮤니티.

  

현재는 다이렉트무브용 KSF를 스텝매니아에서 완벽구동이 가능하도록, 일종의 컨버젼을 하는 'StepmaniaConversion'`[18]`
프로젝트를 진행하고 있다.

  

카페 주소는 <http://cafe.naver.com/5knote>이다.

  
  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=10)]

#### 1.3.1.2. Creative Rhythm World ¶

2007년 3월 8일 Forhythm과는 별개로 '지송이'란 필명으로 개인적으로 활동하고 있었던 '만월군`[19]`'이 개설한 카페. 당시의
이름은 '지송이의 자작펌프'였다.

  

2010년 카페명을 현재의 이름인 'Creative Rhythm World'로 변경하였다. Forhythm 시절이나, 현재의 시점에도
KSF계에서 두번째로 규모가 큰 사이트이다.

  

카페 주소는 <http://cafe.naver.com/zisongi>이다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=11)]

### 1.3.2. 운영중단된 사이트 ¶

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=12)]

#### 1.3.2.1. Forhythm ¶

주요 운영진 : TOPNova(운영자), FISH (부 운영자), WindForce(부 운영자), 불포화(부 운영자)

  

Direct Move의 초기 개발진을 중심으로 만든 사이트. 운영자는 TOPNova. 이 사람은 Forhythm의 전신인 WKM을 운영하던
사람이기도 하다.

  

이 이전에 KSF 사이트는 크게 WKM이나 DDM을 대표로 하는 사이트가 양립하여 있는 상황이였으나 서로 합치게 되어 당시 KSF을 다루는
사이트 중에서는 가장 거대한 커뮤니티였다. 그러나, 2009년 3월, 공식적인 운영 중단 발표가 이루어진 후에 폐쇄되었다.

  

줄여서 FOR이라고 부르며, 풀네임은 Federation Of Rhythm이다.  
처음에는 DDM의 회원과 WKBM이 합쳐져서, 페라데이션 오브 리듬이었지만,  
그 후 MONO가 독립, 총 운영자 TOPNova만이 FOR을 운영하기에 이르러,  
Forward >> Rhythm 으로 개명, 요 근래의 FOR은 Forward Rhythm이라고 보면 된다.  
같은 F.O.R.이라하여도 그동안 혼자서 운영해온 TOPNova의 개인 홈페이지화가 되어버린 시기가 오래되어서, 페라데이션의 의미 자체는
사라졌다.

  
  

사이트 주소는 <http://forhythm.com>이며, 지금은 이 주소를 치면 Dropnote가 나온다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=13)]

#### 1.3.2.2. KSF.net ¶

2005년 KSF 제작자인 Flycu가 개설했다. 현재는 Flycu의 부재로 인해 운영이 중단되었으며, 지금은 방치되어 있다.

  

카페 주소는 <http://cafe.naver.com/ksfnet.cafe>이다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=14)]

#### 1.3.2.3. The Rhythm ¶

2008년 KSF 제작자인 EZpump가 개설한 사이트. 이 사이트는 특이하게도 KSF와 BMS를 같이 다루었다. 그러나, 2010년 이후로
거의 운영이 되지 않았다.

  

2011년 9월 20일, Ohpy의 서비스가 종료됨에 따라 자동으로 폐쇄되었다. 공식적인 운영중단 발표가 나오지는 않았다.

  

사이트주소는 <http://therhythm.wo.to>였다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=15)]

# 2. 그 외 ¶

1\. KMPlayer의 스킨 파일 확장자가 KSF다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=16)]

# 3. 각종 협회및 연맹의 약자 ¶

대한볼링협회 (Korea Bowling Congress)  
대한소프트볼협회 (Korea Softball Federation)  
대한사격연맹 (Korea Shooting Federation)  
대한수영연맹 (Korea Swimming Federation)

  

[[edit](http://rigvedawiki.net/r1/wiki.php/KSF?action=edit&section=17)]

# 4. 코리아 스피드 페스티벌(Korea Speed Festival) ¶

[홈페이지](http://www.ksfrace.com/)

`\----`

  * `[1]` '에뮬레이터'가 아닌 '시뮬레이터' 개념이며 제작자 역시 그렇게 불리길 원했다.
  * `[2]` 사실은 초기시절의 펌프잇업에 있던 스텝파일 형식과 유사하다. 이를 알 수 있는것은 구 문법 참고.
  * `[3]` 여담으로 Kick it up 당시 이 옵션이 4를 초과하면 판정인식이 밀려나는 버그가 있었다.
  * `[4]` 단, 순간변속이나 저속변속을 적용한 KSF파일을 옛날 킥잇업 프로그램로 읽으면 프로그램상 버그가 있어서 KSF파일 자체에도 없는 스텝파일이 나오기도 한다. 근데 이것은 miss가 난 상태에서 국한.
  * `[5]` 다만 이 BGA기능은 추후 삭제되었으며, 추후 또 다른 프로그래머 **도라에몽**에 의해 부활된다.
  * `[6]` 사실 이 때 킥잇업의 개발의도는 펌프 잇 업의 곡들을 PC로 가동시키는 것이었다. 하지만 펌프 잇 업 3rd에 등장했던 최초 변속 리믹스곡인 Remix 7 Banya Mix의 변속을 나타낼 방도가 기존 버전엔 존재치 않았고, 때문에 이 변속을 나타내기 위해 변속 기능이 추가된 것이었다.
  * `[7]` 시기상 1999~2000년 초
  * `[8]` 본인의 이름인 김진오에서 따온 것.
  * `[9]` 그 이전에 채보를 제공했던 페이지는 윈도우 탐색기를 모티브로 디자인 되었던 ⓩino의 개인 홈페이지였다. P.K World가 오픈하고 나서는 개인 홈페이지와 P.K World 두 종류의 사이트가 동시에 운영되었다.
  * `[10]` 이전에도 자작 KSF를 만드는 사이트는 조금씩 있었으나, KIU 자체가 인지도가 낮았기에 사실상 극소수였다. 그나마 펌프 잇 업의 수록 채보들을 세련된 컬러 그래픽으로 재생산하여 제공하던 유저 ejav의 사이트가 가장 인지도가 높았다.
  * `[11]` 노기태와 ⓩino는 웹상으로 친분이 두터운 관계였는데, 개인 서버 호스팅을 돌리고 있던 노기태가 ⓩino에게 서버 호스팅을 제공하고 있었다.
  * `[12]` 도중도중 휴가를 나온 ⓩino에 의해 사이트 보수가 이루어지긴 했지만, ⓩino 본인이 전역 후 펌프를 비롯한 KSF에 관련된 것들을 싹 접으면서 완전히 폐쇄되었다. ⓩino는 전역한 후 [DJMAX 시리즈](DJMAX%20%EC%8B%9C%EB%A6%AC%EC%A6%88.md) 관련 블로그도 운영했으나, 테크니카 발매 이후 이 역시 그만 두었다.
  * `[13]` 재밌는 점은 이 시기가 펌프 Extra가 출시한 직후 지점이었다는 것. 국내의 펌프 또한 Extra가 발매되고 나서부터 급격한 침체기를 맞이하였다.
  * `[14]` 시기상 2002년~2003년
  * `[15]` 이후 펌프 스텝 작업이 영 이루어지지 않은 것은 아니었으나, 사실 이쪽에 관련한 작업들은 거의가 [스텝 매니아](%EC%8A%A4%ED%85%9D%20%EB%A7%A4%EB%8B%88%EC%95%84.md)쪽으로 넘어가게 된다.
  * `[16]` 사실 고소를 먹을 뻔한 입장으로선 당연한 행동이지만, 경고를 주면 모를까 곧바로 영구정지를 먹여버려 후대사람들에게 상당히 까였다.
  * `[17]` 애초에 KIU나 다이렉트 무브나 KSF 자체를 접하는 사람들은 펌프를 통해서 접하는 경우가 십중팔구이기에 펌프에 흥미를 느끼던 사람들을 내쫓은 것은 주 고객층 전부를 배제한 것이나 진배없다. 이 점이 KSF 자체의 몰락을 초래하는데 가장 큰 원인이 되었다.
  * `[18]` 2012년부터는 Dropnote에서도 DirectMove를 대신할 프로그램으로 Stepmania를 다루기 시작하였다.
  * `[19]` 초대 리플렉 비트 시절에 유명했던 그 분 맞다

