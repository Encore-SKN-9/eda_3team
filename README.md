# SKN09 - EDA 3Team

> **SK Networks AI CAMP 9기**  
> **개발기간:** 2025.01.15 ~ 2025.01.20  
> **팀명:** 경제 콜럼버스  

---

## 📢 Team Introduction (팀 소개)

### 팀명 : **경제 콜럼버스 (SKN09-eda-3Team)**

#### 팀원 (GitHub Links)
- [김정훈](https://github.com/Zayden0815)
- [김하늘](https://github.com/nini12091)
- [이광운](https://github.com/Leegwangwoon)
- [정윤경](https://github.com/kinoble)

---

## 🎯 Project Introduction (프로젝트 개요)

### 프로젝트명
**글로벌 자산 시장 동향 분석**

### 프로젝트 소개
📈 **주식(S&P 500, KOSPI)**, ₿ **비트코인(BTC)**, 🪙 **금(Gold)**, 💵 **환율(USD)**의 시계열 데이터를 활용하여 **경제적 변수와 자산 가격 간의 관계를 탐구**하고, 각 자산 간 연관성을 **시각화 자료**를 통해 확인합니다.

### 프로젝트 필요성 (배경)
금융 시장은 글로벌 경제와 다양한 자산군의 상호작용에 의해 크게 영향을 받습니다. 주식, 비트코인, 금, 환율과 같은 주요 자산들은 서로 밀접하게 연관되어 있으며, 전통 자산(금, 주식)과 디지털 자산(비트코인)의 상호작용 및 역할 변화를 이해하는 것이 중요합니다.

### ✅ 프로젝트 목표
1. **자산 간 상관관계 분석**  
   주요 자산들의 가격 데이터를 분석하여 **각 자산 간의 상관관계를 관찰**하고, 특정 경제적 사건(예: 코로나) 기간의 반응을 **시각적으로 표현**합니다.

2. **경제적 사건에 대한 관찰**  
   과거 경제적 사건이 자산 가격에 미친 영향을 분석하여 **특정 사건이 자산군에 미치는 패턴과 상관관계를 도출**하고, 이를 통해 **경제적 사건과 자산 간의 관계를 심층적으로 이해**합니다.

---

## 🚀 Getting Started (시작 가이드)

### 주요 사용 라이브러리
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import kagglehub
from sklearn.preprocessing import MinMaxScaler
```

### 설치 및 실행 방법

1. **GitHub에서 리포지토리 클론**
```bash
git clone https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN09-1st-5Team.git
```

2. **필요 라이브러리 설치**
```bash
cd eda_3team
pip install -r requirements.txt
```

3. **주요 분석 파일 실행**  
   주요 분석 결과는 Jupyter Notebook에서 확인 가능합니다.

---

## 📁 Directory Structure (디렉토리 구조)
```
C:.
│  pt_version.ipynb
│  README.md
│  requirements.txt
│
├─Data
│      BTC-2017min.csv
│      BTC-2018min.csv
│      BTC-2019min.csv
│      BTC-2020min.csv
│      BTC-2021min.csv
│      BTC-Daily.csv
│      BTC-Hourly.csv
│      BTC_USD Bitfinex Historical Data.csv
│      BTC_USD.csv
│      Gold Price (2013-2023).csv
│      KOSPI 50 Historical Data.csv
│      snp500.csv
│      USD_KRW Historical Data.csv
│
├─image
│      hitmap.png
│      image.png
│
├─kjh
│      01.BTC_data.ipynb
│      02.USD_KRW.ipynb
│      03.KOSPI.ipynb
│      04.mini_project_zayden.ipynb
│
├─lgw
│      snp_btc.ipynb
│
└─sky
        eda_final.ipynb
```

---

## 📊 Data Description (데이터셋)

| 자산         | 데이터 링크                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------|
| **금**       | [Gold Price (2013-2023)](https://www.kaggle.com/datasets/farzadnekouei/gold-price-10-years-20132023) |
| **비트코인** | [Bitcoin Historical Data](https://www.kaggle.com/datasets/prasoonkottarathil/btcinusd)              |
| **S&P 500**  | [S&P 500 Dataset](https://www.kaggle.com/datasets/yash16jr/snp500-dataset)                          |
| **환율**     | [USD/KRW Historical Data](https://ecos.bok.or.kr/#/StatisticsByTheme/KoreanStat100/K257)            |

---

## 🛠️ Data Preprocessing (데이터 전처리)

1. **Null 값 확인 및 처리**
2. **데이터 타입 변환** (예: `object` → `float`)
3. **Price가 없는 경우**: High, Low의 평균값으로 대체
4. **주식장 휴장일 처리**: Y-M-D 형태로 공통 일자 정리
5. **스케일링**: 가격 변동폭이 심한 자산은 Min-Max Scaling 처리 후 시각화

---

## 📈 Data Analysis (데이터 분석)

#### 5개 주요 항목(S&P 500, KOSPI, 비트코인, 금, 환율)에 대한 가격 변동 (**pt_version.ipynb**)
![5개 항목 차트 (코로나 하이라이트)](./image/image.png)
(그래프 해석 설명 필요)

![5개 항목 히트맵](./image/hitmap.png)
(그래프 해석 설명 필요)

---
#### 5개 주요 항목(S&P 500, KOSPI, 비트코인, 금, 환율)에 대한 가격 변동 (**pt_version.ipynb**)

#### S&P 500, 금(Gold) 변동 분석 (**lgw/snp_btc.ipynb**)

---
#### 비트코인(BTC), 금(Gold) 자산 분석 (**sky/eda_final.ipynb**)
##### 금 가격과 비트코인 변동성 비교 / 경제 위기의 기간 동안의 트랜드 분석
   ![연도별 데이터 분석](https://github.com/user-attachments/assets/30995915-3ca9-41e1-a141-f44d4c60f377)
   ![산점도](https://github.com/user-attachments/assets/b81fc908-d6a2-45ea-bde1-6f4205948173)
   ![가격 비교 그래프](https://github.com/user-attachments/assets/05852f87-5295-4bd8-84b3-9c10568b7571)
   ![각각의 그래프 가격 비교 그래프](https://github.com/user-attachments/assets/b8ecd8b0-7f76-423a-a69c-c8eb95b0867e)
   ![정규화 가격 비교 그래프](https://github.com/user-attachments/assets/87258867-2120-4e70-b955-9858596b7b8a)
   ![1](https://github.com/user-attachments/assets/25248b4c-bb8f-439d-8400-564eab86a4f1)
   ![2](https://github.com/user-attachments/assets/a2affad8-7e8a-4184-b190-959b07af78d2)
   ![3](https://github.com/user-attachments/assets/8e38881d-cd3d-4585-bc75-0ebe87daa5be)
   ![4](https://github.com/user-attachments/assets/05f4463d-6270-481f-a7fc-8f7095f704e8)

---
#### 비트코인(BTC), 환율(USD/KRW), KOSPI 지수 변동 분석
(**kjh/01.BTC_data.ipynb**, **kjh/02.USD_KRW.ipynb**, **kjh/03.KOSPI.ipynb**, **kjh/04.mini_project_zayden.ipynb**)



## 📝 Conclusion (결론)
### EDA를 통해 관찰한 주요 사항
- (작성 필요)

---

## 💬 Team Reflection (한 줄 회고)
- **김정훈**: (작성 필요)
- **김하늘**: (작성 필요)
- **이광운**: 수집 기간과 변동폭이 서로 다른 항목에 스케일링 필요성과 같은 데이터라도 결과를 강조하거나 희석시키는 방식이 가능함을 관찰.
- **정윤경**: (작성 필요)

---
