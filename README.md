Regression Project ; Toyota Corolla Price Prediction
===================

Abstract
-------------

[프로젝트 목표]
 제시된 Toyota사의 Corolla차량의 중고차 가격 데이터(training)를 바탕으로 회귀분석을 통해 새로이 제시되는 중고차 가격(test)을 예측해 보는 것이다.
 
- **training data : 1019 rows, 39 columns**
- **test data : 417 rows, 38 columns(price열 제외)**
 
[프로젝트 평가]
 실제 가격과 예측한 가격의 차이를 **Root-Mean-Squared-Error(RMSE)**를 통하여 채점한다.
-------------

Methods & Process
-------------

> **데이터 탐색 및 분석**
> - 예측해야할 종속 변수 데이터(Price)를 위해 사용되어야 할 독립 변수 데이터들을 탐색하여 실수 값 (정량적) 변수와 카테고리 값 (정성적) 변수로 분리하였다. 이후 이 변수들간의 상관도 분석(상관계수 및 t,F-test 검정)을 통해 연식, 주행거리 등 약 8개의 독립 변수를 선정했다.
