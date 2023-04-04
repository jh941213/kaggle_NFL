# 🏈 Kaggle_NFL  
<img alt="NFL" src ="https://user-images.githubusercontent.com/112835087/227435245-cca96607-2203-4f21-a309-34632eb69cfb.png"/>


# 👥 팀원  
[김재현](http://https://github.com/jh941213) | [이성연](https://github.com/deepshadow25) | [임보라](https://github.com/violet417) | [정유석](https://github.com/dbtjr1103) | [이창재](https://github.com/com0040)
------|------|------|------|------|
Team Member|Team Member|Team Leader|Team Member|Team Member|
<img src="https://user-images.githubusercontent.com/112835087/214769736-c6880568-a4f9-42f7-b5d9-3ef466b6a997.jpeg" width="100" height="100">|<img src="https://user-images.githubusercontent.com/112835087/214769769-f12d45ae-6b09-4567-b142-591c73ccffdb.png" width="100" height="100">|<img src="https://user-images.githubusercontent.com/112835087/227434174-b9458dbd-3819-4947-8533-386baafcdfc1.jpg" width="100" height="100">|<img src ="https://user-images.githubusercontent.com/112835087/227434260-00788b7e-16ec-4d71-b2a5-2fa5fff37e6b.png" width="100" height="100">|<img src="https://user-images.githubusercontent.com/112835087/227434307-5314bcf8-8980-4389-8be8-4ca0b744d395.jpg" width="100" height="100">


# 💾 컴퓨터 환경
비고| AWS Server | Google Colab | Kaggle Notebook |
-----|-------|-------|-------|
GPU | A10G | T4 | P100
RAM |16GB|13~52GB|13GB|
Storage |250GB|166GB|73GB| 

# 목차
- [🏈 대회소개](#-대회소개)
- [📆 수행일정](#-수행일정)
- [📁 데이터 ](#-데이터)
- [📌 대회규칙](#-대회규칙)
- [👫 멀티모달](#-멀티모달)


***

## 🏈 대회소개  
<p align="center">
  <img width="610" alt="스크린샷 2023-03-24 오후 3 05 59" src="https://user-images.githubusercontent.com/112835087/227438232-5538ff70-ca26-4024-a606-679af843c747.png">
 </p>   
 
### NFL 이란?  
 

> 미식축구(National Football League, NFL)는 미국에서 가장 인기 있는 프로페셔널 리그 중 하나
미식축구 경기는 공을 가지고 상대편 골대까지 전진하며 점수를 얻는 것이 목적
총 32개의 팀으로 구성되어 있으며, 미국과 세계 각지에서 매년 매우 인기 있는 경기들을 개최
매년 2월 초에 열리는 NFL의 결승전인 슈퍼볼은 단일 스포츠 이벤트로서는 세계 최대 규모의 흥행을 자랑  

### 1st and Futre - Player Contact Detection by Kaggle
<img width="966" alt="스크린샷 2023-03-24 오후 3 14 38" src="https://user-images.githubusercontent.com/112835087/227440285-519b539a-ba84-4a3c-a303-7bce5ad4e62d.png">  
NFL(The National Football League) & AWS에서 주최한 미식축구 관련 대회  

VIDEO 및 플레이어 Tracking Data를 사용하여 선수 부상 감시 및 완화 프로그램을 만들기 위한 목적   

>1️⃣ 첫번째 대회는 헬멧 충돌 탐지(Impact Detection) - 헬멧 중 어떤 것이 충돌을 일으키고 있는가?   
2️⃣ 두번째 대회는 헬멧 배정(Helmet Assignment) - 충돌하는 헬멧을 쓰고 있는 선수는 누구인가?  
3️⃣ 여기에 이어 열린 3번째 대회 선수 접촉 탐지(Player Contact Detection) - 경기 중에 누가 접촉을 했는가?  
***
## 📌 대회규칙
<img width="600" height = "300" alt="스크린샷 2023-03-24 오후 3 27 30" src="https://user-images.githubusercontent.com/112835087/227442507-26d691d0-e372-4af8-a288-25d01b84b7d4.png">

***


## 📆 수행일정 
<img width="600" img height="300" src="https://user-images.githubusercontent.com/112835087/227437692-0209e5fa-d55c-474c-afb7-296772346876.png">

***

## 📁 데이터  

### 비정형 데이터  
▶️ NFL 영상  
NFL 영상| Train| Test | 
 ------------|------|-------|
갯수 | 720개 | 6개 |  

- 1280x720 해상도  
- 60fps (Frame Per Second)  
- Video 당 약 5~12초 정도의 길이  
> 두 개의 메인 뷰는 Sideline 및 Endzone에서 촬영 → 비디오 쌍은 시간 프레임별로 일치  
 영상 모두 59.94HZ의 프레임 속도 (초당 약 60개의 프레임(정확히는 59.94개)으로 구성)

### 정형 데이터  
📄 CSV 파일  
<img width="550" alt="스크린샷 2023-03-24 오후 3 39 32" src="https://user-images.githubusercontent.com/112835087/227444643-2467b40a-145f-493a-a38e-673c536544a6.png"> 

***

## 👫 멀티모달  

### 💻 머신러닝  
📁 데이터 전처리  
피처엔지니어링, 피처셀렉션, 파생변수 추가, 결측치 채우기, K-Fold CrossValidation   

📚 모델 선정 및 학습  
Pycaret 을 사용하여 모델선정 XGboost, LGBM, RandomForest, Catboost  

📐 하이퍼 파라미터 튜닝  
Optuna frame work 를 사용하여 모델의 최적의 파라미터 값 찾기

🧮 Group K-fold  
'game_play' 영상데이터를 frame 단위로 구분한 시계열 데이터이므로 Group K-fold 교차 검증 수행
___

### 🧘 딥러닝  
📁 데이터 전처리 
1. Video 영상 파일을 이미 파일로 변환 -> 변환 후 이미지 총 372,506 장
- 이미지로 변환후 학습시키는 이유 : 동영상은 3D tensor, 학습에 불필요한 데이터, 효율적인 학습을 위한 동영상 일부 에서 프레임 추출
**2.5D 모델로 학습(연산량을 낮추고, 학습시간을 낮춘다) 시간정보를 반영하였기 때문에 각 픽셀의 공간적 정보를 유지함으로써 양질의 데이터 

📚 모델 선정 및 학습  

📐 하이퍼파라미터 튜닝  





