# EPL(Eat,Play,Love) Seoul : 서울시 교통관광정보 시스템

공공데이터포털, 서울열린데이터광장 등 **open API로 검증된 데이터를 가공**하고, Google Api, Kakao Api, T-map Api, Naver Api, Open API, Chart.js를 활용하여 **시각화된 데이터를 제공**하는 웹 페이지를 제작한 풀스택 프로젝트

#### [프로젝트 목표]

- **☁️ openAPI 활용**: 다양한 데이터 및 DB를 구축해 교통·관광 정보 통합 제공
- **🗂️ 효율적인 데이터 조합**: 데이터 분석 및 재가공으로 맞춤형 데이터 생성
- **📊 데이터 시각화**: 클러스터링 및 차트 시각화를 활용한 사용자 경험(UX) 향상

#### [프로젝트 개요]

- **인원**: 백엔드 5인
- **기간**: 24. 11. 25 - 24. 12. 19. (Total 25일 / Workday 18일)
- **주요 기술 스택**: ```Java```, ```Spring```, ```Jsp```, ```MariaDB```, ```JUnit 5```, ```Jpa```, ```Chart.js```
- **나의 담당 역할**: 버스 정류소

<br>

## 개선 내용(진행 예정)

> URL을 통해 서버의 동작(runBatch)을 트리거하는 구조를 구현하여 REST API를 설계했다고 하지만, REST 원칙을 엄격히 준수했다고 하기에는 아직 한참 부족하다. REST원칙을 더 공부해서, 이를 준수한 RESTful API 형식으로 수정해보고 싶다.

<br>

## 담당 기능별 핵심 내용 [🔍Presentation : Check more Details](https://docs.google.com/presentation/d/1I4oSCDEbJj2i-Sc2cHZ9rFU1D0vD3rE64fTLxj3CJRU/edit?usp=sharing)

*시연영상과 더불어 기능에 초점을 맞춘 내용을 담고 있습니다.*

*더 자세한 로직에 대한 설명 및 코드에 대한 내용은 ☝️Presentation을 확인해 주시기 바랍니다.*

<br>

### [API연결 및 파일 데이터 저장] ```_workday 7(단위 테스트 포함)```

- **단일 Service로 다양한 API 데이터 호출**: RESTful API 구조를 분석하여, 공통 서비스 로직에 파라미터를 활용해 데이터를 동적으로 호출
- **Spring Batch로 ETL 프로세스 구현**: Batch 실행 트리거를 REST API 형식으로 구현하고, url 경로 파라미터 값에 따라 로직 분기 처리
- **JUnit 단위 테스트로 로직 검증**: Mocking된 객체를 활용하여 메서드 호출 동작과 예외 상황에 따른 반환값을 검증

<br>

### [실시간 대여 정보 지도 마킹] ```_workday 4```

- **DB데이터로 옵션 생성**: 행정구역/역사 옵션 선택값에 따른 중심 좌표 변경
- **전체 데이터 배열 리스트 반환**: JSON 문자열의 전체 데이터 배열을 반환하고, 클라이언트(JS)에서 데이터를 가공·처리
- **조건별 캐싱 적용**: 응답 속도 691.73ms → 6.29ms로 대폭적인 성능 개선(약 110배 빨라짐)

![실시간](https://github.com/user-attachments/assets/62698d79-be2b-4ef9-8821-586a36a6a14c)

<br>

### [월별 통계 클러스터링] ```_workday 2```

- **기간 옵션 다중 선택 가능**: 기간 선택값에 따른 데이터 호출 및 합계 계산, 행정구 생성
- **데이터 조합**: 유사 API 데이터와 조합하여 좌표값 매칭

![월별](https://github.com/user-attachments/assets/46ac2905-1788-42a7-8904-96bb64eb8760)

<br>

### [연도별 사고 통계 차트] ```_workday 2```

- **데이터 기반 동적 필터링 옵션**: 화면이 로드되면 전체 데이터를 서버로 부터 반환받아, 클라이어트 측에서 필터링 및 가공 처리
- **차트 동적 생성 및 업데이트**: 세부 항목의 합산값을 담은 데이터셋 생성해 시각적 데이터 표현

![연도별](https://github.com/user-attachments/assets/960b488b-26c5-492e-afba-257ad883f364)
