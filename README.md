# 🚇 서울시 지하철 승하차 데이터 분석

## 프로젝트 개요
### 목표
서울시 지하철 승하차 데이터를 활용하여 데이터 전처리 및 Google Maps API 연동을 통해 각 역의 승하차 현황을 `folium`으로 시각화하는 데이터 분석 파이프라인을 구축합니다.

### 해결하고자 하는 문제
- 서울시 지하철의 혼잡도를 효과적으로 분석하여 시민과 정책 입안자가 보다 나은 교통 정책을 수립할 수 있도록 지원합니다.
- 특정 시간대 및 지역의 지하철 이용 현황을 시각적으로 직관적으로 분석합니다.

### 주요 기능
- 서울 열린 데이터 광장에서 제공하는 데이터를 활용하여 승하차 현황을 분석
- `pandas`를 이용한 데이터 전처리 및 가공
- `Google Maps API`를 활용한 위치 데이터 매핑
- `folium`을 활용한 지하철 역 위치 및 승하차 데이터 시각화
- 시간대별, 역별 지하철 이용 패턴 분석

---

## 프로젝트 구조

```bash
subway_data_analysis
├── README.md               # 프로젝트 소개 및 실행 방법
├── subway_data.ipynb       # 지하철 데이터 전처리 및 기본 분석
├── subway_map.ipynb       # 지하철 위치 데이터 및 지도 시각화
├── subway_time_data.ipynb # 시간대별 지하철 이용 패턴 분석
```

### 주요 코드 파일 설명
- **`subway_data.ipynb`**: 서울 열린 데이터 광장에서 가져온 데이터를 정제하고 전처리하는 코드가 포함되어 있습니다.
- **`subway_map.ipynb`**: `Google Maps API` 및 `folium`을 활용하여 지하철 역별 승하차 현황을 지도에 시각화하는 코드가 포함되어 있습니다.
- **`subway_time_data.ipynb`**: 시간대별 지하철 이용 패턴을 분석하여 특정 시간대의 혼잡도를 파악하는 코드가 포함되어 있습니다.

---

## 설치 및 실행 방법

### 1️⃣ 환경 설정
본 프로젝트는 Python 3.8 이상에서 실행할 수 있습니다. 먼저, 프로젝트 디렉토리를 클론합니다.

```bash
git clone https://github.com/your-repo/subway_data_analysis.git
cd subway_data_analysis
```

### 2️⃣ 가상환경 생성 (선택사항)

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate    # Windows
```

### 3️⃣ 필수 패키지 설치

```bash
pip install -r requirements.txt
```

`requirements.txt`가 없는 경우, 주요 패키지를 수동으로 설치할 수도 있습니다.

```bash
pip install pandas numpy matplotlib folium googlemaps
```

### 4️⃣ API 키 설정 (Google Maps API 사용 시 필수)
Google Maps API를 활용하려면, API 키를 발급받고 `.env` 파일을 생성하여 설정합니다.

```bash
echo "GOOGLE_MAPS_API_KEY=your_api_key_here" > .env
```

또는 `subway_map.ipynb` 파일 내부에서 API 키를 직접 입력할 수도 있습니다.

### 5️⃣ Jupyter Notebook 실행

```bash
jupyter notebook
```

노트북 실행 후 `subway_data.ipynb`부터 순서대로 실행하여 데이터를 분석하고 시각화를 진행할 수 있습니다.

---

## 참고자료
- [서울 열린 데이터 광장](https://data.seoul.go.kr/)
- [Google Maps API](https://developers.google.com/maps)
- [Folium 공식 문서](https://python-visualization.github.io/folium/)

---
