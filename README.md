# Text Classification

목적 : 주어진 문장 분류기의 영문으로 된 음식점 리뷰의 긍부정을 학습하여 정확도를 올리는 프로젝트입니다.


## 목적

Bert 모델을 활용하여 데이터 전처리과정, 하이퍼 파라미터 변경 등을 통해 성능을 개선합니다.

---

### Requirement

- transformers 4.16.2
- torch 1.10.0

### Preprocess

- 영문으로 된 음식점 리뷰 로드(train.1/train.0/dev.1/dev.0)
- bert tokenizer로 분절화된 토큰들의 아이디 값 리턴
- 리턴된 아이디 값으로 데이터셋 구축
- train_pos data(=> 1)와 train_neg data(=> 0)의 라벨링
- collate_fn_sentiment()에서 각 배치사이즈 마다의 max_sequence_len을 기준으로 패딩처리

### Train

- BertForSequenceClassification 모델 활용
- Optimizer : AdamW 활용
- Hyper Parameter 변경하며 성능 비교
- Early Stopping 활용

### issue

- 초반 prediction의 성능이 0.5로 비정상적으로 낮은 수치가 나오는 현상
- Hyper Parameter 변경

### Result
```bash
optimizer : AdamW
batch_size : 128
Learning_rate : 5e-5
random_seed : 42
epoch : 4
````
위의 조건으로 0.988의 성능 달성





