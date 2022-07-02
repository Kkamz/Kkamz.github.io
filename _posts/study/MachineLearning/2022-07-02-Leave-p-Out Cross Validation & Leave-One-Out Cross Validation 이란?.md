---
layout: post
title: Leave-p-Out Cross Validation & Leave-One-Out Cross Validation 이란?
description: >
  Leave-p-Out Cross Validation & Leave-One-Out Cross Validation 대하여
sitemap: false
categories:
  - study
  - MachineLearning
---

# Leave-p-Out Cross Validation & Leave-One-Out Cross Validation 이란?

## Leave-p-Out Cross Validation 
>- 전체 데이터 중에서 p개의 샘플을 선택 -> 모델 검증에 사용
- 따라서, test set을 구성할 수 있는 경우의 수
    - $$nCp$$ : 조합
-  각 데이터 폴드 세트의 검증 결과들을 평균 -> 최종적인 검증 결과를 도출하는 것이 일반적 
- 데이터 폴드 세트의 경우의 수가 매우 크기 때문에, 계산 시간에 대한 부담이 매우 큼
![](https://velog.velcdn.com/images/kkamz/post/1f5e8527-e815-427f-bc78-5f88e1886076/image.png)


## Leave-One-Out Cross Validation
>- Leave-One-Out Cross Validation은 k분할 교차 검증에서 개별 분할 샘플이 하나
   - K개의 데이터를 K분할하여, K번 Train&Test를 실행
   <br>
- 데이터세트가 작은 경우 더 나은 추정이 가능하게 되는 방법 
- 테스트 세트를 하나가 아닌 P개 사용하는 경우를, Leave-p-Out Cross Validation 이라고 부름
![](https://velog.velcdn.com/images/kkamz/post/12760aae-9f57-465c-b541-fe4e084d90be/image.png)
