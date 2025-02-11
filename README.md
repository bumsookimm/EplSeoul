# EPL(Eat,Play,Love) Seoul : 서울시 교통관광정보 시스템

공공데이터포털, 서울열린데이터광장 등 **open API로 검증된 데이터를 가공**하고, Google Api, Kakao Api, T-map Api, Naver Api, Chart.js를 활용하여 **시각화된 데이터를 제공**하는 웹 페이지를 제작한 풀스택 프로젝트

#### [프로젝트 목표]

- **☁️ openAPI 활용**: 다양한 데이터 및 DB를 구축해 교통·관광 정보 통합 제공
- **🗂️ 효율적인 데이터 조합**: 데이터 분석 및 재가공으로 맞춤형 데이터 생성
- **📊 데이터 시각화**: 클러스터링 및 차트 시각화를 활용한 사용자 경험(UX) 향상

#### [프로젝트 개요]

- **인원**: 백엔드 5인
- **기간**: 24. 11. 25 - 24. 12. 19. (Total 25일 / Workday 18일)
- **주요 기술 스택**: ```Java```, ```Spring```, ```MySQL```, ```MyBatis```, ```Chart.js```
- **나의 담당 역할**: 버스 정류소

   <br>

### [버스 정류장 주변 시설] 

- **DB 데이터 활용**: 서울 시 버스정류소 위치 DB에 저장 -> 저장된 위치 기반으로 주변 시설 탐색
- **APi 활용**: Google Places API를 활용하여 장소의 이미지, 리뷰 수, 평점을 조회하여 사용자에게 제공,
                Kakao Api를 활용하여 카카오 맵 장소 url을 사용자에게 제공


![Image](https://github.com/user-attachments/assets/5b502a0c-a1f2-4fd4-b839-e98a44511d45)



<br>

### [주변 시설 블로그 검색] 

- **APi 활용**: 네이버 블로그 API에서 블로그 포스트를 검색, 검색어를 URL 인코딩하여 API에 전달하고, JSON 응답을 파싱하여 블로그 포스트 목록 반환


![Image](https://github.com/user-attachments/assets/bfe14014-45a5-44a0-89b1-3268401f9055)

<br>

### [실시간 버스 위치 추적]

- **APi 활용**: 버스 위치 정보 Open API와 연동하여 실시간 버스 정보를 JSON 형식으로 파싱, 버스 정보를 객체로 변환 하여 실시간 버스 위치, 혼잡도, 위치 정보 등을 제공

![Image](https://github.com/user-attachments/assets/bdf6007b-348e-40fc-bf32-91e902f29577)
