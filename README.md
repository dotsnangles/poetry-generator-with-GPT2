# poetry-generator-with-GPT2

### Objectives
- 시 생성 언어모델 개발을 위해 웹 크롤링한 데이터를 활용, GPT2를 파인튜닝한다.

### Models and Data
- skt/kogpt2-base-v2
- 웹사이트 시 사랑 시의 백과사전 시인의 시 106371건

### Envs and Requirements
- Colab, Git/Github
- BeautifulSoup, Pandas, RE, Huggingface, PyTorch

### Progress
- 웹 크롤링 및 텍스트 데이터 정제
- GPT-2 토크나이저로 토큰화 및 정수 인코딩 / SentencePiece 토크나이저 학습
- 훈련 코드 작성 및 훈련
- 문장 생성 종료를 위한 스페셜 토큰 추가
- 각종 제너레이션 메소드 실험

### Retrospective
- 처음으로 Transformer PLM을 활용해본 프로젝트
- 당시에는 Masked LM보다는 Causal LM의 활용 방안이 더 직관적이었기 때문에 한국어로 사전 학습 된 GPT 계열의 모델을 탐색함
- SKT에서 사전 학습한 KoGPT-2를 발견하고 Transformer PLM 허브인 Huggingface를 활용해야 함을 인지
- 창작 활동에 도움을 주는 모델을 개발하고자 데이터를 물색했으나 실패
- 웹 크롤링을 통해 10만건 이상의 시 데이터를 확보
- Raw 데이터의 경우 유형화된 노이즈가 상당 수 존재했기에 정규표현식을 활용해 제거
- Huggingface API 구성을 파악한 뒤 Transformers, Datasets, Tokenizers를 활용해 훈련 코드를 작성
- 훈련이 끝난 모델의 생성 문장에서 동일 단어 반복을 줄이기 위해 각종 제너레이션 메소드를 이해한 뒤 적용
- 생성된 시가 종결될 수 있도록 EOS 토큰을 추가하여 재훈련
- 훈련 성과 측정을 위해 파인튜닝 전후 Perplexity를 산출해 비교
- 기발한 표현의 문장들이 생성되는 것을 기대했으나 최종 결과물로 산출한 문장들은 복고풍의 서정시인 경우가 많았음
- 좋은 결과물을 얻기 위해서는 좋은 데이터를 사용해야 한다는 점을 재차 확인

### References
- https://huggingface.co/
- https://pytorch.org/
- https://github.com/SKT-AI/KoGPT2
- https://jalammar.github.io/illustrated-gpt2/
