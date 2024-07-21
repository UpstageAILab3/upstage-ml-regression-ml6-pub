[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/D1pZhJxu)
# 6팀 다섯남자들

## Team

| ![민경도](https://avatars.githubusercontent.com/u/156163982?v=4) | ![조진우](https://avatars.githubusercontent.com/u/156163982?v=4) | ![이승민](https://avatars.githubusercontent.com/u/156163982?v=4) | ![유정수](https://avatars.githubusercontent.com/u/156163982?v=4) | ![유승호](https://avatars.githubusercontent.com/u/156163982?v=4) |
| :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: |
|            [민경도](https://github.com/UpstageAILab)             |            [조진우](https://github.com/UpstageAILab)             |            [이승민](https://github.com/UpstageAILab)             |            [유정수](https://github.com/UpstageAILab)             |            [유승호](https://github.com/UpstageAILab)             |
|                            팀장, 팀의 기본적인 목표 설정 및 협업 리딩, 데이터셋 구축                             |                            데이터셋 구축 , 데이터 정리                             |                             데이터셋 구축 , lgbm 모델링                             |                            데이터셋 구축 , catboost 모델링                             |                            데이터셋 구축 , xgboost 모델링                             |

## 1. Competiton Info

(https://stages.ai/_next/image?url=https%3A%2F%2Faistages-api-public-prod.s3.amazonaws.com%2Fapp%2FCompetitions%2F000312%2Fetc%2F%25E1%2584%258B%25E1%2585%25A8%25E1%2584%258E%25E1%2585%25B3%25E1%2586%25A8_%25E1%2584%258B%25E1%2585%25A1%25E1%2584%2591%25E1%2585%25A1%25E1%2584%2590%25E1%2585%25B3_%25E1%2584%2589%25E1%2585%25B5%25E1%2586%25AF%25E1%2584%2580%25E1%2585%25A5%25E1%2584%2585%25E1%2585%25A2%25E1%2584%2580%25E1%2585%25A1_%25E1%2584%258B%25E1%2585%25A8%25E1%2584%258E%25E1%2585%25B3%25E1%2586%25A8-thumbnail.png&w=2048&q=75)

### Overview

- House Price Prediction | 아파트 실거래가 예측

서울시 아파트 실거래가 매매 데이터를 기반으로 아파트 가격을 예측하는 대회
프로젝트 전체 기간 (2주) : 7월 9일 (화) 10:00 ~ 7월 19일 (금) 19:00
평가 데이터 개요
.csv 형태로 제공되며 학습데이터와 같이 예측해야 할 거래금액(target)을 제외하고 51개의 거래 대상이 되는 아파트의 정보에 대한 변수와 거래시점에 대한 변수가 주어집니다.학습 데이터는 1,118,822인 반면, 평가 데이터는 총 9272개이며 대략적인 구조는 아래와 같습니다. 
학습 데이터의 기간은 2007년 1월 1일부터 2023년 6월 30일까지이고, 평가 데이터는 학습 데이터기간 이후 3개월인 2023년 7월 1일부터 2023년 9월 26일까지의 정보로 구성되어 있습니다.

### Timeline

- 프로젝트 전체 기간 (2주) : 7월 9일 (화) 10:00 ~ 7월 19일 (금) 19:00

### Evaluation

- .csv 형태로 제공되며 학습데이터와 같이 예측해야 할 거래금액(target)을 제외하고 51개의 거래 대상이 되는 아파트의 정보에 대한 변수와 거래시점에 대한 변수가 주어집니다.학습 데이터는 1,118,822인 반면, 평가 데이터는 총 9272개 입니다. 학습 데이터의 기간은 2007년 1월 1일부터 2023년 6월 30일까지이고, 평가 데이터는 학습 데이터기간 이후 3개월인 2023년 7월 1일부터 2023년 9월 26일까지의 정보로 구성되어 있습니다.

## 2. Components

### Directory

- project_root/
├── notebooks/
│   └── 결과물 정리.ipynb
├── docs/
    └── README.md
    └── 팀원별 회고.ipynb
    └── 발표자료.pdf

    

## 3. Data descrption

### Dataset overview

- 학습 데이터의 기간은 2007년 1월 1일부터 2023년 6월 30일까지이며, 각 변수 명이 한글로 되어있어 어떤 정보를 나타내는 변수인지 쉽게 확인할 수 있습니다.



시군구 : “서울특별시 강남구 개포동” 과 같이 주소에 대한 정보입니다.

아파트명 : “개포더샵트리에”와 같이 아파트명에 대한 정보입니다.

전용면적(㎡) : “108.2017”와 같이 매매대상의 전용면적에 대한 정보입니다.

건축년도 : “2021”과 같이 아파트의 건축 연도를 나타내는 정보입니다.

각 변수들은 아래와 같은 결측치 비율을 가지고 있습니다.

- (images/EDA.png)


### EDA

- 각 컬럼별 데이터 타입에 따른 시각화

- (images/newplot.png)
- (images/newplot (1).png)
- (images/newplot (2).png)
- (images/newplot (3).png)
- (images/newplot (4).png)
- (images/newplot (5).png)
- (images/newplot (6).png)
- (images/newplot (7).png)
- (images/newplot (8).png)
- (images/newplot (9).png)
- (images/newplot (10).png)
- (images/newplot (11).png)
- (images/newplot (12).png)
- (images/newplot (13).png)
- (images/newplot (14).png)
- (images/newplot (15).png)
- (images/newplot (16).png)
- (images/newplot (17).png)
- (images/newplot (18).png)
- (images/newplot (19).png)
- (images/newplot (20).png)
- (images/newplot (21).png)
- (images/newplot (22).png)
- (images/newplot (23).png)
- (images/newplot (24).png)
- (images/newplot (25).png)
- (images/newplot (26).png)

### Feature engineering

- xgboost 모델에서의 grid search를 통해 최적 feature들을 선정하였습니다.
- lgbm 모델에서의 grid search를 통해 최적 feature들을 선정하였습니다.

- (images/featureselction_xgboost.png)
- (images/featureselction_lgbm.png)
- (images/featureselction_lgbm2.png)

## 4. Modeling

### Model descrition

- xgboost, catboost 
- (images/modeldescription.png)

### Modeling Process

1. 경진대회 준비

데이터 이해 및 탐색 (7월 9일)
학습 데이터 및 평가 데이터 구조 이해
데이터 전처리 및 결측치 처리 방법 결정
변수 간 상관관계 분석
2. 데이터 전처리 (7월 10일 ~ 7월 11일)

결측치 처리
결측치가 있는 변수에 대해 적절한 대체 값 선택
변수 변환 및 생성
범주형 변수 인코딩


3. 모델링 (7월 12일 ~ 7월 15일)

모델 선택
다양한 회귀 모델 테스트 (e.g., 선형 회귀, 랜덤 포레스트, XGBoost, LightGBM)
모델 학습 및 검증
K-fold 교차 검증을 통한 모델 성능 평가
하이퍼파라미터 튜닝

4. 예측 및 제출 (7월 16일 ~ 7월 17일)

최종 모델 선정 및 학습
최적의 성능을 보인 모델로 전체 학습 데이터 학습
평가 데이터 예측
학습된 모델을 통해 평가 데이터의 아파트 가격 예측
결과 제출
예측된 결과를 .csv 파일로 제출

모델 예측 결과

모델 세팅 : xgboost
변수 세팅 : 면적, 위도y, 경도x,  건축년도, 전용면적,세대당 주차대수, 건축연수, 주민등록인구 (명), 세대당 평균 전용면적, 연면적

- (images/숫자형-xgboost.png)

모델 세팅 : catboost
변수 세팅 : 자치구명, 법정동명, 도로명주소, 아파트명, 시도명, 날짜, 통화량M1

- (images/범주형-catboost.png)


숫자형 변수들로 xgboost를 돌렸을때 좋은 성능을 나타내었습니다.

## 5. Result

### Leader Board

- (images/Leader Board Capture.png)

데이터 정제에 많은 시간을 투자한 결과, 모델링 및 하이퍼파라미터 최적화에 충분한 시간을 할애하지 못했습니다. 이를 개선하기 위해 다음 프로젝트에서는 데이터 정제와 모델링 시간을 균형 있게 배분하고, 필요에 따라 자동화된 데이터 정제 도구를 활용하여 시간을 절약할 계획입니다. 또한, 모델링 단계에서의 반복적인 실험과 검증을 통해 최적의 성능을 얻도록 하겠습니다.

### Presentation

- _Insert your presentaion file(pdf) link_

## etc

### Meeting Log

- [팀 노션](https://sincere-nova-ec6.notion.site/6-aadb7f3e3be54c77a2ff1b93f65a9714)

### Reference

- https://data.seoul.go.kr/


