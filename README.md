Regression Project ; Toyota Corolla Price Prediction
===================

Abstract
-------------

>[프로젝트 목표]
 제시된 Toyota사의 Corolla차량의 중고차 가격 데이터(training)를 바탕으로 회귀분석을 통해 새로이 제시되는 중고차 가격(test)을 예측해 보는 것이다.
 
> - **training data : 1019 rows, 39 columns**
> - **test data : 417 rows, 38 columns(price열 제외)**
 
> [프로젝트 평가]
> - 실제 가격과 예측한 가격의 차이를 **Root-Mean-Squared-Error(RMSE)** 를 통하여 채점한다.
 
-------------

Methods & Process
-------------

> **데이터 탐색 및 분석**
> - 예측해야할 종속 변수 데이터(Price)를 위해 사용되어야 할 독립 변수 데이터들을 탐색하여 실수 값 (정량적) 변수와 카테고리 값 (정성적) 변수로 분리하였다. 이후 이 변수들간의 상관도 분석(상관계수 및 t,F-test 검정)을 통해 연식, 주행거리 등 약 8개의 독립 변수를 선정했다.

> **회귀 분석 및 평가**
 > - 1차 선정된 회귀식(아래)으로 Ordinary Least Squares 방식으로 성적을 도출한다.
1차 선정 :  차량연식 + 주행거리 + 에어콘옵션 + 자동에어컨옵션 + CD플레이어옵션 + 중앙잠금 + 보드컴퓨터
R-Squared 값 0.859로 성능은 만족스러우나, 정규성(Normality) 불만족

> **아웃라이어 제거, 변수 변환 및 정규화**
> - 실수값 변수(연식, 주행거리)의 아웃라이어를 Fox Recommendation 기준으로 제거한다.
연식/주행거리를 2차식으로 변환하고 스케일링한다.
Ridge, Lasso, Elastic-Net 세 가지 방법으로 정규화 해보았지만, 성능이 나아지지 않았다.
        
> **최종 결과 도출**
> - R-Squared 값 0.851, 정규성 0.130(Omnibus), RMSE 1508 수준
