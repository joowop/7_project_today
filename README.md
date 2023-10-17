![image](https://github.com/joowop/7_project_today/assets/80230688/31647df0-e269-4427-99b9-6ea8e83aa909)# 📖 프로젝트명

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

1. 분류 모델
   - 채팅 감정분석, 노래 가사 감정분석<br>
   
2. 추천 시스템
   - 유사도 분석을 이용한 노래 추천 시스템
   - 노래 플레이리스트 생성<br>

3. 텍스트 요약
   - 채팅 내용 요약
   - 정보 요약<br>
   
### ✔️ 데이터 수집 방법

- Melon 음원 사이트 노래 제목, 가수, 가사 데이터 Crawling
- AI hub : 감성 대화 말뭉치 데이터, 감성 및 발화 스타일별 음성합성 데이터 활용
   
### ✔️ 주요 기능

1. 분석과정 (감정분석)
   - Bert 모델 커스텀 학습
     - 감정 type : ['기쁨','슬픔','분노','불안','상처','당황','중립']
     - 사용 Data <br>
       ![image](https://github.com/joowop/7_project_today/assets/80230688/28f20811-6bcd-441f-be23-cd5781fdc65d)<br>

     - 학습 결과<br>
       ![image](https://github.com/joowop/7_project_today/assets/80230688/d516fe3c-17cb-4669-960c-ef68f9b32554)<br>
       
   - 채팅 감정 분석
     - 예시(전남친과의 대화 카톡방)<br>
       ![image](https://github.com/joowop/7_project_today/assets/80230688/6d00ac96-b775-4089-b892-e22facc70205)<br>
       
     - 결과<br>
       ![image](https://github.com/joowop/7_project_today/assets/80230688/59831956-a10d-4669-93ce-264dadd89af0)<br>
       
   - 노래 가사 감정 분석
     - 노래 가사 감정 정보 <br>
       ![image](https://github.com/joowop/7_project_today/assets/80230688/0cc7bb11-fcbf-4cd3-94bd-7ba71f33e9e2)<br>
       
     - 노래 가사 Data <br>
       ![image](https://github.com/joowop/7_project_today/assets/80230688/c95559c2-ef5e-4977-8d0c-f59854fb332d)<br>

     - 노래 가사 감정 추론 <br>
       ![image](https://github.com/joowop/7_project_today/assets/80230688/d8750b99-d951-4b43-a1db-fa8af91ab1b1)<br>

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
