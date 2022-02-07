# Text Classification

목적 : 주어진 문장 분류기의 영문으로 된 음식점 리뷰의 긍부정을 학습하여 정확도를 올리는 프로젝트입니다.


## 목적

Bert 모델을 활용하여 데이터 전처리과정, 하이퍼 파라미터 변경 등을 통해 성능을 개선합니다.


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
  :arrow_forward: 기존의 bert 모델에서 단일 문장을 입력받아 cls 토큰이 분류값 중 하나가 되도록 학습
- Optimizer : AdamW 활용
- 


### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

