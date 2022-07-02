---
layout: post
title: Hold-Out Cross Validation(홀드 아웃 교차 검증)이란?
description: >
  Hold-Out Cross Validation에 대하여
sitemap: false
categories:
  - study
  - MachineLearning
---


## Hold-Out이란?

- 데이터 셋을 Train Set과 Test Set 두 세트로 나누는 과정
- 일정 비율로 설정
- Train Set이 작으면 모델 정확도의 분산 증가 -> 과소적합 가능성 상승
- 반대로, Train Set이 커지면 과대적합 가능성 상승
![](https://velog.velcdn.com/images/kkamz/post/8bea714a-ac37-420b-a9d8-182394915ffe/image.png)

최고의 효율을 내기 위해 Random Subsampling이 있다.
- Train set과 Test set을 바꿔가면서 hold-out을 반복적으로 실행하는 것 
