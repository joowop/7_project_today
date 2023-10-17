# 📖 프로젝트명

### ✔️ NLP를 활용한 오늘 하루 요약 프로젝트 (메티버스 아카데미 2기 AI반 7월 프로젝트)

# 📃 프로젝트 소개

### ✔️ AI를 활용하여 오늘 하루의 카톡 대화 내용을 분석(감정 분석)하여 해당 감정에 맞는 노래를 추천해주고 대화 내용을 요약하여 일기를 대신 작성해주는 서비스 입니다. 


# 👩‍🔧 팀원 소개 및 역할

### ✔️ 팀원

메타버스 아카데미 2기 AI반 서주완, 김나래, 이정빈, 원예찬 총 4명

### ✔️ 역할 분담

- 서주완 : GPT 활용 대화 요약, Song2Vec 모델 활용 노래 추천
 
- 김나래 : Song2Vec 모델 활용 노래 추천, Bert 활용 감정분석
  
- 이정빈 : Figma 구현
  
- 원예찬 : 감정별 노래 데이터 수집
  
# 📅프로젝트 진행 기록

### ✔️ 수행 기간

2023.07.03 ~ 2023.07.31

# 💡 주요 내용

### ✔️ 개요

1. 분류 모델델
   - 분실된 도서, 뒤집어진 도서, 위치 변경이 필요한 도서 Detection
   - Detection된 도서의 정확한 위치 파악
     <br>
2. 추천시스템 패스파인더
   - 이용자들에게 유사도 기반의 도서 추천
   - 도서 찾기<br>
   
### ✔️ 데이터 수집 방법

1. 장서 점검<br>
   (1) 직접 찍은 책장 사진 데이터<br>
   (2) 책(BOOK), 뒤집어진 책(BOOK_REVERSED), 책 라벨, (BOOK_LABEL), 뒤집어진 책 라벨, (BOOK_REVERSED_LABLE)<br>
   <br>
2. 추천시스템 패스파인더 <br>
   (1) 교보문고 및 도서관 도서 데이터 Crawling <br>
   <br>
   
### ✔️ 주요 기능

1. 서비스 기능(장서 점검)
   (1) roboflow<br>
       - 직접 찍은 책장 사진 데이터 라벨링<br>
       - book, book_label, book_reversed, book_reversed_lable<br>
         - 약 3000개의 데이터셋 확보<br>
   <br>
   (2) YOLOv8-s 모델<br>
       - mAP50 : 0.987<br>
       ![results](https://github.com/joowop/octaforaugust/assets/80230688/85abebf4-ead8-4a3d-ba55-e6d2cdf9e0fe)<br>
       ![image](https://github.com/joowop/octaforaugust/assets/80230688/5ae83b47-515c-405e-bd96-2874ae7e7381)<br>
       - 높은 정확도 도출 및 class별 객체 탐지가 우수<br>
   
   (3) easy ocr <br>
       - yolo를 통해 탐지된 책 라벨 Crop하여 저장<br>
       - Crop된 라벨 이미지 ocr<br>
       ![스크린샷 2023-10-17 101115](https://github.com/joowop/octaforaugust/assets/80230688/601ef66b-4428-4f54-ab68-16ecf5323528)<br>
   <br>
   (3) 장서 점검 모델<br>
       - ocr된 라벨을 통해 뒤집어진 도서, 순서가 바뀐 도서, 분실된 도서를 탐지 하고 사서에게 알려주는 알고리즘 구현<br>
   <br>
   
2. 서비스 기능 (추천 시스템 패스파인더)
   (1) 데이터셋<br>
       - 데이터 수 : 교보문고 크롤링 데이터셋 약 10000건 (정치/사회,역사/문화,가정/육아,기술/공학, 종교, 요리 등)<br>
       - 수집 내용 : 책 제목, 키워드, 저자, 출판사, 리뷰 수, 리뷰 내용<br>
   <br>
   (2) 유사도 기반 추천 시스템<br>
       - 트랜스포머를 이용하여 키워드 문장의 임베딩을 얻고, 입력값과 코사인유사도 값이 가장 높은 키워드를 얻어냄<br>
       - 해당 키워드와 짝이 되는 내용을 도출<br>
       ![image](https://github.com/joowop/octaforaugust/assets/80230688/f6f09b51-e209-40b0-a0a8-704e4d7e9500)<br>
   <br>
4. 서비스 기능 (도서관 Q/A 챗)
   (1) 데이터셋<br>
       1.1 초창기 모델<br>
           - 데이터 수 : 대학도서관, 공공도서관 질의 응답 데이터 셋 약 4500 건<br>
           - KoGPT-2 모델을 이용한 생성 모델에 전체 4500건 데이터 학습<br>
           - + 정제된 데이터 셋 150건 학습<br>
           ![image](https://github.com/joowop/octaforaugust/assets/80230688/3f585522-3dc5-466e-bb6d-81fb1bfd917c)<br>
       <br>
       1.2 개선 모델<br>
           - 데이터 수 : 대학도서관, 공공도서관 자주 묻는 질문 데이터셋 약 150 건<br>
           ![image](https://github.com/joowop/octaforaugust/assets/80230688/9b36a30c-ecd5-4fc6-9cca-7732f10949e8)<br>
   <br>

### ✔️ 결과
![image](https://github.com/joowop/7_project_today/assets/80230688/5f627b48-f3e6-4ba6-9269-53d56909daa9)<br>

1. 기대효과
- 소중한 추억을 보관하고 기록할수 있습니다.
- 빠르고 쉽게 하루를 마무리 할 수 있습니다.
- 대화 속 키워드로 유용한 맞춤 광고를 받을 수 있습니다.
- 소중한 순간을 공유하고 감동을 선물할 수 있습니다.

# 🛠 기술 스택

### ▪ 언어
<img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white">

### ▪ 주요 라이브러리
<img src="https://img.shields.io/badge/BERT-F7931E?style=for-the-badge&logo=BERT&logoColor=white"> <img src="https://img.shields.io/badge/GPT-150458?style=for-the-badge&logo=GPT&logoColor=white">
<img src="https://img.shields.io/badge/Song2vec-013243?style=for-the-badge&logo=Song2vec&logoColor=white"> <img src="https://img.shields.io/badge/Bart-99CC00?style=for-the-badge&logo=Bart&logoColor=white">

### ▪ 개발 툴
<img src="https://img.shields.io/badge/VS code-2F80ED?style=for-the-badge&logo=VS code&logoColor=white"> <img src="https://img.shields.io/badge/Google Colab-F9AB00?style=for-the-badge&logo=Google Colab&logoColor=white">

### ▪ 협업 툴
<img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=Github&logoColor=white"> <img src="https://img.shields.io/badge/Google Slides-FFBB00?style=for-the-badge&logo=Google Slides&logoColor=white">
