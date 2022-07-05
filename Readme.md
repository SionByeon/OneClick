# <image src="./app/src/main/res/drawable/icon.png" width="30"/> One Click

## 개발 팀원
- KAIST 새내기과정학부 김지나
- POSTECH 컴퓨터공학과 변민우

<br>

## 개발 환경
- OS: Android (minSdk: 26, targetSdk: 32)
- Language: Java
- IDE: Android Studio
- Target Device: Galaxy S7


<br>

## 앱 소개
One Click App은 연락처, 갤러리, 알람 기능을 가지고 있는 기본적인 앱이다. <br>
하단 3개의 탭을 통해 연락처, 갤러리, 알람 기능에 접근할 수 있다.
<br>

### 탭 1 . Contacts
<div>
<image src="./app/src/main/res/drawable/tab_phone_1.jpg" width="200"/>
<image src="./app/src/main/res/drawable/tab_phone2.jpg" width="200"/>
</div>


- 휴대폰 연락처 정보를 가져와 목록을 구성한다.
- 동기화 버튼을 클릭하면 연락처에 저장된 정보를 Listview로 보여준다. "+" 버튼을 클릭하였을 때, 주소록과 연동되어 새로운 연락처를 추가할 수 있고, 동기화 버튼을 누르면 추가된 연락처까지 함께 Listview로 보여준다.
- 각 목록을 클릭하면 기본 이미지와 함께 그 사람의 자세한 정보(이름, 전화번호)를 확인할 수 있고, 하단의 각 버튼을 클릭하면 전화, 문자를 할 수 있다.

<br>

### 탭 2 . Gallery
<div>
<image src="./app/src/main/res/drawable/tab_gallery_1.jpg" width="200"/>
<image src="./app/src/main/res/drawable/tab_fullscreen.jpg" width="200"/>
</div>


- 휴대폰 갤러리에서 사진을 가져와 목록을 구성한다.
- "+" 버튼을 클릭하면 휴대폰 갤러리에 접근할 수 있으며, 동시에 여러장을 선택하여 가져와 GridView를 이용하여 2 Columns로 보여준다.
- 불러온 사진을 클릭하면 Intent를 통해 `FullScreenActivity`를 실행하여 Full Screen을 볼 수 있다.
- 이미지를 추가하면 기존에 있던 이미지에 append 되어 추가 된다.
<br>
 

<br>

### 탭 3 . Alarm
<div>
<image src="./app/src/main/res/drawable/tab_alarm.jpg" width="200"/>
<image src="./app/src/main/res/drawable/alarm_check.jpg" width="200"/>
</div>

- 알람을 설정하고 알람이 울린 이후 알람을 끌 수 있다.
- 시간을 설정한 후 저장 버튼을 클릭하면, 하단에 알림창이 뜨고, 해당 시간에 알람이 울린다.
- 종료 버튼을 클릭하면, 알람을 끌 수 있다.

<br>

- `Notification` 과 `AlarmManager`을 이용하여 알림을 set하였다.
- AlarmReceiver class에서 `onReceive` method를 이용하여 알림을 notify하였다.

<br>


* * *
### Permission

전화 - 연락처 탭에서 특정 사람을 클릭한 후, 전화 버튼을 클릭했을 때, 전화 앱과 연동하기 위해 필요하다.
<br>


주소록 - 동기화 버튼을 클릭하면 주소록에 저장되어 있는 연락처들을 불러오기 위해 필요하다.

