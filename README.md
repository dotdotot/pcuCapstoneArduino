# 캡스톤 아두이노

주제 : 움직이는 공기청정기

- 주제 선정 과정에서 움직이는 공기청정기가 선정되어 하드웨어 사전 조사 및 구상 진행하였습니다.

    bp랩에서 만든 아두이노 공기청정기에 초음파 센서와 바퀴를 통하여 로봇청소기처럼 스스로 움직일수 있게 만들도록 구상했고
    초음파 센서와 아두이노 바퀴의 H브릿지 연결 및 회로도 조작에 대해 학습을 통하여 진행
     -!문제점 : 바퀴에서 2개의 바퀴로 진행을할지 4개의 바퀴로 진행할지의 고찰 ( 비용,성능)
            -> 4개의 바퀴를 이용하여 케이블을 통해서 앞뒤 바퀴를 병합, 같은 코딩으로 제자리회전 및 기동성 상승, 안정성 확보)
    
- 피드백 이후 공기청정기 + 로봇청소기로 주제 설정 변경
    공기청정기 및 바퀴 분해이후 3D맵핑에 필요한 YDLIDER 구매 후 ubuntu 설치 및 ROS 학습 진행
        !문제점 : ubuntu의 버전 충돌 및 ROS연계에 대하여 에러발생
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