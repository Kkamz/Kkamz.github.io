---
layout: post
title: K-Fold Cross Validation란?
description: >
  K-Fold Cross Validation란 무엇인가
sitemap: false
categories:
  - study
  - MachineLearning
---

# K-Fold Cross Validation(k-겹 교차 검증)

**- 보통 회귀 모델에 사용되며, 데이터가 독립적이고 동일한 분포를 가진 경우에 사용된다.**

## 정의 및 절차
> - 정의 : 전체 데이터셋을 k개의 fold로 나누어 번 다른 fold k개를 test data로, 나머지 개의 fold를 train data로 분할하는 과정을 반복함으로써 train 및 test data를 교차 변경하는 방법론
![](https://velog.velcdn.com/images/kkamz/post/190aecd8-a649-4528-b663-f71ef404d1d7/image.png)
- 절차	
    - 1. 전체 data set을 Train Set과 Test Set으로 나눈다
    - 2. Train Set을 k개의 Fold로 나눈다.
    - 3. k개의 폴드에서 각 폴드 1개씩은 Validation set으로 사용
    - 4. 성능 중 가장 성능이 좋은 모델을 찾기
    - 5. 가장 좋은 성능 모델을 통해 전체 Train set의 학습 진행
    - 6. 학습을 한 것을 토대로 Test set 평가
<br>
![](https://velog.velcdn.com/images/kkamz/post/bf72e6e6-273d-46d2-96ab-5c77b8d21215/image.png)
- 절차
    - 1. Train Set을 k개의 Fold로 나눈다.
    - 2. k개의 폴드에서 각 폴드 1개씩은 Validation set으로 사용
    - 3. 각각의 결과의 평균 값을 최종 성능으로 평가
