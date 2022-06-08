---
layout: post
title: Stratified k-fold cross validation(계층별 k-겹 교차검증)
description: >
  Stratified k-fold cross validation(계층별 k-겹 교차검증)에 대하여
sitemap: false
categories:
  - study
  - MachineLearning
---


# Stratified k-fold cross validation(계층별 k-겹 교차검증)

## K-fold 문제점
![](https://velog.velcdn.com/images/kkamz/post/c107298f-11ae-41b7-b960-7a41565cd47e/image.png) 

- 일정하게 fold를 나누기 때문에 데이터 편향이 일어날 수 있음
- 이것을 해결하기위해 Stratified k-fold를 사용하여 해결

## Stratified k-fold cross validation
- k-fold의 문제점인 target 데이터의 비율을 일정하게 유지하지 못하는 것을 일정하게 유지하게 해줌
- **대체적으로 회귀에서는 기본적인 K-fold를사용 , 분류에서는 Stratified k-fold를 사용**



