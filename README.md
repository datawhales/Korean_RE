# Korean_RE (Korean Relation Extraction)
한국어 문장 내 관계 추출을 통한 지식 그래프를 구축하는 방법에 대해 연구한 프로젝트입니다. (2021.03 ~ 2022.01)

한국어 관계 추출 데이터셋을 직접 구축하고, 한국어로 사전 학습된 BERT 모델 [KR-BERT-MEDIUM](https://github.com/snunlp/KR-BERT-MEDIUM)을 이용하여 한국어 관계 추출 모델을 학습하였습니다.

학습된 모델을 이용하는 [**한국어 관계 추출 모듈 korre**](https://github.com/datawhales/korre)를 개발하여 공개하였습니다.

## Korean Relation Extraction Dataset
한국어 위키피디아 코퍼스 데이터와 위키데이터를 활용하여 한국어 관계 추출 데이터셋을 구축하였습니다.

한국어 위키피디아 코퍼스에 대해 **Entity Recognition**을 통해 **Entity Extraction**을 진행하고, 이를 위키데이터에 **Entity Linking**하여 관계 트리플 데이터를 얻어 데이터셋으로 구축하였습니다.

### Download
한국어 관계 추출 데이터셋: [Download](https://drive.google.com/file/d/184Qg2yTRKVlxyyhHSvHY7KmG16rQwpdV/view?usp=sharing)

### Dataset Details
데이터셋은 csv 파일 형태로 되어 있습니다.

- `sentence`: 관계를 추출하고자 하는 문장을 의미합니다.

- `subj_name`, `subj_start_pos`, `subj_end_pos`, `subj_type`: 문장 내에서 주체(첫 번째 개체)에 해당하는 개체의 이름, 시작 인덱스, 끝 인덱스, 개체 타입을 의미합니다.

- `obj_name`, `obj_start_pos`, `obj_end_pos`,	`obj_type`: 문장 내에서 대상(두 번째 개체)에 해당하는 개체의 이름, 시작 인덱스, 끝 인덱스, 개체 타입을 의미합니다.

- `relation`: 해당 문장에서 두 개체 사이에 존재하는 관계의 위키데이터 id를 의미합니다.

| sentence | subj_name | subj_start_pos | subj_end_pos | subj_type | obj_name | obj_start_pos | obj_end_pos | obj_type | relation |
| -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
| 마저리 모나한은 미국의 텔레비전 배우, 영화배우, 연극 배우이다. | 마저리 모나한 | 0 | 7 | PERSON | 미국 | 9 | 11 | COUNTRY	| P27 |