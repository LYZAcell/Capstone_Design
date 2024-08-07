# Capstone_Design

## Machine learning 위주의 학습

### 코드 구현 ( 0314~ 0330)
- 텍스트 크롤링 업로드 예정
  - 구현해봤으나 누락이 심해 SiY님코드 활용. 
- 이미지 크롤링 코드업로드 완료
  - SuY님이 주신 자동 클릭코드 (webdriver, 자동 클릭 코드) 바탕으로 html에서 태그 뽑아서 크롤링하기
- 월말까지 csv 모으기 성공. 약 7천건의 데이터

### 평가모델 및 이미지 텍스트 추출(0401~16)
- rouge 평가모델 관련 노션 작성 겸 실습 코드 업로드(0403)
- csv파일 생성 및 합치기 공부
  - append하는게 이상적이지만 힘들어 pandas로 컬럼명만 지정하고 이어 추가하는 방법
  - encoding 오류, 병합 오류 해결 (0408)
  - 학사 파일 병합 및 데이터 append(0410)
  - 학사 데이터 개선 완료 (셀병합 및 표 정정, 불용어 처리 등  _0411)
  - 공지 데이터 병합 중( 0412~0414)
  - 데이터 추출완료 !!! (0416)
  - 학사 인덱스 누락사항 정정 및 다시 날짜 sorting(0420)
 
### 전처리 (0416~~0503)
- 불용어 찾기 (0416~
- randomforest 스터디(0417~
  - 클론코딩 및 konlpy  관련 사항 확인
- 벡터화 연산 라이브러리 수정 및 오류명 확인 (0522)

### 중간 시연 완료. 분기점 (0523)
- colab으로 re패키지 통해 전처리중 
  - 현재 전번, 메일, 학교메일, 사이트 등 기본 사항 test(0422)
- tf-idf 만들어보기 및 전처리
  - 사용자 사전 만들기 경로 설정 및 오류 개선 완료(0428)
  - 코로나 관련 공지 및 데이터프레임 개선
  - konlpy 사용자 사전 경로 관련 코드첨부(0429)
  - 병합시 생기는 encoding 오류 개선 및 외국어 처리 (0501)
- 학사 사용자 사전 구축(0501)

### Tf-IDF (0503~14)
- 전처리 및 TF-IDF 개선 (0506)
  - 현재 병목 ㅠㅠ 절차 정리해서 하기
  - 정제 -> 토큰화 ->형태소분석-> 기타과정
- 공지1 정제 후 TF-IDF 및 Textrank 시도 (0507)
- 공지1 textrank 변수명 고쳐서 성공. 다만 연산시간이 너무 길어 추가 전처리 필요 (0508)
- 1차 tf-idf 정리 코드 업로드 완료 -> for문으로 문장 돌려서 정방행렬 맞추는 것으로 방식 정정(0509)

### Textrank 및 summarization 1차(0515~0601)
- 학사 textrank 및 이에따른 sentence graph, summarization 그리기 (0515)
  - sentence 그래프 알고리즘 다시 생각해보기 (문장이 아닌 공지가 다 나옴)
- lovit님 textrank 함수 활용 및 okt, komoran 성능 비교 (0519)
- 희소행렬 벡터 에러 고치기 및 리스트 제외 결정 (0521)
- 에러개수 각 확인 (파트별 에러율 5%이하) (0526)
- 5/30까지 모델 구현후 모델링 시작 예정.
- 0529 외국어 filtering 구현 (한국어 0.3이하면 외국공지로 filter)
- 0530 외국어 예외처리 및 return 개선 + 모델링 전 점검
- 0602 fastapi 시범 및 okt에 불용어 처리 넣어보기


### 배포 (0602~0620)
- 0603 pickle 직렬화도전
- 0606 .pik, .sav 생성 및 ngrok 서버 연결
- 0607 1차 200ok 및 api 작동여부 확인 완료
- 0609 코드 class로 정리 및 rouge 평가 스터디
- 0610 rouge 분석 _ ngram, rouge-L 및 reference문장 기준 선정.
- 0612 pyrouge 다운 및 rouge-u 해보기
- 0613 testcase 및 json 예외처리
- 0614 return 개선 및 stopwords 클래스 내장화
  - aws 배포 스터디 (0615)
 -0616 중요키워드 가중치 올리기 + 정적 IP 
- 0617 고정도메인으로 실행 + 테스트데이터 추가, 전달용 백업 0616/0617 업뎃
  - 불용어, 중요한 단어 클래스 내장화
- 0620 엔드포인트 수정 및 논문쓰기 위한 postman 환경 설정

### 졸업논문 심화 연구(0621~)
- 목차 설정 및 공동저자 논의(08~)
