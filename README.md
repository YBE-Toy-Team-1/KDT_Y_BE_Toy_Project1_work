## 토이 프로젝트1 JAVA


여행 여정을 기록과 관리하는 SNS 서비스 1단계


### 🕰️ 개발 기간

---

- 23.09.04 - 23.09.08

### 🧑‍🤝‍🧑 멤버 구성

---

- [권민우](https://github.com/Kwonminwoo)

- [권도형](https://github.com/tfedohk)

- [백인권](https://github.com/BackInGone)

- [임경민](https://github.com/pabu-lim)

- [유현](https://github.com/yuhyun1)

### ⚙️ 개발 환경

---

- Java 11
- Gradle
- 의존성
    - opencsv 5.7.1
    - jackson-databind 2.15.2


### 📌 주요 기능

---

#### - 여행 기록 및 여정 기록 기능
- 여행 일정 기록
- 하나의 여행에 여러 개의 일정 기록


#### - 여행 정보 조회 기능
- 저장된 여행 전체 리스트 조회
- 여행 전체 리스트에서 확인된 아이디를 입력하면 해당 여행 정보 조회
- JSON파일과 CSV파일 각각 조회

### 💡 착안사항

---

#### - MVC
- 컨트롤러
- 모델
- 뷰
- 서비스
- 레포지토리

#### - 예외처리
- 여행 정보가 없거나(파일입출력), 여정이 포함되어 있지 않다면 오류 메시지 출력
- 입력값이 가능한 범주에 없거나, 타입에 맞지 않으면 오류 메시지 출력
- JSON, CSV 파일 형식에 맞지 않다면 오류 메시지 출력
- 한글 문자가 깨지지 않게 처리

#### - 리팩토링
- 상수 패키지(constant) 분리
- 예외처리 패키지(exception) 분리
- DAO 패턴 사용(TripDao Class) : 서비스 로직과 데이터엑세스 로직을 분리하여 재사용성, 유연성 보장
- 유틸 패키지(util) 분리


### 💻 프로그램 실행 화면

---


#### 여행 기록


- 여행 기록 상황 1 : 여행 하나 - 세부 여정 2개_1
![여행 기록 상황1 여행 하나-세부 여정2개_1.jpg](img%2F%EC%97%AC%ED%96%89%20%EA%B8%B0%EB%A1%9D%20%EC%83%81%ED%99%A91%20%EC%97%AC%ED%96%89%20%ED%95%98%EB%82%98-%EC%84%B8%EB%B6%80%20%EC%97%AC%EC%A0%952%EA%B0%9C_1.jpg)


- 여행 기록 상황 1 : 여행 하나 - 세부 여정 2개_2
![여행 기록 상황1 여행 하나-세부 여정2개_2.jpg](img%2F%EC%97%AC%ED%96%89%20%EA%B8%B0%EB%A1%9D%20%EC%83%81%ED%99%A91%20%EC%97%AC%ED%96%89%20%ED%95%98%EB%82%98-%EC%84%B8%EB%B6%80%20%EC%97%AC%EC%A0%952%EA%B0%9C_2.jpg)


- 여행 기록 상황 2 : 여행 두 번 기록_1
![여행 기록 상황2 여행 두번 기록_1.jpg](img%2F%EC%97%AC%ED%96%89%20%EA%B8%B0%EB%A1%9D%20%EC%83%81%ED%99%A92%20%EC%97%AC%ED%96%89%20%EB%91%90%EB%B2%88%20%EA%B8%B0%EB%A1%9D_1.jpg)



- 여행 기록 상황 2 : 여행 두 번 기록_2
![여행 기록 상황2 여행 두번 기록_2.jpg](img%2F%EC%97%AC%ED%96%89%20%EA%B8%B0%EB%A1%9D%20%EC%83%81%ED%99%A92%20%EC%97%AC%ED%96%89%20%EB%91%90%EB%B2%88%20%EA%B8%B0%EB%A1%9D_2.jpg)



---
#### 여행 조회




- 여행 조회 상황 1 : JSON형식 선택하여 조회
![여행 조회 상황1-JSON형식 선택하여 조회.jpg](img%2F%EC%97%AC%ED%96%89%20%EC%A1%B0%ED%9A%8C%20%EC%83%81%ED%99%A91-JSON%ED%98%95%EC%8B%9D%20%EC%84%A0%ED%83%9D%ED%95%98%EC%97%AC%20%EC%A1%B0%ED%9A%8C.jpg)


- 여행 조회 상황 2 : CSV형식 선택하여 조회
![여행 조회 상황2-CSV형식 선택하여 조회.jpg](img%2F%EC%97%AC%ED%96%89%20%EC%A1%B0%ED%9A%8C%20%EC%83%81%ED%99%A92-CSV%ED%98%95%EC%8B%9D%20%EC%84%A0%ED%83%9D%ED%95%98%EC%97%AC%20%EC%A1%B0%ED%9A%8C.jpg)


- 여행 조회 상황 3 : 저장된 여행이 없을 때 조회
![여행 조회 상황3-저장된 여행이 없을 때 조회.jpg](img%2F%EC%97%AC%ED%96%89%20%EC%A1%B0%ED%9A%8C%20%EC%83%81%ED%99%A93-%EC%A0%80%EC%9E%A5%EB%90%9C%20%EC%97%AC%ED%96%89%EC%9D%B4%20%EC%97%86%EC%9D%84%20%EB%95%8C%20%EC%A1%B0%ED%9A%8C.jpg)


---
#### 예외 처리


- 예외 처리 1 : 옵션 선택지 정수 입력, 옵션 범위 확인 후 예외 처리
![예외처리1-옵션 선택지 정수입력, 옵션 범위 확인 후 예외처리.jpg](img%2F%EC%98%88%EC%99%B8%EC%B2%98%EB%A6%AC1-%EC%98%B5%EC%85%98%20%EC%84%A0%ED%83%9D%EC%A7%80%20%EC%A0%95%EC%88%98%EC%9E%85%EB%A0%A5%2C%20%EC%98%B5%EC%85%98%20%EB%B2%94%EC%9C%84%20%ED%99%95%EC%9D%B8%20%ED%9B%84%20%EC%98%88%EC%99%B8%EC%B2%98%EB%A6%AC.jpg)


- 예외 처리 2 : 사용자가 입력한 여행 ID로 여행 조회 불가 시 예외 처리
![예외처리2-사용자가 입력한 여행ID로 여행 조회불가 시 예외처리.png](img%2F%EC%98%88%EC%99%B8%EC%B2%98%EB%A6%AC2-%EC%82%AC%EC%9A%A9%EC%9E%90%EA%B0%80%20%EC%9E%85%EB%A0%A5%ED%95%9C%20%EC%97%AC%ED%96%89ID%EB%A1%9C%20%EC%97%AC%ED%96%89%20%EC%A1%B0%ED%9A%8C%EB%B6%88%EA%B0%80%20%EC%8B%9C%20%EC%98%88%EC%99%B8%EC%B2%98%EB%A6%AC.png)



---
#### 서비스 종료

![서비스 종료-메인화면에서 종료.jpg](img%2F%EC%84%9C%EB%B9%84%EC%8A%A4%20%EC%A2%85%EB%A3%8C-%EB%A9%94%EC%9D%B8%ED%99%94%EB%A9%B4%EC%97%90%EC%84%9C%20%EC%A2%85%EB%A3%8C.jpg)

---
#### 파일 출력 결과
![image](https://github.com/Kwonminwoo/KDT_Y_BE_Toy_Project1_1/assets/34360434/6ac8b553-149d-4d1f-897d-e4f7a8af3be8)
![image](https://github.com/Kwonminwoo/KDT_Y_BE_Toy_Project1_1/assets/34360434/83475ca7-81ff-4855-aff6-502db2908b79)



---



### 🛠️ UML Diagram



---

![UML 다이어그램.png](img%2FUML%20%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8.png)


### 📝 Sequence Diagram

---

![시퀀스 다이어그램.png](img%2F%EC%8B%9C%ED%80%80%EC%8A%A4%20%EB%8B%A4%EC%9D%B4%EC%96%B4%EA%B7%B8%EB%9E%A8.png)



