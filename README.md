# 시시콜콜 서비스

모바일 화면을 기준으로 만든 정적 웹 서비스입니다. 별도 서버나 빌드 과정 없이 HTML 파일을 브라우저에서 열어 사용할 수 있습니다.

## 주요 화면

- `index.html`: 서비스 시작 화면
- `life.html`: SiSiColCol 라이프
- `calculator.html`: SiSiColCol 계산기
- `calendar.html`: SiSiColCol 캘린더
- `memo.html`: SiSiColCol 메모장
- `dashboard.html`: 이전 대시보드 파일

## 기능

### 시작 화면

`index.html`에서 각 서비스로 이동합니다.

- SiSiColCol 라이프
- SiSiColCol 계산기
- SiSiColCol 캘린더
- SiSiColCol 메모장
- 추후 추가

오른쪽 상단 설정 버튼에서 API 키와 기본 위치를 저장할 수 있습니다.

### SiSiColCol 라이프

현재 위치 기반 생활 정보 대시보드입니다.

- 현재 날씨
- 오전/오후 날씨 요약
- 내일/모레 예보
- 대기질과 생활 지수
- 주변 교통/시설 지도 링크
- 최근 지진 정보

사용 API:

- Open-Meteo Forecast API
- Open-Meteo Air Quality API
- BigDataCloud Reverse Geocoding
- USGS Earthquake API

### SiSiColCol 계산기

탭과 좌우 스와이프로 전환되는 계산기 화면입니다.

- 일반 계산기
- 단위 계산기: 길이, 무게, 온도
- 날짜 계산기: 날짜 차이, 날짜 더하기

### SiSiColCol 캘린더

월간 달력과 날짜별 메모 기능을 제공합니다.

- 이전 달 / 다음 달 / 오늘 이동
- 날짜 선택
- 날짜별 메모 작성
- 메모 저장 및 삭제
- 메모가 있는 날짜 표시

### SiSiColCol 메모장

LocalStorage 기반 메모장입니다.

- 메모 제목 입력
- 메모 내용 입력
- 저장
- 새 메모 작성
- 저장 내역 불러오기
- 현재 메모 삭제

## LocalStorage 저장 정보

브라우저 LocalStorage에 아래 키로 데이터가 저장됩니다.

- `sisicolcol.settings`: 설정 화면의 API 키와 기본 위치
- `sisicolcol.calendar.memos`: 캘린더 날짜별 메모
- `sisicolcol.memo.items`: 메모장 저장 내역

설정 화면에서 LocalStorage 데이터를 JSON 파일로 백업하거나, 백업 파일을 업로드해 복원할 수 있습니다.

## 실행 방법

프로젝트 폴더에서 `index.html`을 브라우저로 열면 됩니다.

```text
index.html
```

위치 기반 기능을 사용하려면 브라우저의 위치 권한을 허용해야 합니다.

## 파일 구조

```text
sisicolcol/
  README.md
  index.html
  life.html
  calculator.html
  calendar.html
  memo.html
  dashboard.html
```

## 참고

- 모든 화면은 모바일 사용을 우선으로 디자인되어 있습니다.
- 데이터는 서버가 아닌 현재 브라우저에 저장됩니다.
- 브라우저를 바꾸거나 LocalStorage를 삭제하면 저장된 설정과 메모가 사라질 수 있습니다.
