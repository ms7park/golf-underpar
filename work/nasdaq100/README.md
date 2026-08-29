# 🇺🇸 나스닥 100 (NASDAQ 100) 최근 6개월 고점 대비 폭락주 분석

본 디렉토리는 미국 나스닥 100(NASDAQ 100) 지수 편입 종목들을 대상으로 최근 6개월간의 주가 데이터를 분석하여, **기간 내 최고가 대비 현재가(또는 최신 종가)가 50% 이상 폭락한 종목을 검색 및 필터링**하는 분석 모듈입니다.

---

## 📌 분석 개요

- **대상 지수**: NASDAQ 100 Index (대형 기술주 및 성장주 중심의 상위 100개 종목)
- **분석 주기/기간**: 현재 기준 최근 6개월 (약 126 거래일)
- **핵심 기준**: 
  - 최근 6개월 내 일별 최고가(High) 산출
  - 현재가(Current Close)와 비교하여 **-50% 이상 하락**한 종목 필터링
- **활용 목적**:
  - 단기 어닝 쇼크, 규제 리스크, 시장 조정 등으로 인한 과대 낙폭주 발굴
  - 과매도(Oversold) 구간 진입 여부 및 기술적 반등 모멘텀 평가
  - 밸류에이션(PER/PSR/PBR)과 결합한 저평가 우량주 선별

---

## 📊 세부 분석 지표

| 지표명 | 수식 / 정의 | 의미 |
|---|---|---|
| **6개월 최고가 (High_6M)** | $\max(\text{High}_{t-126 \dots t})$ | 6개월 중 가장 높았던 주가 |
| **현재가 (Current Price)** | $\text{Close}_t$ | 가장 최근 정규장 종가 |
| **고점 대비 낙폭 (%)** | $\frac{\text{Current Price} - \text{High\_6M}}{\text{High\_6M}} \times 100$ | **-50% 이하** 시 스크리닝 대상 |
| **고점 도달일 (Peak Date)** | $\arg\max(\text{High})$ 일자 | 언제부터 하락세가 시작되었는지 파악 |
| **RSI (14일)** | 상대강도지수 (Relative Strength Index) | 30 이하 시 극단적 과매도 상태 |
| **6개월 최저가 대비 반등률** | $\frac{\text{Current Price} - \text{Low\_6M}}{\text{Low\_6M}} \times 100$ | 바닥 확인 후 턴어라운드 진행 여부 |
| **섹터 / 산업군** | GICS Sector & Industry | 섹터 전반의 침체인지 개별 기업 악재인지 구분 |

---

## 🗂️ 디렉토리 및 파일 구성

```plaintext
work/nasdaq100/
├── README.md               # 본 문서 (분석 가이드 및 사양)
├── data/
│   ├── nasdaq100_tickers.json   # 나스닥 100 구성 종목 티커 목록
│   └── raw_prices/              # 티커별 최근 6개월 OHLCV 캐시 데이터
├── scripts/
│   ├── fetch_tickers.py         # 나스닥 100 최신 구성종목 크롤링/수집
│   ├── fetch_data.py            # yfinance 기반 6개월 시세 데이터 다운로드
│   └── analyze_drop.py          # 50% 이상 낙폭 종목 추출 및 기술지표 연산
└── reports/
    └── drop_50pct_summary.md    # 최종 스크리닝 리포트 및 분석 결과
```

---

## 🚀 실행 가이드 (스크립트 구현 시)

1. **필수 라이브러리 설치**:
   ```bash
   pip install yfinance pandas numpy tabulate
   ```

2. **종목 리스트 수집 및 시세 데이터 다운로드**:
   ```bash
   python scripts/fetch_tickers.py
   python scripts/fetch_data.py
   ```

3. **50% 이상 폭락 종목 분석 및 리포트 생성**:
   ```bash
   python scripts/analyze_drop.py --threshold -50
   ```

---

## ⚠️ 분석 시 유의사항
- **액면분할/합병 및 배당**: 수정주가(Adjusted Close / Adjusted High)를 기준으로 계산하여 분할에 따른 왜곡을 방지합니다.
- **지수 리밸런싱**: 나스닥 100 지수 편출입 여부를 주기적으로 갱신해야 합니다.
- **하락 원인 분석 필수**: 단순 가격 하락뿐만 아니라 기업의 재무 상태, 매출 성장률 훼손 여부(Value Trap 주의)를 함께 검토해야 합니다.
