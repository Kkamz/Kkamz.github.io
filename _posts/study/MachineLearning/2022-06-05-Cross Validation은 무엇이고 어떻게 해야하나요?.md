---
layout: post
title: Cross Validation은 무엇이고 어떻게 해야하나요?
description: >
  Cross Validation이란 무엇인가?
sitemap: false
categories:
  - study
  - MachineLearning
---

참고
[데이터 사이언스 인터뷰 질문 모음집](https://zzsza.github.io/data/2018/02/17/datascience-interivew-questions/#%EB%A8%B8%EC%8B%A0%EB%9F%AC%EB%8B%9D)


# Cross Validation은 무엇이고 어떻게 해야하나요?

## Cross Validation이란?
>#### Cross Validation은 교차 검증이라고 합니다.
- 보통 활용할 데이터가 있으면 Train set으로 모델을 훈련하고 Test set으로 모델을 검증합니다.
- **Test set으로만 모델 검증을 진행하면 약점이 존재합니다.**
    - 고정된 Test Set을 가지고 모델의 성능을 측정하게 된다면 _**과적합(Overfitting)**_되어 다른 실제 데이터를 가지고 수행하게 되면 엉망인 결과가 나오게 된다.
- 이를 해결하기 위해 하는 것이 Cross Validation(교차 검증)이다.

<br>

## Cross Validation은 어떻게 과적합 문제를 해결할까?
> 'Test set에 과적합 되는 문제'는 test set이 데이터 중 일부분으로 고정되어 있고, 이 일부분의 데이터 셋에 대하여 성능이 잘 나오도록 파라미터를 반복적으로 튜닝하기 때문에 발생합니다. 
Cross Validation(교차 검증)은 데이터의 모든 부분을 사용하여 모델을 검증하고, test set을 하나로 고정하지 않는다. 아래 그림을 살펴보자
![K-fold CV 예제](https://velog.velcdn.com/images/kkamz/post/c7c1b852-800d-4e5d-8861-41ecf8cbeb78/image.png)
K-fold CV = 전체 데이터 셋을 k개로 나누고 k번의 평가를 실행한다 -> test set 중복 없이 바꾸어가면서 진행
```
Accuracy의 평균 = (Accuracy1+Accuracy2+...Accuracyk)/k
```
Accuracy의 평균을 내어 최종적으로 모델의 성능을 평가
<br>
**_보통 5-fold나 10-fold를 많이 사용한다고 함_**

## Cross Validation의 장단점
>### 장점
- 모든 데이터 셋을 평가에 활용 가능 -> 과적합(Overfitting) 방지 / 데이터 편중 방지(k-fold 경우)
- 모든 데이터 셋을 훈련에 활용 가능 -> 정확도 향상 / 데이터 부족에서 오는 과소적합(Underfitting) 방지
    - 적은 데이터에 대한 Validation 신뢰성 상승
- 더욱 일반화된 모델 생성이 가능
<br>
### 단점
- 모델 훈련 및 평가 소요시간 증가
    - Iteration(반복) 횟수가 많기 때문
    
## Cross Validation 기법 종류
>- K-Fold Cross Validation(k-겹 교차 검증)
- Stratified k-fold cross validation(계층별 k-겹 교차검증)
- Hold-Out Cross Validation(홀드 아웃 교차 검증)
- Leave-p-Out Cross Validation
- Leave-One-Out Cross Validation
등

다음 글에서는 Cross Validation의 기법들의 대해 소개하겠습니다.

감사합니다.

