# 스파로스 아카데미 - 팀 웨이비(Wavey)

## 팀 구성
|김지욱(BE)|김민지(BE)|송윤서(FE)|신현채(BE)|홍미소(FE)|
|:-:|:-:|:-:|:-:|:-:|
|팀장<br>인프라 구성<br>CI/CD파이프 라인<br>카카오 결제<br>[Rental-service](https://github.com/spharos-wavey/rental-service)|백엔드 리더<br>DB Replication<br>kafka<br>[user-service](https://github.com/spharos-wavey/user-service)|프론트 리더<br>스크럼 마스터<br>[front](https://github.com/spharos-wavey/spharos-wavey-frontend)|[Vehicle-service](https://github.com/spharos-wavey/vehicle-service)|차량 예약 및 결제<br>[front](https://github.com/spharos-wavey/spharos-wavey-frontend)|

### Tech stack
Back-end  
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat&logo=Spring Boot&logoColor=white" />
<img src="https://img.shields.io/badge/Spring-6DB33F?style=flat&logo=Spring&logoColor=white" />
<img src="https://img.shields.io/badge/Spring Security-6DB33F?style=flat&logo=Spring Security&logoColor=white" />
<img src="https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white" />
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=MySQL&logoColor=white" />
<img src="https://img.shields.io/badge/jwt-000000?style=flat&logo=jsonwebtokens&logoColor=white" />
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white" />
<img src="https://img.shields.io/badge/apachekafka-231F20?style=flat&logo=apachekafka&logoColor=white"/>

FrontEnt  
<img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=white" />
<img src="https://img.shields.io/badge/Next.js-000000?style=flat&logo=Next.js&logoColor=white" />
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=TypeScript&logoColor=white" />
<img src="https://img.shields.io/badge/Recoil-5A29E4?style=flat&logo=Recoil&logoColor=white" />
<img src="https://img.shields.io/badge/Axios-000000?style=flat&logo=Axios&logoColor=white" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=HTML5&logoColor=white" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=CSS3&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=white" />


Tool  
<img src="https://img.shields.io/badge/IntelliJ IDEA-000000?style=flat&logo=IntelliJ IDEA&logoColor=white" />
<img src="https://img.shields.io/badge/Visual Studio Code-007ACC?style=flat&logo=Visual Studio Code&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub Actions-2088FF?style=flat&logo=GitHub Actions&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white" />
<img src="https://img.shields.io/badge/Google Cloud-4285F4?style=flat&logo=Google Cloud&logoColor=white" />

## 전기차 카 셰어링 서비스 BILLITA ([링크](https://billita.xyz))  (서버 상태 : CLOSE)

### 아키텍쳐 ###

<img src="https://github.com/spharos-wavey/.github/assets/90381800/216a5eee-6a38-4f4c-91ab-a579a6ddddd4" />

* 프론트엔드 서버는 버셀을 이용하였기에 버셀에서 CI/CD 진행
* 백엔드는 깃 액션을 통해 CI/CD 진행
* 프론트는 https, 백엔드는 http가 기본 프로토콜로 적용되어있음
  * 해당 문제를 해결하기 위하여 GCP load balancer를 사용하였음.

<details>
<summary>프로젝트 진행과정</summary>
<div markdown="1">

  **이벤트스토밍**  
 
  |팀 회의|결과물|
  |-|-|
  |<img src="https://github.com/spharos-wavey/.github/assets/90381800/10eb21f7-e036-4bb9-9b85-92f2d5bc0b71" width=400px height=250px>|<img src="https://github.com/spharos-wavey/.github/assets/90381800/fcbe101b-f8ca-4d10-a0fd-d8085d903a07" width=400px height=250px>|
 
 **DB설계**
 
 <table>
  <tr>
    <td>erd cloud</td>
    <td colspan="3">결과물</td>
  </tr>
  <tr>
    <td rowspan="2"><img src="https://github.com/spharos-wavey/.github/assets/90381800/fc27b89a-5fa9-4990-b01c-d66b49627018" width=400px height=250px></td>
    <td>user</td>
    <td>vehicle</td>
    <td>rental</td>
  </tr>
  <tr>
    <td><img src="https://github.com/spharos-wavey/.github/assets/90381800/9aa024a4-8af2-487b-bb9b-1fc7d8594c4e"></td>
    <td><img src="https://github.com/spharos-wavey/.github/assets/90381800/b6075249-8ee2-4a3b-8726-769964bec437"></td>
    <td><img src="https://github.com/spharos-wavey/.github/assets/90381800/35d1dab4-93c1-4a46-a69a-7b7248529149"></td>
  </tr>
</table>
  
</div>
</details>

<details>
<summary>DB replication test</summary>
 <div markdown="1">
  테스트 도구 : Jmeter
  <table>
   <tr>
    <td>예약 등록</td>
    <td>예약 조회</td>
   </tr>
   <tr>
    <td>예약 등록</td>
    <td>예약 조회</td>
   </tr>
  </table>
 </div>
</details>
