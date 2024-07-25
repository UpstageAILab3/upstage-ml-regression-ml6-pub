[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/D1pZhJxu)
# 6팀 다섯남자들

## Team

| ![민경도](https://avatars.githubusercontent.com/u/156163982?v=4) | ![조진우](https://avatars.githubusercontent.com/u/156163982?v=4) | ![이승민](https://avatars.githubusercontent.com/u/156163982?v=4) | ![유정수](https://avatars.githubusercontent.com/u/156163982?v=4) | ![유승호](https://avatars.githubusercontent.com/u/156163982?v=4) |
| :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: | :--------------------------------------------------------------: |
|            [민경도](https://github.com/UpstageAILab)             |            [조진우](https://github.com/UpstageAILab)             |            [이승민](https://github.com/UpstageAILab)             |            [유정수](https://github.com/UpstageAILab)             |            [유승호](https://github.com/UpstageAILab)             |
|                            팀장, 팀의 기본적인 목표 설정 및 협업 리딩, 데이터셋 구축                             |                            데이터셋 구축 , 데이터 정리                             |                             데이터셋 구축 , lgbm 모델링                             |                            데이터셋 구축 , catboost 모델링                             |                            데이터셋 구축 , xgboost 모델링                             |

## 1. Competiton Info

### Overview

- House Price Prediction | 아파트 실거래가 예측

서울시 아파트 실거래가 매매 데이터를 기반으로 아파트 가격을 예측하는 대회<br/>
프로젝트 전체 기간 (2주) : 7월 9일 (화) 10:00 ~ 7월 19일 (금) 19:00<br/>
평가 데이터 개요<br/>
.csv 형태로 제공되며 학습데이터와 같이 예측해야 할 거래금액(target)을 제외하고 51개의 거래 대상이 되는 아파트의 정보에 대한 변수와 거래시점에 대한 변수가 주어집니다.학습 데이터는 1,118,822인 반면, 평가 데이터는 총 9272개이며 대략적인 구조는 아래와 같습니다.<br/> 
학습 데이터의 기간은 2007년 1월 1일부터 2023년 6월 30일까지이고, 평가 데이터는 학습 데이터기간 이후 3개월인 2023년 7월 1일부터 2023년 9월 26일까지의 정보로 구성되어 있습니다.<br/>

### Timeline

- 프로젝트 전체 기간 (2주) : 7월 9일 (화) 10:00 ~ 7월 19일 (금) 19:00

### Evaluation

- 해당 시점의 매매 실거래가를 예측하는 Regression 대회이며, 평가지표는 RMSE(Root Mean Squared Error)를 사용합니다.

## 2. Components

### Directory

- project_root/<br/>
├── notebooks/<br/>
│   └── 결과물 정리.ipynb<br/>
├── docs/<br/>
    └── README.md<br/>
    └── 팀원별 회고.ipynb<br/>
    └── 발표자료.pdf<br/>

    

## 3. Data descrption

### Dataset overview

- 학습 데이터의 기간은 2007년 1월 1일부터 2023년 6월 30일까지이며, 각 변수 명이 한글로 되어있어 어떤 정보를 나타내는 변수인지 쉽게 확인할 수 있습니다.<br/><br/>



시군구 : “서울특별시 강남구 개포동” 과 같이 주소에 대한 정보입니다.<br/>

아파트명 : “개포더샵트리에”와 같이 아파트명에 대한 정보입니다.<br/>

전용면적(㎡) : “108.2017”와 같이 매매대상의 전용면적에 대한 정보입니다.<br/>

건축년도 : “2021”과 같이 아파트의 건축 연도를 나타내는 정보입니다.<br/>

각 변수들은 아래와 같은 결측치 비율을 가지고 있습니다.<br/>

![image](https://github.com/user-attachments/assets/ec3637a7-a41f-4345-9e97-5aba9802e9a1)



### EDA

각 컬럼별 데이터 타입에 따른 시각화<br/>

- 자치구명 
![image](https://github.com/user-attachments/assets/41ea2215-8d65-411b-a0d1-f4f9b1110ea9)

- 법정동명
![image](https://github.com/user-attachments/assets/6aae8958-b2c1-485a-97b2-e42d0d5e22c6)

- 연도
![image](https://github.com/user-attachments/assets/075d5bc1-afc0-4ce1-89fb-78606cc6ccc2)

- 월
![image](https://github.com/user-attachments/assets/6d186900-771a-4727-9471-8b14ef4f61e9)

- 거래유형
![image](https://github.com/user-attachments/assets/359f4365-137c-4563-a2d8-a659182b3753)

- 층
![image](https://github.com/user-attachments/assets/e9fa16bd-c268-4ae7-8d43-6e15d101ad4b)

- 건축년도
![image](https://github.com/user-attachments/assets/e8a9876d-479a-443e-bf77-543a8000520c)

- 아파트의 x 좌표
![image](https://github.com/user-attachments/assets/a701144d-081b-4ec4-9f36-92ddc01e21cc)

- 아파트의 y 좌표
![image](https://github.com/user-attachments/assets/eeddf102-c842-4682-9db9-1bd449bf603e)

- 통화량
![image](https://github.com/user-attachments/assets/e0df80e4-1c68-429d-8416-8e1b14349328)

- KOSPI(1day)
![image](https://github.com/user-attachments/assets/c59f54b0-fd08-48fd-8d00-41e1c0a3a8e0)

- 다우존스(1day)
![image](https://github.com/user-attachments/assets/652ef962-73de-4991-8910-de8be4ddf2a7)

- 한국은행 기준금리
![image](https://github.com/user-attachments/assets/79342102-ede4-4023-ac62-69e7eedebcaa)

- target 
![image](https://github.com/user-attachments/assets/f1414a08-eab0-43a8-b842-4770e6d1fc28)



### Feature engineering

- xgboost 모델에서의 grid search를 통해 최적 feature들을 선정하였습니다.

![image](https://github.com/user-attachments/assets/ecf8a829-722f-43bb-a324-a3c954d76338)


- lgbm 모델에서의 grid search를 통해 최적 feature들을 선정하였습니다.

![image](https://github.com/user-attachments/assets/99e5a228-0518-4c4b-9f9f-256290fe070e)



## 4. Modeling

### Model descrition

- xgboost, catboost
![image](https://github.com/user-attachments/assets/b85ab3b9-9b0b-4aa3-ac4b-492afbd577dd)

![image](https://github.com/user-attachments/assets/2886932b-dabd-42b4-ab7d-f3aa697eda52)


### Modeling Process

1. 경진대회 준비<br/>

데이터 이해 및 탐색 (7월 9일)<br/>
학습 데이터 및 평가 데이터 구조 이해<br/>
데이터 전처리 및 결측치 처리 방법 결정<br/>
변수 간 상관관계 분석<br/>

2. 데이터 전처리 (7월 10일 ~ 7월 11일)<br/>

결측치 처리<br/>
결측치가 있는 변수에 대해 적절한 대체 값 선택<br/>
변수 변환 및 생성<br/>
범주형 변수 인코딩<br/>


3. 모델링 (7월 12일 ~ 7월 15일)<br/>

모델 선택<br/>
다양한 회귀 모델 테스트 (e.g., 선형 회귀, 랜덤 포레스트, XGBoost, LightGBM)<br/>
모델 학습 및 검증<br/>
K-fold 교차 검증을 통한 모델 성능 평가<br/>
하이퍼파라미터 튜닝<br/>

4. 예측 및 제출 (7월 16일 ~ 7월 17일)<br/>

최종 모델 선정 및 학습<br/>
최적의 성능을 보인 모델로 전체 학습 데이터 학습<br/>
평가 데이터 예측<br/>
학습된 모델을 통해 평가 데이터의 아파트 가격 예측<br/>
결과 제출<br/>
예측된 결과를 .csv 파일로 제출<br/>

모델 예측 결과<br/>

모델 세팅 : xgboost<br/>
변수 세팅 : 면적, 위도y, 경도x,  건축년도, 전용면적,세대당 주차대수, 건축연수, 주민등록인구 (명), 세대당 평균 전용면적, 연면적<br/>

![image](https://github.com/user-attachments/assets/19bb0ccb-0b69-452a-b629-a409f80383ca)


모델 세팅 : catboost<br/>
변수 세팅 : 자치구명, 법정동명, 도로명주소, 아파트명, 시도명, 날짜, 통화량M1<br/>

![image](https://github.com/user-attachments/assets/185ad5b1-7fa7-4d3e-a914-eaa50f9bfbae)



숫자형 변수들로 xgboost를 돌렸을때 좋은 성능을 나타내었습니다.

## 5. Result

### Leader Board

![image](https://github.com/user-attachments/assets/7b795da1-2cb0-4045-b772-529264c65419)


데이터 정제에 많은 시간을 투자한 결과, 모델링 및 하이퍼파라미터 최적화에 충분한 시간을 할애하지 못했습니다. 이를 개선하기 위해 다음 프로젝트에서는 데이터 정제와 모델링 시간을 균형 있게 배분하고, 필요에 따라 자동화된 데이터 정제 도구를 활용하여 시간을 절약할 계획입니다. 또한, 모델링 단계에서의 반복적인 실험과 검증을 통해 최적의 성능을 얻도록 하겠습니다.

### Presentation

- [프레젠테이션 파일](https://docs.google.com/presentation/d/1Z8q-_K3HgSlu13Aa1OGtcxa0AaY-PCX5atAKPJMtaj4/edit#slide=id.g2788afeb3d7_0_95)

## etc

### Meeting Log

- [팀 노션](https://sincere-nova-ec6.notion.site/6-aadb7f3e3be54c77a2ff1b93f65a9714)

### Reference

- https://data.seoul.go.kr/


