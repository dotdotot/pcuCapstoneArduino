# 캡스톤 아두이노

주제 : 움직이는 공기청정기

- 주제 선정 과정에서 움직이는 공기청정기가 선정되어 하드웨어 사전 조사 및 구상 진행하였습니다.

아두이노 공기청정기에 초음파 센서와 바퀴를 통하여 로봇청소기처럼 스스로 움직일수 있게 만들도록 구상했습니다

필요물품 : 공기청정기프레임, 온습도 센서(DHT11), 미세먼지 센서(GP2Y1014AU), 아두이노 초음파센서 (HC-SR04), LED전광판, 블루투스 모듈, 아두이노 바퀴, 아두이노 우노, LED불빛, 브레드보드
    
- 구상 : 공기청정기 스스로 집안 구조를 파악한 후 돌아다니면서 미세먼지, 온습도 확인 및 공기청정기 가동

아두이노 우노에 대하여 3.3V와 5V의 차이점, GND 아날로그 신호, 디지털 신호에 대하여 학습진행하였습니다.
디지털 신호 : 어떠한 정보, 자료, 물체, 지표 등을 0과 1로 표기하는 것
아날로그 신호 : 디지털핀이 0과 1로 표기하는것과 달리 아날로그신호는  0~1023의 정수로 표기하는 것

미세먼지 센서 : 대기중에 떠다니거나 흩날려 내려오는 직경 10um이하의 입자상 물질을 측정해 내는 센서

온습도 센서 : 정전식 습도 센서와 시미스터를 사용하여 대기온도와 습도를 측정하고 디지털 센서 신호로 출력하는 센서 

![회로](https://user-images.githubusercontent.com/102634570/190965744-843503e5-474f-4274-9c2d-fb06348a80c6.jpg)

문제점 : 거리측정
-> 거리측정 같은 경우 아두이노에 적외선 센서와 초음파 센서가 있는것을 확인하였고 공기청정기가 작동되려면 미세먼지가 있어야 되기 때문에 적외선 센서같은경우 객체가 움직임이 있을때만 감지가 가능하지만 초음파 센서같은 경우 객체의 움직임이 없어도 탐자가 되었고, 적외선 센서같은 경우에는 유리창이 있을경우 감지가 어렵다는 정보를 확인하여 초음파 센서로 사용하였습니다.

초음파 센서 : 20kHz이상의 주파수 소리를 보낸후 반사되어 돌아오는 시간차를 이용하여 거리를 알수있는 센서
    
문제점 : 근거리 통신
-> 아두이노 같은경우에는 유선통신인 시리얼통신을 사용합니다. 공기청정기가 움직이려면 무선을 통한 통신을 진행해야되는데 아두이노에는 WIFI모듈과 블루투스 모듈이 있는것을 확인하였고 두개를 비교한 결과 저렴하고 다루기가 쉽고 범용성이 높은 블루투스 모듈을 사용하였습니다

블루투스 모듈 : 무선통신을 위한 모듈

-제작과정
유튜브를 통하여 프레임 설계 및 회로도에 대한 정보를 확인하고 기초가되는 공기청정기의 뼈대 및 회로도 정리를 완료하였습니다.
또한 우노 코딩을 진행하여 각 디지털, 아날로그 핀별로 어떤 역할을 진행하고있는지, 브래드보드에 +,-선 연결방법등에 대해 학습 진행하였습니다.


이후 블루투스 모듈을 연결하여 근거리 통신을 진행 하던중 정보를 어떤 방식으로 보내는지 확인하기 위하여 검색한 결과 휴대폰으로도 정보를 입력 받을수 있는것을 확인하였고 휴대폰에 아두이노 블루투스 어플을 설치 이후 데이터 결과값을 전송 받을수 있도록 진행하였고 결과값을 도출해 낼 수 있었습니다

![휴대폰 결과값](https://user-images.githubusercontent.com/102634570/190965746-c7b781fa-01e8-4185-930c-1933e52542c9.jpg)

문제점 : 집 안을 돌아다니면서 초음파센서로 장애물 탐지를 하는데 있어서 크기에 비해 초음파 센서 하나로는 감지가 어려운것을 파악 하였고, 이러한 문제점을 해결하기 위하여 초음파 센서 밑에 서보모터를 달아서 초음파 센서를 회전시키며 전방에 대한 장애물 감지를 조금더 용이하게 할수 있도록 진행하였습니다.

![초음파센서 + 서보모터](https://user-images.githubusercontent.com/102634570/190965733-e00f1dbc-c1a3-44aa-80fa-bfe12ff47166.jpg)

문제점 : 바퀴의 경우 2개만 달경우 안정성이 떨어져서 무게추를 다는것, 앞쪽에 바퀴 하나를 더 다는것, 바퀴를 총 4개를 다는것으로 안정성 확보를 위해여 3개의 방안을 준비했지만 앞서 말한 2가지의 경우 제자리에서 방향 전환에 있어서 어려움을 확인하고 4개의 바퀴를 달아서 제자리 회전에 있어서 용이할수 있도록 만들고 추가적으로 안정성까지 확보 할 수 있었습니다.

![아두이노 바퀴](https://user-images.githubusercontent.com/102634570/190965739-bc1092a0-7277-4e8d-9e70-000d3114d208.jpg)

문제점 : 전원 같은경우 무선으로 움직이는데 있어서 배터리 장착에 대한 필요성을 느끼고 배터리 부착을 통한 무선으로 움직일수 있도록 설계하였고 충전식 건전지와 배터리 홀더를 통하여 무선으로도 작동을 가능하게 할 수 있도록 설계 진행하였습니다
    
![배털](https://user-images.githubusercontent.com/102634570/190965742-aad2eaee-6b0e-4e7f-a646-d62e52f519be.jpg)

- 피드백 이후 공기청정기 + 로봇청소기로 주제 설정 변경
공기청정기 및 바퀴 분해이후 3D맵핑에 필요한 YDLIDER 구매 후 ubuntu 설치 및 ROS 학습 진행

<라이더 센서 src = "https://user-images.githubusercontent.com/102634570/190965748-22064bc4-864b-412e-81c9-a96c8374d6f1.png" width="200" height="400"/>

문제점 : ubuntu의 버전 충돌 및 ROS연계에 대하여 에러발생
     -> 우분투 다운그레이드 및 ROS재설치 진행
       ->알수없는 에러 발생 및 설치 중단
        -> ubuntu의 부족한 학습 및 익숙하지 않은 소프트웨어 및 할당량 부족등등 이유로 ubuntu에서 window ROS로 변경
    
-Window ROS로 변경후 설치 및 학습 진행
    - ROS설치 이후 gozabo 학습 진행 ~2022.09.19








참고 사이트
- 아두이노 공기청정기 회로도 : https://www.youtube.com/watch?v=riergzv41AU
- 아두이노 공기청정기 프레임 : https://www.youtube.com/watch?v=riergzv41AU
- 아두이노 bp랩 코드 및 바퀴 코딩 : https://github.com/yoonsongjik/Capstone-Design
- 우분투 설치 : https://ubuntu.com/download/desktop
- 우분투 ROS설치 :https://krobot.tistory.com/entry/ROS-ubuntu-1804%EC%97%90%EC%84%9C-ROS-melodic-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0
-우분투 ROS : https://taemian.tistory.com/entry/1-2-ROS-%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0
- 우분투 다운그레이드 18.04 버전 : https://dora-guide.com/ubuntu-download/
- 윈도우 ROS 설치 : https://medium.com/@cyjun0304/%EC%9C%88%EB%8F%84%EC%9A%B0-10%EC%97%90-ros-melodic-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0-d2412168aeb4
- 윈도우 ROS설치 영상 : https://www.youtube.com/watch?v=mO_ilabG63I
- gozebo 학습 : https://blog.naver.com/PostView.nhn?blogId=ycpiglet&logNo=222158109284&categoryNo=90&parentCategoryNo=0