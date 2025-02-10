# Hi6 로봇제어기 기능설명서 - 사용자 정의 에러/경고

{% hint style="warning" %}
본 제품 설명서에서 제공되는 정보는 HD현대로보틱스의 자산입니다.

HD현대로보틱스의 서면에 의한 동의 없이 전부 또는 일부를 무단 전재 및 재배포할 수 없으며, 제3자에게 제공되거나 다른 목적에 사용할 수 없습니다.



본 설명서는 사전 예고 없이 변경될 수 있습니다.



**Copyright ⓒ 2025 by HD Hyundai Robotics**
{% endhint %}# 1. 개요

{% hint style="info" %}
이 기능은 V60.30-00 및 이후 버전부터 지원됩니다.
{% endhint %}

# 1.1 사용자 정의 에러/경고 기능

본 기능은 Hi6 로봇 제어기에 사용자가 특정 조건에 대한 에러 및 경고를 정의하고, 조건을 충족시켰을때 사용자가 정의한 에러 및 경고를 발생시키는 기능입니다.# 2. 기본 설정

Hi6 로봇 제어기에 사용자 정의 에러/경고를 설정하는 방법을 설명합니다.

# 2.1 사용자 정의 에러 설정

1. \[시스템 &gt; 4: 응용 파라미터 &gt; 13: 사용자 정의 에러\] 메뉴를 터치하십시오.<br><br>
2. '샘플파일 생성' 버튼을 클릭하십시오.<br>
* MAIN/project 경로에 'help_user_err.json' 파일이 생성됩니다.
<p align="center">
 <img src="../_assets/image1.png"></img>
 <em><p align="center">그림 1 샘플파일 생성</p></em>
</p>

3. 설정화면 재진입 시 샘플파일에 작성된 사용자 정의 에러가 표시됩니다.
-   에러 코드 : 발생시킬 에러 코드를 지정합니다.
-	조건식 : 해당 에러를 발생하기 위한 조건식을 지정합니다. 조건식은 if문에서 사용되는 조건식은 모두 가능합니다.
-	메시지 : 해당 에러가 발생할 때 출력되는 메시지를 지정합니다.
-	모터 off : 사용자 지정 에러가 발생되는 경우에 모터 off 동작 여부를 지정합니다.
<p align="center">
 <img src="../_assets/image2.png"></img>
 <em><p align="center">그림 2 사용자 정의 에러 샘플</p></em>
</p>

4. 티칭 펜던트에 USB를 장착하고, 파일 관리자 메뉴로 진입하여 'help_user_err.json' 파일을 USB 경로로 복사합니다.<br><br>
<p align="center">
 <img src="../_assets/image3.png"></img>
 <em><p align="center">그림 3 사용자 정의 에러 설정 파일</p></em>
</p>

5. PC에서 파일을 열고 정의할 에러를 샘플파일 양식에 맞게 편집합니다.(메모장으로 편집 가능)<br><br>
<p align="center">
 <img src="../_assets/image4.png"></img>
 <em><p align="center">그림 4 사용자 정의 에러 편집</p></em>
</p>
-   E65###: 에러 코드(설정 범위 E65001 ~ E65500)
-	cnd : 조건식
-	msg : 에러 도움말에 표시되는 원인 메시지
-   remedy : 에러 도움말에 표시되는 조치 방법
-	mot_off : 모터 off

6. 편집된 파일을 다시 티칭 펜던트로 복사합니다.# 2.2 사용자 정의 경고 설정

1. \[시스템 &gt; 4: 응용 파라미터 &gt; 14: 사용자 정의 경고\] 메뉴를 터치하십시오.<br><br>
2. '샘플파일 생성' 버튼을 클릭하십시오.<br>
* MAIN/project 경로에 'help_user_warn.json' 파일이 생성됩니다.
<p align="center">
 <img src="../_assets/image5.png"></img>
 <em><p align="center">그림 5 샘플파일 생성</p></em>
</p>

3. 설정화면 재진입 시 샘플파일에 작성된 사용자 정의 경고가 표시됩니다.
-   경고 코드 : 발생시킬 경고 코드를 지정합니다.
-	조건식 : 해당 경고를 발생하기 위한 조건식을 지정합니다. 조건식은 if문에서 사용되는 조건식은 모두 가능합니다.
-	메시지 : 해당 경고가 발생할 때 출력되는 메시지를 지정합니다.
<p align="center">
 <img src="../_assets/image6.png"></img>
 <em><p align="center">그림 6 사용자 정의 경고 샘플</p></em>
</p>

4. 티칭 펜던트에 USB를 장착하고, 파일 관리자 메뉴로 진입하여 'help_user_warn.json' 파일을 USB 경로로 복사합니다.<br><br>
<p align="center">
 <img src="../_assets/image7.png"></img>
 <em><p align="center">그림 7 사용자 정의 경고 설정 파일</p></em>
</p>

5. PC에서 파일을 열고 정의할 경고를 샘플파일 양식에 맞게 편집합니다.(메모장으로 편집 가능)<br><br>
<p align="center">
 <img src="../_assets/image8.png"></img>
 <em><p align="center">그림 8 사용자 정의 경고 편집</p></em>
</p>
-   W65###: 경고 코드(설정 범위 W65001 ~ W65100)
-	cnd : 조건식
-	msg : 경고 도움말에 표시되는 원인 메시지
-   remedy : 경고 도움말에 표시되는 조치 방법

6. 편집된 파일을 다시 티칭 펜던트로 복사합니다.# 2. 기본 설정

Hi6 로봇 제어기에 설정한 사용자 정의 에러/경고를 발생시키는 예제를 설명합니다.

# 3.1 사용자 정의 에러 예제

1. 'help_user_err.json' 파일을 아래와 같이 수정합니다.
<p align="center">
 <img src="../_assets/image9.png"></img>
 <em><p align="center">그림 9 샘플파일 생성</p></em>
</p>

2. 조건식을 만족시키기 위해 di5번 신호를 on하면 E65001이 발생합니다.
<p align="center">
 <img src="../_assets/image10.png"></img>
 <em><p align="center">그림 10 사용자 정의 에러 발생</p></em>
</p>

3. 에러에 대한 도움말을 확인하면 작성한 내용과 동일한 내용을 확인할 수 있습니다.

<p align="center">
 <img src="../_assets/image11.png"></img>
 <em><p align="center">그림 11 사용자 정의 에러 도움말</p></em>
</p>