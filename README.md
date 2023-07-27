[2023-06-27 오타 수정]

# Project_Final #

-----------------------------------

https://docs.google.com/presentation/d/1lNkvvwCKJEGnOMeBa-MwexF7AqvAFYjE/edit?usp=sharing&ouid=117701096765562912938&rtpof=true&sd=true <br>


### 최종 ppt는 용량이 커서 github에 파일이 올라가지 않아서 구글 드라이브에 업로드하고 링크 올립니다 <br>
-----------------------------------


## 아이디어 제안서
### 주제 : < 아두이노를 활용한 블루투스 자동 호출 엘리베이터 ><br>
### 팀명: 아이오토<br>
### 팀원 : 20182640 김시연, 20182644 홍주혜, 20185014 이하연<br><br>
### ● 프로젝트 개요 (개발할 프로젝트의 전체적인 개요 작성 (전체구상도 그림 포함)<br>

![image](https://user-images.githubusercontent.com/109746200/180240276-403ab4fb-50e3-4de8-8572-d7c235713764.png)

-엘리베이터 안쪽 스위치, led, 7세그먼트<br><br><br><br>
![image](https://user-images.githubusercontent.com/109746200/180240391-7ee4d734-ef30-4ea3-aeec-6217f6830816.png)

-스마트폰과 아두이노 블루투스 연결<br><br><br><br>
![image](https://user-images.githubusercontent.com/109746200/180240423-224a694f-a87f-4b7b-935f-e143e55d1484.png)

-앱인벤터를 이용해 엘리베이터를 호출 할 수 있는 1층 ~ 9층 버튼 만들기<br>
<br>
### ● 개발 동기 및 필요성 (제안하는 시스템의 개발 동기 및 필요성에 대한 설명)<br>
 팀원중 물류 받는 아르바이트를 하는 팀원이 있음. 평균 120박스 정도의 많은 물류를 받기 때문에 시간안에 마치기 위해선 스피드가 생명임. 물류를 옮길 때 가장 많은 시간이 지체되는 곳은 고층에 가있는 엘리베이터를 호출할 때임. 따라서 물류를 끌고 엘리베이터를 타러 갈 때 스마트폰으로 미리 엘리베이터를 호출한다면 물류를 더욱 빠른 시간 내에 옮길 수 있다고 늘 생각함. 현장에서 사용되는 엘리베이터는 직원 전용이지만, 별다른 보안이 되어 있지 않아 외부인 출입이 잦다는 점, 엘리베이터의 하차 위치가 물류창고라 도난 문제가 생길 수 있다는점 등을 고려하여 버튼을 엘리베이터 안에만 만듦. 외부인은 밖에서 엘리베이터를 호출하지 못하고 피치못할 사정에만 직원하에 문을 열고 원하는 층을 골라 갈 수 있게 만듦.<br><br>

### ● 프로젝트 개발(추진)내용 (개발할 프로젝트의 전반적인 내용 설명)
 <br>
1) 엘리베이터 층수 선택<br>
● 기능설명: 엘리베이터에 탑승한 후 상하스위치를 이용하여 가고 싶은 층을 선택하고 이동버튼을 누르면 엘리베이터가 해당 층으로 이동함. <br>
● 구상: 외부인 출입을 자제하기 위해 일반적인 엘리베이터와 다르게 밖에서 호출 할 수 있는 버튼을 만들지 않음. 호출은 반드시 아두이노와 연동된 스마트폰으로만 가능. 또한 핀 최소화를 하기 위해 상승, 하강, 이동 버튼으로만 구성. (단, 마지막 층에서 상승버튼을 눌렀을 땐 다시 1층으로, 1층에서 하강버튼을 눌렀을 땐 9층으로 변경됨) <br>
<br>
2) 엘리베이터 층수 이동<br>
● 기능설명: 원하는 층수를 선택한 후 이동 스위치를 누르면 서보모터를 활용하여 이동.<br>
● 구상: 상승버튼 또는 하강버튼을 눌렀을 때 숫자가 1씩 증가하거나 감소하는 것을 7세그먼트로 확인할 수 있음. 선택한 층을 7세그먼트로 확인한 후 이동버튼을 누르면 서보모터가 선택한 층으로 설정한 각도만큼 돌아간다.<br>
<br>
3) 엘리베이터 잠시 멈춤 & 도착알림<br>
● 기능설명: 사용자가 엘리베이터를 탑승, 하차 시간을 충분히 제공하기 위해 원하는 층에 도착한 후 일정시간동안 서보모터 및 상하버튼이 작동되지 않음. 엘리베이터의 도착을 알리는 표시등 <br>
● 구상: 서보모터가 작동되고 3초가량 딜레이가 들어간다. 이 3초는 문이 열리는 시간을 위해 만들었다. 선택한 층에 도착하면 led가 켜지고 5초가량 딜레이가 들어간다. 엘리베이터의 도착을 알려준다. 즉, 3초동안 엘리베이터 문이 열리고 led가 켜지는 5초 동안은 사용자가 안전하게 타고 내릴 수 있다. (스위치 , 서보모터가 작동되지 않기 때문)<br>
<br>
4) 스마트폰 - 아두이노 블루투스 연동 및 앱인벤터<br>
● 기능설명: 스마트폰과 아두이노를 블루투스로 연동한 후, 앱인벤터를 활용하여 사용자가 스마트폰 앱에 접속후 원하는 층수버튼을 클릭함으로써 엘리베이터를 조작함.<br>
● 구상: 앱인벤터를 활용하여 엘리베이터 앱을 간단하게 만듦. (앱에는 1층~9층 버튼이 만들어질 예정) 그리고 엘리베이터를 조작하는 아두이노에 블루투스 모듈을 연결하여 아두이노와 스마트폰이 통신할 수 있게 만들 예정임. <br>
<br>

### ● 시스템 구성 요소 (개발 시스템에 사용된 소자 및 사용용도 설명)

항목
목적
서보모터
엘리베이터의 층수 이동을 담당
led
엘리베이터의 도착을 알리는 표시등
스위치 버튼
엘리베이터 층수를 누르는 버튼
블루투스
아두이노와 스마트폰 연동
7세그먼트
엘리베이터의 층수를 알리는 문구







![image](https://user-images.githubusercontent.com/94774284/180189535-0387c58a-644e-45a3-b0d5-10c08a468a9e.png) <br><br>








![image](https://user-images.githubusercontent.com/94774284/180189063-6e5f900e-ba5d-4f0d-8814-166974f17bd3.png) <br><br>




### 산학 SW 프로젝트 

### 조선대학교 컴퓨터공학과 

### 20182644 홍주혜 
