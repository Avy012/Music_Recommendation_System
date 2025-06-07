## 📁 파일 구성

| 파일명 | 설명 |
|--------|------|
| `BERT_embedding.ipynb` | 노래 가사에 대해 BERT를 이용해 문장 임베딩을 생성하는 코드입니다. 추천 모델의 입력으로 사용될 벡터를 생성합니다. |
| `data_processing.ipynb` | 원본 음악 데이터 및 사용자 데이터를 전처리하고, 분석 및 모델 학습을 위한 형식으로 가공합니다. |
| `data_merge.ipynb` | BERT 임베딩 결과와 전처리된 사용자-아이템 데이터를 병합하여 학습에 사용할 최종 데이터를 구성합니다. |
| `NeuMF_No_BERT.ipynb` | 기존 NeuMF 모델을 이용한 추천 시스템 구현 코드입니다. BERT 없이 사용자-아이템 행렬만으로 학습합니다. |
| `NeuMF_with_BERT copy.ipynb` | BERT 임베딩을 반영한 NeuMF 추천 모델 구현 코드입니다. 콘텐츠 기반 정보와 협업 필터링을 결합하여 추천 성능을 향상시킵니다. |

## 💻 실험 환경 정보

- OS: Windows 11
- 실행 환경: Visual Studio Code + Jupyter Notebook 확장
- Python 버전: 3.9.13
- 주요 라이브러리 및 버전:
  - pandas==1.5.3
  - numpy==1.24.4
  - tqdm==4.65.0
  - swifter==1.3.5
  - nltk==3.8.1
  - langdetect==1.0.9
  - scikit-learn==1.2.2
  - tensorflow==2.11.0
  - keras==2.11.0
  - torch==1.13.1
  - transformers==4.30.2
  - sentence-transformers==2.2.2

- 실행 전 설정:
  ```python
  import nltk
  nltk.download('words')
