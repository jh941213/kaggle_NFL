# 🏈 Kaggle_NFL  
## 🥉Kaggle Bronze 획득🎉
- Private Score
![private](https://user-images.githubusercontent.com/112835087/229681560-a245932f-4dba-482f-9a6a-78f29a75f66c.jpg)  
- Public Score
![public](https://user-images.githubusercontent.com/112835087/229681566-aba8ae95-5995-4e33-8124-648623fc24ac.jpg)




# 👥 팀원  
[김재현](http://github.com/jh941213) | [이성연](https://github.com/deepshadow25) | [임보라](https://github.com/violet417) | [정유석](https://github.com/dbtjr1103) | [이창재](https://github.com/com0040)
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
- [👫 수행과정](#-수행과정)
- [🏆 프로젝트평가](#-프로젝트평가)

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

## 👫 수행과정    

### 💻 머신러닝  
### 데이터 전처리  

1️⃣ 데이터 재구성  

train_labels.csv  
<img width="600" alt="스크린샷 2023-04-04 오전 11 42 18" src="https://user-images.githubusercontent.com/112835087/229673053-32ea6135-77e5-4d94-b226-0e4008c0ddd4.png">  

player_tracking.csv  
 <img width="600" alt="스크린샷 2023-04-04 오전 11 43 01" src="https://user-images.githubusercontent.com/112835087/229673144-e632edfd-4a92-4759-8cd2-bfe1686dc441.png">  
 
- 한 선수의 정보만 기록된 기존 정보에서 **두 선수의 정보를 모두 고려 (8 * 2)**
- **'step'을 기준**으로 PLAYER 1과 PLAYER 2의 위치(X, Y 좌표), 이동 속도, 거리, 가속도, 선수 방향, 선수가 바라보는 방향 추가
- 한 팀당 선수는 **11명 / 총 22명의 선수들 사이의 모든 경우의 수 기록**
- **두 선수의 거리, nfl_player_id_1의 그라운드 충돌 여부 추가**  

<img width="600" alt="스크린샷 2023-04-04 오전 11 46 32" src="https://user-images.githubusercontent.com/112835087/229673621-a3229b39-bb19-4e34-bb1f-0d7723b0bdf8.png">

2️⃣ 데이터 필터링  

- **거리 2야드 이하인 Feature만 선택 (2야드 = 약 1.8미터)**
    - 서로 가까운 선수들만 포함하여 **접촉 가능성이 높은 데이터에 집중함**으로써 더 정확한 접촉 감지 모델을 학습
    - **접촉 가능성이 낮은 데이터를 제거**함으로써, 모델이 불필요한 노이즈에 영향을 받지 않고 접촉 감지에 집중
    - 학습 데이터 크기가 줄어들어 **모델 학습 시간이 단축**
<img width="600" alt="스크린샷 2023-04-04 오전 11 48 23" src="https://user-images.githubusercontent.com/112835087/229673928-585c7d88-bea9-4475-89a6-19f5fbdbcf43.png">  

3️⃣ 파생변수 추가  

<img width="600" alt="스크린샷 2023-04-04 오전 11 48 51" src="https://user-images.githubusercontent.com/112835087/229674033-16a31c77-8fc9-439a-99f9-35b1064abc10.png">  

- 헬멧 Bounding Box 정보로 **클러스터링**을 이용하여 데이터 feature 증강
- **데이터 간의 차**를 이용하여 feature 증강
- **데이터 간의 곱**을 이용하여 feature 증강    

4️⃣ 결측치 처리
- 선수가 땅에 부딪힐 경우 결측치를 '0'으로 채움




### 모델 선정 및 학습  

- Pycaret 을 사용하여 모델선정 XGboost, LGBM

<img width="600" alt="스크린샷 2023-04-04 오전 11 39 24" src="https://user-images.githubusercontent.com/112835087/229672708-d4f2fe1f-c6d1-426f-bd64-06108f188a39.png">

### 하이퍼 파라미터 튜닝  

- Optuna frame work 를 사용하여 모델의 최적의 파라미터 값 찾기

<img width="600" alt="스크린샷 2023-04-04 오전 11 40 23" src="https://user-images.githubusercontent.com/112835087/229672808-9b0e303f-4473-44f9-8035-8f16c4af1dc6.png">

### Group K-fold  

- 'game_play' 영상데이터를 frame 단위로 구분한 시계열 데이터이므로 Group K-fold 교차 검증 수행

<img width="600" alt="스크린샷 2023-04-04 오전 11 40 43" src="https://user-images.githubusercontent.com/112835087/229672851-5658d5e4-402b-42f8-ab7c-284d057f4021.png">


___

### 🧘 딥러닝  
### 데이터 전처리  

1. Video 영상 파일을 이미 파일로 변환 -> 변환 후 이미지 총 372,506 장  
**⇒ 2.5D 모델로 학습(연산량을 낮추고, 학습시간을 낮춘다) 시간정보를 반영하였기 때문에 각 픽셀의 공간적 정보를 유지함으로써 양질의 데이터** 

2. Feature Selection
- 거리 2야드 이하인 Feature 만 선택  
- 데이터프레임에 새로운 열 'frame' 추가  
- NFL Video 보다 Tracking Data의 Frame 의 길이가 김  
- 두 Dataset 을 ball snap 이 발생하는 시점에 정보를 활용하여 맵핑  
3. 결측치 처리
- 헬멧 정보를 가져와 PlayerID에 따라 그룹화 → **각 프레임별로 BBox 계산**
- 누락된 프레임의 경우, 데이터의 양방향으로 **선형 보간**
- 주변 정보를 충분히 고려하기 위해 **window 값을 24로 설정 (약 0.4초)**
- 누락된 Frame 정보가 인접한 frame 정보를 바탕으로 적절하게 생성되어 **품질 개선**
4. Image Transform
- 잘라낸 부분 이미지는 다음 단계에서 모델에 input으로 사용  
**⇒ 이미지에서 선수끼리 충돌하는 영역에 집중 가능**
5. Data Transformation
- Geometric Transformations, Color Transformations, Blur, Noise, Crop and Pad, Optical Distortion, Grid Distortion 등 다양한 기법들을 고려해보았으나  
  
- 📊 최종데이터 시각화  
<img width="600" alt="스크린샷 2023-04-04 오전 11 28 05" src="https://user-images.githubusercontent.com/112835087/229671136-43425ae5-c6d9-4d3a-96e5-dd10cf6408ab.png">

### 모델링  
- 멀티모달 
<img width="600" alt="스크린샷 2023-04-04 오전 11 27 50" src="https://user-images.githubusercontent.com/112835087/229671105-7dfd5dc2-253f-4a3a-9b52-cccec7ac66ab.png">

### 앙상블  
- Stacking
<img width="600" src="https://user-images.githubusercontent.com/112835087/229672093-03474eba-91f5-4896-bb75-f7999c36c5ab.png">

- Hard Voting
<img width="600" src="https://user-images.githubusercontent.com/112835087/229672202-f83d79c8-a64b-4137-8524-d869486fd1c6.png">


- Soft Voting
<img width="600" src="https://user-images.githubusercontent.com/112835087/229672216-5be52ddb-4750-4b07-97ee-f3b16b685473.png">

- Attempts
<img width="600" src="https://user-images.githubusercontent.com/112835087/229672216-5be52ddb-4750-4b07-97ee-f3b16b685473.png">

## 🏆 프로젝트평가  

1. 멀티모달을 사용해 봄으로써 데이터를 다룰 수 있는 관점이 확대
2. 3D영상 데이터의 딥러닝 기술과 정형데이터의 머신러닝 기술을 앙상블하여 모델 핸들링에 대한 시각을 넓힘
3. 미식축구에 대한 이해가 부족해서 어려운 대회였지만, 대회를 참여하며 미식축구에 대한 지식을 쌓을 수 있는 좋은 기회
4. Score를 다른 사람들과 비교하며 향상시킬 수 있는 점에서 몰입감 상승
5. 이번 대회를 통해 배운 최신 기술과 경험들을 더욱 발전시켜 앞으로의 프로젝트에 적용 가능
 
</br>

