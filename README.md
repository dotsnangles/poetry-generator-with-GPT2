# KoGPT-2_Poem_Generator
---
- KoGPT-2를 웹에서 임의로 크롤링한 10만여건의 시로 파인튜닝하여 시적 표현을 생성하는 모델을 구축했습니다.
- huggingface API를 사용하여 training하였으며, 전처리 단계에서는 pandas와 re 모듈을 활용하여 시 본문 외의 노이즈를 최대한 줄였습니다.
- 시가 끝나는 시점마다 eos 토큰을 배치해 문장 생성시 보다 자연스럽게 완결이 되도록 했습니다.
- KoGPT-2_Poem_Generator.ipynb 파일을 이용해 시연이 가능합니다.
