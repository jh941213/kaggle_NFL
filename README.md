
# kaggle_nfl Notion link  
https://www.notion.so/jh941213/kaggle_NFL-54fe47ac01a64087a36cfd8d5539e27c?pvs=4
<div align="center">




<img src="https://user-images.githubusercontent.com/103908794/222314882-9fe1ae73-0d39-4816-be45-5ca2f1617b7b.png" width="700" height="150"/>

# :football:

<img src="https://user-images.githubusercontent.com/103908794/222314397-a46d1f5e-45d6-4e16-932a-69e72d1d8fb7.gif" width="500" height="300"/>

</div>
  
  #  <a href="https://www.kaggle.com/competitions/nfl-player-contact-detection/overview"><img src="https://img.shields.io/badge/kaggle-20BEFF?style=plastic&logo=kaggle&logoColor=white"/>    :boom: Player-Contact-Detection :boom: 
  
  Participation period (참여기간) : 23.02.22-23.03.02 
  
  team : UnderDog (임보라 [leader], 이성연, 정유석, 김재현, 이창재) 
 
<div align="center">

# :tada: Bronze :trophy: Medal :tada:

<img src="https://user-images.githubusercontent.com/103908794/222660680-bf7a86a7-b6ab-44a2-a489-c6d5d24eafe4.png" width="700" height="350"/>  

</div>

***

# Table of Contents(목차)

1. Overview(대회 요약)
2. Strategy (전략)
3. Method (방법)

## 1. Overview(대회 요약)

### a. Description

Goal of the Competition

- identify moments with contact to help improve player safety.

- 플레이어의 안전을 개선하는 데 도움이 되는 접촉을 통해 순간을 식별합니다

### b. Evaluation

- Submissions are evaluated on **Matthews Correlation Coefficient** between the predicted and actual contact events.

- (이진분류에 사용되는 **매튜 상관 계수** 를 평가지표로 사용합니다.)

- The file should contain a header and have the following format:
- (제출 파일 형식은 아래와 같습니다.)

<div align="center">

|contact_id|contact|
|---|---|
|58168_003392_0_38590_43854|0|
|58168_003392_0_38590_41257|1|
|58168_003392_0_38590_41944|0|
|...|...|

</div>

### c. Timeline

- December 5, 2022 - Start Date. (대회 시작일)

- February 22, 2023 - Entry Deadline. You must accept the competition rules before this date in order to compete. (참여 마감)

- February 22, 2023 - Team Merger Deadline. This is the last day participants may join or merge teams.(팀 병합 마감)

- March 1, 2023 - Final Submission Deadline. (제출 마감)

### d. Prizes

1st Place - $50,000

2nd Place - $25,000

3rd Place - $13,000

4th Place - $7,000

5th Place - $5,000

### e. Code Requirements

- CPU Notebook <= 9 hours run-time (CPU 런타임 시간제한)
- GPU Notebook <= 9 hours run-time (GPU 런타임 시간제한)
- Internet access disabled (인터넷 엑세스 사용안함)
- Freely & publicly available external data is allowed, including pre-trained models
- (사전 훈련된 모델을 포함하여 자유롭고 공개적으로 사용 가능한 외부 데이터가 허용됩니다.)
- Submission file must be named submission.csv (제출파일명은 submission.csv)

---

## 2. Strategy (전략)

### a. Dataset Description

#### Files

> train (train.mp4 videos of each play.)

> test (test.mp4 videos of each play.)

>> sample_submission.csv (examples of submission)

>> test_baseline_helmets.csv 

>> test_player_tracking.csv

>> test_video_metadata.csv

>> train_baseline_helmets.csv

>> train_labels.csv

>> train_player_tracking.csv

>> train_video_metadata.csv

### b. Direction :sunglasses:

#### :one: Train Custom DL Model
  
#### :two: ML Ansemble Voting

#### :three: Train Custom DL Model + ML Voting

#### :four: :point_right: Pretrained DL Model + ML Ansemble Voting :point_left: (We Choose This)  
---

## 3. Method (방법)
  
### Pretrained DL Model
  
  resnet50

### ML Ansemble Soft-Voting

#### 1. XGBoost - 5, 10 Fold / cluster = [10, 50, 100, 300, 500]
  
#### 2. LightGBM - 5, 10 Fold / cluster = [10, 50, 100, 300, 500]

#### 3. CatBoost - 5, 10 Fold / cluster = [10, 50, 100, 300, 500]

#### 4. RandomForest - 5, 10 Fold / cluster = [10, 50, 100, 300, 500]

#### 5. Stacking(XGBoost, LightGBM, CatBoost) - KFold X / cluster = [10, 50, 100, 500]

### Best Score
  
#### **:thumbsup: CNN + XGBoost(X2) - Ensemble Soft Voting = 0.71187(Privite) / 0.69624(Public)** :thumbsup:
  
