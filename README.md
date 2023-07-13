# KUBIG_2023_WIN Project

### 개인 투자자를 위한 기업 투자정보 요약 프로젝트

<img width="703" alt="스크린샷 2023-07-14 오전 1 17 45" src="https://github.com/cheongsu/NLP-News-Summary-Project/assets/103344737/1e4e1ab9-8ac2-41b9-be4f-5cc5201e8ab7">

### team

14기 김태영
16기 박민규
17기 임청수

### pre-trained model
- SKT-AI/KoBART model
https://github.com/SKT-AI/KoBART

- huggingface/Sentence-transformers
https://huggingface.co/sentence-transformers/paraphrase-distilroberta-base-v1

### fine-tuning
AI Hub 문서요약 텍스트 데이터 활용

- Train Data : 34,242 개
- Test Data  : 8,501  개

=> 직접 크롤링한 데이터에 KoBART를 finetuning한 model을 이용해 뉴스기사 요약 진행

=> 요약이 잘 안된 기사들을 거르기 위해 Title과 Content를 sentenceTransformer를 활용해 인코딩 후 유사도 구함

### service
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=FastAPI&logoColor=white">

1. 유저가 탐색하고자 하는 기업명 입력 * 국내 상장 기업 중

2. 해당 기업의 최신 뉴스 정보 요약 * 네이버 중권 뉴스

3. 유저에게 요약 결과 전달

