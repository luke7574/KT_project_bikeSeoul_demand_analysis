# 공공데이터를 활용한 서울시 따릉이 수요 분석
---
## 프로젝트 개요
- 주제 : 서울시 따릉이 수요 분석
- 데이터 출처
>>1. 서울시 열린데이터 광장 - 서울시 공공자전거 이용정보(시간별)
>>2. 기상자료 개방 포털 - 해당 시점의 날씨 자료
- 중점 사항 : 시계열 데이터 전처리, 단변량/이변량 분석
- 목적 : 데이터를 활용한 시각화/수치화 통해 가설 수립, 가설 검증 통해 인사이트 도출 및 정책 방향 연구 
---

## 도메인 이해 
![image](https://github.com/user-attachments/assets/abc0b41d-388d-4b93-a522-b656981f285a)

![image](https://github.com/user-attachments/assets/e6bc2f68-60ef-4b5d-b20f-c48ddd1f86de)
---
## 사례소개 

- 자치구별 대여량/대여소
![image](https://github.com/user-attachments/assets/308c6c69-ecf8-4c7a-b929-6eeba3947f4a)
- 년도별 상위 10개 대여소
![image](https://github.com/user-attachments/assets/9d2089d9-393b-46a5-a90a-c8b30bc6b88d)
- 서울시 자전거 도로 현황
![image](https://github.com/user-attachments/assets/ba1acd1a-f114-4055-9e01-79e629610423)
---

## 가설 수립 
- 가설 1 : 강수 여부와 따릉이 수요량에는 관계가 있다.
- 가설 2 : 온도와 따릉이 수요량은 관련이 있다.
- 가설 3 : 오존 농도와 따릉이의 수요량에 관계가 있다.
- 가설 4 : 습도와 따릉이 수요량에는 관계가 있다.
- 가설 5 : 주말 여부와 따릉이 수요량에는 관계가 있다.
---

## 가설에 대한 분석 및 평가
### 가설 1 : 강수 여부와 따릉이 수요량에는 관계가 있다.
![image](https://github.com/user-attachments/assets/981fcdcf-545a-41a8-a23f-025768da5927)
- 강수 이후 시간이 경과함에 따라 5시간까지는 따릉이 수요가 감소하는 것을 확인할 수 있다.
- t-test 검정 결과 (statistic=20.998879971563788, pvalue=2.428442706503082e-94)

  t-통계량의 값이 매우 크고, p-value의 값 또한 유의수준보다 작은 값이 나왔다.
- **강수 여부에 따라 따릉이의 대여 수가 확연히 차이나는 모습을 확인할 수 있다.**

------------------------------------------------------------------------------------------
### 가설 2 : 온도와 따릉이 수요량은 관련이 있다.
- **(1번그래프)시간대별 온도**

  ![image](https://github.com/user-attachments/assets/0fcc22a3-74b7-4e10-9c10-e63bb035fd69)
- **(2번그래프)월 평균 온도**

  ![image](https://github.com/user-attachments/assets/b92cb252-5487-4e4b-a331-594812b29e25)
- **(3번그래프)월 평균 따릉이 대여수**

  ![image](https://github.com/user-attachments/assets/ab71ff09-d51f-41b8-8f21-8240f670acaf)
- **(4번그래프)온도에 따른 따릉이 수요변화**

  ![image](https://github.com/user-attachments/assets/32df4f93-a90d-41b7-b65d-8ba38cb9e07e)
- 3번 그래프를 통해 9월에 따릉이대여가 가장 높은것을 확인 할 수 있다.
- 2번 그래프를 통해 월 평균 온도를 보면 9월에 20도 ~ 24도 인것을 확인 할 수 있다.
- 4번 그래프를 보면 20도 ~ 25도 부근에 따릉이 대여가 많이 분포되어있는것을 확인 할 수 있다.

  
- 온도와 따릉이 대여 상관관계
  
  ![image](https://github.com/user-attachments/assets/38e0f336-583d-4230-a0e6-8d56f34a8897)

- 상관계수가 0.274, pvalue 2.58e-98 인것으로 보아 pvalue의 값이 0.05이하이므로 관계성이 있다고 판단



------------------------------------------------------------------------------------------
### 가설 3 : 오존 농도와 따릉이의 수요량에 관계가 있다.
- 오존 분포도 / 오존에 따른 대여량 / 시간대별 오존

  ![image](https://github.com/user-attachments/assets/59fbdba1-fe19-4f34-b932-c31034a1f8ae)
- 오존농도와 따릉이 상관관계

  ![image](https://github.com/user-attachments/assets/cc91de86-d9de-4a10-a598-1b545167672b)
  상관계수는 0.316, p-vlaue는 0에 거의 수렴하는 숫자이므로 상관관계가 높다고 할 수 있다.


------------------------------------------------------------------------------------------
### 가설 4 : 습도와 따릉이 수요량에는 관계가 있다.
- 습도에 따른 따릉이 대여량

  ![image](https://github.com/user-attachments/assets/d49a2aa5-a580-4798-b828-b79aadaddaa9)

- 습도가 높을수록 따릉이 수요가 낮아지는 우하향 직선의 경향을 보인다.
- 상관계수 -0.48, p-value 0으로 상관도가 매우 높지는 않지만, p-value가 0.05 이하이므로 관계가 있음을 알 수 있다.

------------------------------------------------------------------------------------------
### 가설 5 : 주말 여부와 따릉이 수요량에는 관계가 있다.
### 시간대와 자전거 대여 수요가 관계가 있다.

- 시간에 따른 수요변화

  ![image](https://github.com/user-attachments/assets/efe61051-f507-4635-9ff9-3fa610681e66)

  매일 수요가 작은 시간대는 **4시**이고, 제일 수요가 많은 시간대는 **18시** 이다.

  
- 오전 시간대에서는 출근시간인 8시, 오후 시간대에서는 퇴근시간인 18시가 가장 대여 수요가 많다.
- 오전 시간대에 비하여 오후 시간대가 수요량이 높은 편이다.
### 주말 여부에 따라서 따릉이 대여 수요가 다르다.**
- 시간대 및 요일별 평균 수요량

  ![image](https://github.com/user-attachments/assets/b5610ea4-269d-491d-a1a9-d6a78ec81560)
- 시간대 및 주말여부 평균 수요량

  ![image](https://github.com/user-attachments/assets/7fdfd269-8004-4619-9016-0a8c72063f5b)
- 주말은 출퇴근 하는 사람들이 평일에 비해 비교적 적기 때문에, 주말 여부에 따라서 자전거 대여 수요가 다르다.
- 주말여부에 대한 상관관계

  ![image](https://github.com/user-attachments/assets/ccf39265-bb96-4d41-875b-ae200064fd71)
  t 통계량은 3.8로 큰 수치이며, p-vlaue <0.05이므로 주말 여부와 자전거 대여 수요는 관계가 있다.


------------------------------------------------------------------------------------------

- **관계 분석**

  ![image](https://github.com/user-attachments/assets/adcbd405-943b-4edd-8d0e-1937d1c96bed)


> 강한 관계의 X
>> 강수 여부, 시간대, 오존, 온도

> 중간 관계의 X
>> 시정, 풍속

> 약한 관계의 X
>> 미세먼지 수치 

---
## 가설 검증 과정 

- **강수 여부 - 대여량**
  - 가설 : 비가 올때는 따릉이 대여량이 적을 것
  - 가설 검증을 통해 강우 여부에 따라 따릉이 대여량이 적음 확인

- **온도 - 대여량**
  - 가설 : 온도에 따라 대여량이 다를 것
  - 가설 검증을 통해 온도가 20도 ~ 25도 부근에 대여량이 많은 것을 확인

- **오존 - 대여량**
  - 가설 : 오존 수치가 낮을 때에는 따릉이 대여량이 높을 것
  - 가설 검증 통해 상관계수 0.316, p-value는 0에 수렴하므로 상관관계가 높음을 확인

- **습도 - 대여량**
  - 가설 : 습도가 높을수록 따릉이 대여량 적을 것
  - 가설 검증을 통해 상관계수 -0.48, p-value 0으로 상관도가 매우 높지는 않지만, p-value가 0.05 이하이므로 관계가 있음으로 확인

- **주말 여부 - 대여량**
  - 가설 : 주말은 출퇴근 하는 사람들이 평일에 비해 비겨적 적기 때문에, 주말 여부에 따라서 자전거 대여 수요가 다를 것
  - 가설 검증을 통해 t 통계량은 3.8로 큰 수치이며, p-vlaue <0.05이므로 주말 여부와 자전거 대여 수요는 관계가 있음
 
---
## 결론
- 미세먼지와 초미세먼지는 자전거 대여 수요에 거의 영향을 미치지 않았다.

- 자전거 대여 수요량은 강수 여부, 온도, 자외선과 관련된 오존수치 와 같은 환경 요소에 따라서 변화가 많다.

- 시간대, 주말에 따른 자전거 대여 수요량을 확인하였을 시, 사람들이 활동하는 시간대와 패턴을 알 수 있었다.

- 습도 역시 자전거 대여 수요와 상관관계가 있었다. 습도가 높아질수록 자전거의 대여 수요는 감소하는 모습을 보였으며 습도가 높아질수록 비가 올 가능성이 높아져 자전거 대여 수에 영향을 끼친 것으로 보인다.

- 사람들은 9월달에 따릉이를 가장 많이 이용한다. 9월의 평균 온도는 23도이며, 온도에따라 따릉이 수요변화를 확인해본결과 20도에서 25사이일때 많이 이용하는것으로 확인됐다. 따라서 사람들은 기온이 20도~25도일때 따릉이를 많이 이용한다고 판단했다.
