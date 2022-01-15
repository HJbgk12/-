# 1.-AI-Goorm-Text-Classification

주어진 문장 분류기의 정확도를 올리는 프로젝트

데이터로 주어진 음식점 리뷰를 긍정과 부정으로 카테고리화하여 분류

이슈 : index를 sorting 해주어서 csv 파일에 inference 할 경우
       test data의 index가 바뀌어 성능이 떨어지는 현상 발생
       
해결 : collate_fn_sentiment_test() function에서 기존 샘플의 index를 sorting하는 것이 아닌
       단순 ndarray 형태로 넘겨주어 해결함으로써 0.98정도로 성능 개선
       
그 외 다양한 하이퍼파라미터를 변경하여 성능개선
=> 0.988
