# Paper Clustering - 논문 분류기

### 소개
- Unsupervised(비지도 학습) 방법 중 Clustering을 이용하여 Paper들을 clustering

#### Language
- Language: Python
- Library: Tensorflow 1.14.0

#### Data 소개
- Data: 논문 55개
- Cluster 수: 10개

#### File 소개
- 01_html: html 문서로 논문 제목과 저자 추출
- 02_text_extraction: 논문 중 abstract와 introduction 부분 추출(.txt 이용) 및 텍스트 파일 생성
- 03_clustering: 
  - 1) Abstract+Introduction 부분 전처리: stopwords 제거
  - 2) Vectorize: Tf-idf vectorizer 이용
    - unigram, bigram, trigram 상위 20개 단어를 추출
  - 3) unigram + bigram + trigram을 이용하여 clustering
  - 4) 문서 유사도 측정
    - Cosine
    - Jaccard
    - Manhattan
    - Euclidean    
- 04_reference: 논문 reference 추출
