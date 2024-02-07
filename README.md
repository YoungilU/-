# 서울시 평균 기온 예측 AI 해커톤
## 주제
서울시의 평균기온을 예측하는 AI 알고리즘 개발
<br>
<br>
## **데이터**
https://dacon.io/competitions/official/236200/data
<br>
<br>
## **프로젝트 배경**
[Dacon 해커톤 38회, 서울시 평균 기온 예측 AI 해커톤]

서울시의 평균기온을 예측하는 인공지능 모델을 개발하는 것을 목표로 합니다.  

제공된 데이터를 통해 기온 및 일교차, 강수량, 평균습도 등 다양한 날씨 데이터를 분석합니다.

## **프로젝트 과정**
#### 1.라이브러리와 데이터 불러오기
#### 2.전처리
##### - 최고기온, 최저기온, 일교차, 평균풍속, 일조합: 결측 데이터를 해당 데이터의 뒤의 값을 대체
##### - 일사합, 일조율: 결측 데이터를 매년 같은 날짜의 평균 값으롣 대체
##### - 강수량: 결측치 비율 60%, RandomForest 모델을 활용해 강수량을 예측하여 결측치 대체
##### - 날짜 데이터: datetime 타입으로 변경
#### 3.평균기온 예측 모델 생성
##### - 시계열 데이터 분석 모델 선정 -> ARIMA, PROPHET 중 더 나은 성능을 보이는 PROPHET 채택
#### 4.하이퍼파라미터 그리드 설정(GridSearchCV)
#### 5.모델 학습
#### 6.예측 모델 생성 
