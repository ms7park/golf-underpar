---
name: stock-drop-analyzer
description: 최근 6개월 주가 데이터를 분석하여 6개월 최고가 대비 50% 이상 폭락한 나스닥 100 및 코스피 200 종목을 스크리닝하고 비교 분석합니다.
---

# 📉 Stock Drop Analyzer Skill

최근 6개월(약 126 거래일) 동안의 수정주가 데이터를 바탕으로, 최고가 대비 50% 이상 폭락한 종목을 검색하고 기술적/기본적 보조지표(RSI, 반등률, 이격도 등)를 비교 분석하는 스킬입니다.

## 🚀 실행 방법

### 1. 통합 비교 분석 실행 (NASDAQ 100 & KOSPI 200)
```bash
.venv/bin/python work/run_comparison.py --threshold -50.0
```

### 2. 나스닥 100 개별 분석 실행
```bash
.venv/bin/python work/nasdaq100/scripts/analyze_nasdaq100.py --threshold -50.0
```

### 3. 코스피 200 개별 분석 실행
```bash
.venv/bin/python work/kospi200/scripts/analyze_kospi200.py --threshold -50.0
```

## 📊 결과 보고서 위치
- **통합 보고서**: `work/reports/market_comparison_summary.md`
- **나스닥 100 보고서**: `work/nasdaq100/reports/drop_50pct_summary.md`
- **코스피 200 보고서**: `work/kospi200/reports/drop_50pct_summary.md`
