# Korean_RE (Korean Relation Extraction)
한국어 문장 내 관계 추출을 통한 지식 그래프를 구축하는 방법에 대해 연구한 프로젝트입니다. (2021.03 ~ 2022.01)

한국어 관계 추출 데이터셋을 직접 구축하고, 한국어로 사전 학습된 BERT 모델 [KR-BERT-MEDIUM](https://github.com/snunlp/KR-BERT-MEDIUM)을 이용하여 한국어 관계 추출 모델을 학습하였습니다.

학습된 모델을 이용하는 [**한국어 관계 추출 모듈 korre**](https://github.com/datawhales/korre)을 개발하여 공개하였습니다.

## Korean Relation Extraction Dataset
**한국어 관계 추출 데이터셋**: [Download](https://drive.google.com/file/d/184Qg2yTRKVlxyyhHSvHY7KmG16rQwpdV/view?usp=sharing)

한국어 위키피디아 코퍼스 데이터와 위키데이터를 활용하여 한국어 관계 추출 데이터셋을 구축하였습니다.

한국어 위키피디아 코퍼스에 대해 **Entity Recognition**을 통해 **Entity Extraction**을 진행하고, 이를 위키데이터에 **Entity Linking**하여 관계 트리플 데이터를 얻어 데이터셋으로 구축하였습니다.