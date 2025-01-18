# SKN09-eda-3Team

> **SK Networks AI CAMP 9기** <br/> **개발기간: 2025.01.15 ~ 2025.01.20** <br/> **팀명: 경제 콜럼버스** 


<br>
</br>  

# Introduction Team (팀 소개)
###  팀명 : 경제 콜럼버스 SKN09-eda-3Team

#### 팀원 (github link)
-  [김정훈](https://github.com/Zayden0815)
-  [김하늘](https://github.com/nini12091)
-  [이광운](https://github.com/Leegwangwoon)
-  [정윤경](https://github.com/kinoble)

<br>
</br>  

# Introduction Project (프로젝트 개요)

### 프로젝트 명
글로벌 자산 시장의 동향 분석

### 프로젝트 소개
주식(s&P500,KOSPI), 비트코인(BTC), 금, 환율(USD)의 가격 데이터를 이용하여 어떤 움직임으로 반응하고 서로 연관성이 있는지 시각화 자료를 통해 확인한다.

### 프로젝트 필요성(배경) 
금융 시장은 글로벌 경제와 다양한 자산군의 상호작용에 의해 크게 영향을 받음. 주식, 비트코인, 금, 환율과 같은 주요 자산들은 서로 밀접하게 연관되어 있으며, 특정 사건이나 경제적 변동에 대해 어떻게 반응하는지를 이해하는 것은 투자자, 경제학자 및 정책 입안자들에게 중요함.

### ✅프로젝트 목표

 1. **자산 간 상관관계 분석**  
   주식 시장(S&P 500, KOSPI), 비트코인, 금, 환율 등 주요 자산들의 가격 데이터를 분석하여, 각 자산 간의 상관관계를 관찰하고, 특정 경제적 사건(예: 코로나) 기간의 반응을 시각적으로 표현합니다.

 2. **경제적 사건에 대한 관찰**  
   과거의 경제적 사건이 자산 가격에 미친 영향을 분석하여, 비슷한 사건이 발생할 경우 어떤 반응을 예상할 수 있는지 예측합니다.

<br>
</br>

# 시작 가이드

## 사용 라이브러리
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import kagglehub
import matplotlib.font_manager as fm
import matplotlib
import seaborn as sns
from sklearn.preprocessing import MinMaxScaler
```
## 설치/사용 방법

###  GitHub에서 리포지토리 클론

```bash
git clone https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN09-1st-5Team.git
```

### 라이브러리 설치
```bssh
cd eda_3team
pip install -r requirements.txt
```


## 실행 코드

- **pt_version.ipynb**  
  5개 주요 항목(S&P 500, KOSPI, 비트코인, 금, 환율)에 대한 가격 변동을 시각적으로 그래프화한 최종 합쳐진 파일입니다.

- **01.BTC_data.ipynb**  
  비트코인(BTC)의 가격 변동에 대한 분석 파일입니다.

- **02.USD_KRW.ipynb**  
  환율(USD/KRW)의 변동을 분석한 파일입니다.

- **03.KOSPI.ipynb**  
  KOSPI 지수의 변동을 분석한 파일입니다.

- **04.mini_project_zayden.ipynb**  
  비트코인, KOSPI, 환율 3가지 자산의 가격 변동을 합쳐서 분석한 파일입니다.

- **eda_final.ipynb**  
  (이 파일은 현재 프로젝트에 사용되지 않습니다. 무시해 주세요.)

- **sky_eda.ipynb**  
  비트코인과 금 2개의 자산 가격 변동에 대한 분석 파일입니다.

- **snp_btc.ipynb**  
  S&P 500과 금 2개의 자산 가격 변동에 대한 분석 파일입니다.

<br>
</br>


# 차트 이미지
![5개 항목 차트(코로나 하이라이트)](./image/image.png)

# 히트맵 이미지
![5개 항목 히트맵](./image/hitmap.png)




# 디렉토리 구조
```
├── 01.BTC_data.ipynb
├── 02.USD_KRW.ipynb
├── 03.KOSPI.ipynb
├── 04.mini_project_zayden.ipynb
├── eda_final.ipynb
├── pt_version.ipynb
├── README.md
├── requirements.txt
├── sky_eda.ipynb
├── snp_btc.ipynb
│
├── Data
│   ├── BTC-2017min.csv
│   ├── BTC-2018min.csv
│   ├── BTC-2019min.csv
│   ├── BTC-2020min.csv
│   ├── BTC-2021min.csv
│   ├── BTC-Daily.csv
│   ├── BTC-Hourly.csv
│   ├── BTC_USD Bitfinex Historical Data.csv
│   ├── BTC_USD.csv
│   ├── Gold Price (2013-2023).csv
│   ├── KOSPI 50 Historical Data.csv
│   ├── snp500.csv
│   └── USD_KRW Historical Data.csv
│
└── image
    └── image.png
```

# 한 줄 회고
<b>김정훈</b>\

<b>김하늘</b>\

<b>이광운</b>\ 수집 기간과 변동폭이 서로 다른 항목에 스케일링 필요성과 같은 데이터라도 결과를 강조 or 희석 시켜 보이게 할 수 있음을 관찰했다. 

<b>정윤경</b>\
