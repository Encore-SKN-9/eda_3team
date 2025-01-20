# SKN09 - EDA 3Team

> **SK Networks AI CAMP 9기**  
> **개발기간:** 2025.01.15 ~ 2025.01.20  
> **팀명:** 경제 콜럼버스  

---

## 📢 Team Introduction (팀 소개)
| 이름      | GitHub ID                          |
|-----------|------------------------------------|
| 🧑‍💻 김정훈  | [@Zayden0815](https://github.com/Zayden0815) |
| 👩‍💻 김하늘  | [@nini12091](https://github.com/nini12091)        |
| 👩‍💻 이광운  | [@Leegwangwoon](https://github.com/Leegwangwoon)          |
| 👨‍💻 정윤경  | [@kinoble](https://github.com/kinoble) |

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

#### 비트코인(BTC), 환율(USD/KRW), KOSPI 지수 변동 분석
(**kjh/01.BTC_data.ipynb**, **kjh/02.USD_KRW.ipynb**, **kjh/03.KOSPI.ipynb**, **kjh/04.mini_project_zayden.ipynb**)
   ![4-1](https://github.com/user-attachments/assets/a4d9842d-ec5f-4c3e-ad55-ee917f59eca3)
##### - 2021년 말, 비트코인 가격이 급등하며 60,000 USD 이상으로 확인, 2022년에 조정을 겪은 뒤, 2023년 말부터 다시 상승세를 보임
   ![4-2](https://github.com/user-attachments/assets/dc836dbc-65bd-47c0-a3b8-e04d70ca5a7c)
##### - 2022년 이후 원화 약세로 인해 환율이 크게 상승하는 것을 확인
   ![4-3](https://github.com/user-attachments/assets/f3ee91d8-5cd8-4128-a481-188933162a77)
##### - 2020년 COVID-19 팬데믹 이후 저점에서 빠르게 반등하고, 2021년 말에 최고치를 기록한 후 2022년 하락세를 보이며 변동성이 증가
   ![4-4](https://github.com/user-attachments/assets/a2e8a51d-d2d6-4f36-8abd-761608cc9d9a)
##### - 2021년 말, 비트코인 가격이 급등하며 60,000 USD 이상으로 확인, 2022년에 조정을 겪은 뒤, 2023년 말부터 다시 상승세를 보임
   ![4-5](https://github.com/user-attachments/assets/9cbb4a08-b16d-44e5-9c8a-368d96415185)
   ![4-6](https://github.com/user-attachments/assets/a0b58a3a-e0fc-4132-8a13-e26d66e2806e)
   ![4-7](https://github.com/user-attachments/assets/810d635b-cb90-4f7d-a1ac-04fd0bf0671f)
   ![4-8](https://github.com/user-attachments/assets/83065d9f-c5c6-4b35-8156-2b046aab4dfa)
##### - USD/KRW, BTC, KOSPI 모두 2020년대 초반에 큰 변동성을 보였고, 특히, BTC는 2021년에 사상 최고치를 기록했으며, USD/KRW는 2022년 이후 상장되었음. 

---
#### 비트코인(BTC), 금(Gold) 자산 분석 (**sky/eda_final.ipynb**)
##### 금 가격과 비트코인 변동성 비교 / 경제 위기의 기간 동안의 트랜드 분석
   ![연도별 데이터 분석](https://github.com/user-attachments/assets/30995915-3ca9-41e1-a141-f44d4c60f377)
##### - 금 가격은 2020년 이후 경제 불확실성과 안전 자산 선호로 인해 평균적으로 1800달러로 상승 / 비트코인은 2021년 급격한 투자 수요로 증가로 최소/최대 가격 범위가 크게 확대 
###### (출처 : https://www.mk.co.kr/news/economy/9473688) 
###### (출처 : https://www.chosun.com/economy/weeklybiz/2021/01/11/S3XU4EPJXVHZ7INIE3533I2HOM/)

   ![산점도](https://github.com/user-attachments/assets/b81fc908-d6a2-45ea-bde1-6f4205948173)
##### - X 값 변화에 Y값 영향을 주지 않는 것으로 보아 금 가격과 비트코인 가격 간에는 뚜렷한 상관 관계가 보이지 않음
   
   ![가격 비교 그래프](https://github.com/user-attachments/assets/05852f87-5295-4bd8-84b3-9c10568b7571)
   ![각각의 그래프 가격 비교 그래프](https://github.com/user-attachments/assets/b8ecd8b0-7f76-423a-a69c-c8eb95b0867e)
   ![정규화 가격 비교 그래프](https://github.com/user-attachments/assets/87258867-2120-4e70-b955-9858596b7b8a)
##### - 2015년부터 2022년까지 금 가격은 전반적으로 완만한 상승세를 보였으며, 2020년 이후 팬데믹과 경제 불확실성 증가로 인해 더 뚜렷하게 상승 / 비트코인은 2017년 처음 급격한 가격 상승을 보였으며, 이후 큰 변동성을 동반한 상승과 하락을 반복

   ![1](https://github.com/user-attachments/assets/25248b4c-bb8f-439d-8400-564eab86a4f1)
##### - 금은 2020년과 2021년에 걸쳐 평균 가격이 월별로 크게 변화하며, 특히 3월과 8월의 가격 변동이 크게 보이고 연말(11월~12월)로 갈수록 금 가격이 안정되는 경향이 나타남 / 2021년은 월별로 큰 변화가 나타나는 해로, 1월과 4월에 특히 강한 상승세를 보이다가 이후 하락세가 나타남. 

   ![2](https://github.com/user-attachments/assets/a2affad8-7e8a-4184-b190-959b07af78d2) 
   ![3](https://github.com/user-attachments/assets/8e38881d-cd3d-4585-bc75-0ebe87daa5be)
   ![4](https://github.com/user-attachments/assets/05f4463d-6270-481f-a7fc-8f7095f704e8)
##### - 경제 위기 시기(회색 영역) 동안 금 가격은 안정적인 상승세를 보였고, 코로나 팬데믹 초기(2020년 초)에는 금과 비슷하게 약간의 조정을 보였지만, 이후 급격한 상승세를 보이며 최고치를 기록

---

#### 5개 주요 항목(S&P 500, KOSPI, 비트코인, 금, 환율)에 대한 가격 변동 (**pt_version.ipynb**)
![r1](https://github.com/user-attachments/assets/c7ad94aa-afd5-4548-b77d-22200be8ae81)
![5개 항목 차트 (코로나 하이라이트)](./image/image.png)
![5개 항목 히트맵](./image/hitmap.png)
#### S&P 500, 비트코인(BTC) 변동 분석 (**lgw/snp_btc.ipynb**)
![r2](https://github.com/user-attachments/assets/4d96fe54-7e87-4341-8953-743074e90cc0)
##### - 전체적으로 비슷한 우상향 그래프를 보이나, USD/KRW(환율)은 나머지 항복과 반대 움직임 보임을 관찰 할 수 있음. 코로나 기간 가격상승은 금(Gold) 이 가장 높은 상승을 보임

---

## 📝 Conclusion (결론)
### 1. 자산 간 상관관계 분석 결과
   전통 자산(금, 주식)과 디지털 자산(비트코인)의 상관관계는 제한적으로 나타났으며, 서로 다른 역할을 수행함을 확인했습니다.
   
   - **금(Gold)**: 안전 자산으로서 경제적 불확실성 시기에 상승하는 경향이 뚜렷했습니다.
   
   - **비트코인(BTC)**: 높은 변동성을 보이며 투자 심리와 경제의 영향을 가장 크게 받는 자산으로 나타났습니다.
   
   - **환율(USD/KRW)**: 글로벌 경제와 원화 약세를 반영하며 주식 및 비트코인과 반대 방향으로 움직이는 특징을 보였습니다.

### 2.  경제적 사건 관찰 결과
   코로나 팬데믹은 모든 자산군에 강력한 영향을 미쳤습니다.
   
   금은 팬데믹 초기 안전 자산으로서 급등하며, 불확실성 증가에 따른 투자 선호도가 높았고, 주식(S&P 500, KOSPI)은 초기 하락 후 경기 부양책 및 회복세에 힘입어 강한 반등을 보였습니다.
   비트코인은 팬데믹 이후 디지털 자산에 대한 관심 증가와 투자 확대의 결과로 사상 최고치를 기록하였습니다.

---

## 💬 Team Reflection (한 줄 회고)
- **김정훈**: numpy와 pandas를 활용하여, 원하는 형식으로 데이터를 정제하고 청중에게 이해를 도울 수 있게 matplolib으로 다양한 방식으로 데이터에 맞게 시각화할 수 있다는 것을 알게되었습니다. 
- **김하늘**: info, description 함수를 통해 데이터 기초 통계와 타입을 확인하는 작업을 실제 프로젝트에서 적용시켜 보는 과정에서, 각 컬럼마다 알맞는 타입으로 (ex.object -> float) 변경시켜주면서 데이터 null 정제를 쉽게 할 수 있었습니다.
- **이광운**: 수집 기간과 변동폭이 서로 다른 항목에 스케일링 필요성과 같은 데이터라도 결과를 강조하거나 희석시키는 방식이 가능함을 관찰.
- **정윤경**: (작성 필요)

---
