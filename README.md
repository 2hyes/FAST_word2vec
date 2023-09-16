# FAST_word2vec

## Research 1
### 데이터 디렉토리 구조
```
/
├── pretrained/
│   └── GoogleNews-vectors-negative300.bin
├── README.md
├── requirements.txt
├── research1/
    ├── data/
    │   ├── processed/
    │   │   ├── merged_data.csv
    │   │   └── similarity_coherence_data.csv
    │   └── raw/
    │       ├── rawdata_study1.xls
    │       └── rawdata_study2.xls
    ├── 0_save_data_merged_csv.ipynb
    ├── 1_check_words.ipynb
    ├── need_to_be_fixed.csv
    └── 2_get_similarity_and_coherence.ipynb
```

### 0. 준비
- research1/data/raw 디렉토리에 rawdata들을 위치시킨다.
- pretrained/ 디렉토리에 학습된 모델을 위치시킨다. 해당 프로젝트에서는 [GoogleNews-vectors-negative300 모델](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit?resourcekey=0-wjGZdNAUop6WykTtMip30g)을 사용한다. 다운로드받은 후, gz압축을 해제한 .bin형태로 사용한다.
- python 개발 환경을 준비한 후, `pip install -r requirements.txt` 명령어로 필요 라이브러리들을 설치한다.

### 1. 데이터 가공
`research1/0_save_data_merged_csv.ipynb` 소스코드를 통해, rawdata를 피험자들 각각 응답한 단어들을 하나의 row로 갖는 데이터프레임으로 전처리해준다.
해당 결과는 data/processed/merged_data.csv에 생성된다.

### 2. 분석
`research1/2_get_similarity_and_coherence.ipynb` 소스코드를 통해, 실험자가 요청한 대로 데이터를 가공하고 분석한다. 
해당 분석 결과는 research1/processed/similarity_coherence_data.csv에 저장된다.


## Research 2

### 데이터 디렉토리 구조
```
/
├── pretrained/
│   └── GoogleNews-vectors-negative300.bin
├── README.md
├── requirements.txt
├── research2/
    ├── data/
    │   ├── processed/
    │   │   └── similarity_coherence_data_90.csv
    │   └── raw/
    │       ├── web1-sess.1npy
    │       └── web2-sess.1npy
    └── 2_get_similarity_and_coherence_90.ipynb
```

### 0. 준비
- research2/data/raw 디렉토리에 rawdata들을 위치시킨다.
- pretrained/ 디렉토리에 학습된 모델을 위치시킨다. 해당 프로젝트에서는 [GoogleNews-vectors-negative300 모델](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit?resourcekey=0-wjGZdNAUop6WykTtMip30g)을 사용한다. 다운로드받은 후, gz압축을 해제한 .bin형태로 사용한다.
- python 개발 환경을 준비한 후, `pip install -r requirements.txt` 명령어로 필요 라이브러리들을 설치한다.

### 1. 분석
`research2/2_get_similarity_and_coherence_90.ipynb` 소스코드를 통해, 실험자가 요청한 대로 데이터를 가공하고 분석한다. 
해당 분석 결과는 research2/data/processed/similarity_coherence_data_90.csv에 저장된다.
