# poetry-generator-with-GPT2

### 구성원  

박정현, 윤소미, 이봉학, 김미원, 이형언

### 프로젝트명  

GPT2를 활용한 시 생성기

### 프로젝트 목적

HuggingFace API를 활용하여 한국어 GPT2 모델을 파인 튜닝, 크롤링한 데이터를 적용해 시를 생성하는 Causal LM 개발

### 역할  

주제 선정, 크롤링, 노이즈 제거, 전처리 및 훈련 코드 작성, 생성 방식 검증

<!--
- KoGPT-2를 웹에서 임의로 크롤링한 10만여건의 시로 파인튜닝하여 시적 표현을 생성하는 모델을 구축했습니다.
- huggingface API를 사용하여 training하였으며, 전처리 단계에서는 pandas와 re 모듈을 활용하여 시 본문 외의 노이즈를 최대한 줄였습니다.
- 시가 끝나는 시점마다 eos 토큰을 배치해 문장 생성시 보다 자연스럽게 완결이 되도록 했습니다.
- KoGPT-2_Poem_Generator.ipynb 파일을 이용해 시연이 가능합니다.
-->
