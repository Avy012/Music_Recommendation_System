## 📁 파일 구성

- **`data_merge.ipynb`**
  - **설명:** music_info.csv 데이터셋을 연결점으로 유저 데이터, 오디오 피처 + 가사 데이터를 결합하는 코드입니다.
  - **사용 데이터셋:** `Music Info.csv`, `User Listening History.csv`, `songs_with_attributes_and_lyrics.csv` -> `user_track.csv`
  - **music_info.csv 다운로드 링크(Kaggle):** https://www.kaggle.com/datasets/undefinenull/million-song-dataset-spotify-lastfm 
  - **User Listening History.csv 다운로드 링크(Kaggle):** https://www.kaggle.com/datasets/undefinenull/million-song-dataset-spotify-lastfm?select=User+Listening+History.csv
  - **songs_with_attributes_and_lyrics.csv 다운로드 링크(Kaggle):** https://www.kaggle.com/datasets/bwandowando/spotify-songs-with-attributes-and-lyrics
  - **user_track.csv 다운로드 링크(Google Drive):** https://drive.google.com/file/d/1kJA_Vxv98UZTN-WuhrNymTl7Kz5cr6Vr/view?usp=drive_link

- **`data_processing.ipynb`**
  - **설명:** 영어가사 추출, 재생횟수 범위 축소, key, mode 데이터 수치화를 진행하는 데이터 전처리 코드입니다.
  - **사용 데이터셋:** `user_track.csv`-> `balanced_lyrics.csv`

- **`BERT_embedding.ipynb`**
  - **설명:** 노래 가사에 대해 BERT를 이용해 문장 임베딩을 생성하는 코드입니다. 추천 모델의 입력으로 사용될 벡터를 생성합니다.
  - **사용 데이터셋:** `balanced_lyrics.csv` -> `emb_all_.csv`
  - **emb_all_.csv 다운로드 링크(Google Drive):** https://drive.google.com/file/d/1eHQhblqis0P2jXSGvnAVCThcO0QYj6RU/view?usp=drive_link

- **`NeuMF_No_BERT.ipynb`**
  - **설명:** NeuMF 모델을 이용한 추천 시스템 구현 코드입니다. BERT 없이 사용자-아이템, 오디오 피처만으로 학습합니다.
  - **사용 데이터셋:** `emb_all_.csv`

- **`NeuMF_with_BERT.ipynb`**
  - **설명:** BERT 임베딩을 반영한 NeuMF 추천 모델 구현 코드입니다. 사용자-아이템, 오디오 피처, 가사 BERT임베딩 벡터로 학습힙니다.
  - **사용 데이터셋:** `emb_all_.csv`

## 📦 라이브러리 설치 명령어
```bash
pip install pandas==2.2.2 numpy==2.1.2 tqdm==4.67.1 swifter==1.4.0 nltk==3.9.1 langdetect==1.0.9 scikit-learn==1.4.2 tensorflow==2.19.0 keras==3.9.2 torch==2.5.1 transformers==4.44.0 sentence-transformers==4.1.0
```

## 💻 실험 환경 정보

- OS: Windows 11
- 실행 환경: Visual Studio Code + Jupyter Notebook 확장
- Python 버전: 3.10.11
- 주요 라이브러리 및 버전:
  - pandas==2.2.2
  - numpy==2.1.2
  - tqdm==4.67.1
  - swifter==1.4.0
  - nltk==3.9.1
  - langdetect==1.0.9
  - scikit-learn==1.4.2
  - tensorflow==2.19.0
  - keras==3.9.2
  - torch==2.5.1
  - transformers==4.44.0
  - sentence-transformers==4.1.0

- 실행 전 설정:
  ```python
  import nltk
  nltk.download('words')
  ```
