---
layout: post
title:  "Segmentation이란 무엇인가?"
date:   2020-06-30 10:08:56 +0900
categories: jekyll update
---

요즘 Computer Vision에서 핫한 분야를 뽑는다면 Segmentation이라고 할 수 있는데요.

Segmentation이란 무엇일까요? wikipedia에서 가져와 봤습니다.[0]

>컴퓨터 시각에서 분할은 디지털 영상을 여러 개의 픽셀 집합으로 나누는 과정을 말한다. 분할의 목적은 영상의 표현을 좀 더 의미있고 해석하기 쉬운 것으로 단순화하거나 변환하는 것이다.

실제 결과 영상[1]으로 보면 좀 더 이해가 쉬울 것이라고 생각됩니다. 입력 영상이 들어왔을 때 사람 말 배경 이렇게 나누는 것을(Segment) Segmentation이라고 합니다.

![(1)A Example of Segmentation ](http://127.0.0.1:4000/asset/fcn_segmentation_ex.png)

얼마전까지만 해도 Detector였던거 같은데 대표적인 예로는 yolo가 있습니다. 요즘은 Segmentation도 많은 연구가 진행되서 그런지 소스도 공개도 많이 되어 있고 여전히 많이 느리긴 하지만 가져다 쓸수 있는 정도의 속도와 Performance에 오지 않았나 생각이 됩니다.

Segmentation은 주로 두 가지고 나눠서 생각합니다. Instance Segmentation , Semantic Segmentation 이렇게 나누게 됩니다.

잘 설명한 블로그가 있어서 인용합니다. [2]

>Semantic Segmentation은 분할의 기본 단위를 클래스로 하여, 동일한 클래스에 해당하는 사물을 예측 마스크 상에 동일한 색상으로 표시합니다. 반면 Instance Segmentation은 분할의 기본 단위를 사물로 하여, 동일한 클래스에 해당하더라도 서로 다른 사물에 해당하면 이들을 예측 마스크 상에 다른 색상으로 표시합니다. 


![(2)Semantic Segmentation vs Instance Segmentation](http://127.0.0.1:4000/asset/segmentation-types.svg)

그림을 보면 감이 오실 것 같은데요 Semantic Segmentation 같은 경우에는 사람은 모두 레이블으로 인식하게 되고 Instance Segmentation 같은 경우에는 각각의 사람을 모두 다른 레이블을 부여해 주게 됩니다.

Segmentation에 대해

그 중에서도 제가 리뷰하고 싶은것은 DeepLab이라는 알고리즘 입니다.

원래는 Segnet을 하려고 했지만 DeepLab이 좀 더 최신 Paper이기도 하고 많은 Deep Learning Architecture를 포함하고 있어서 더 재미있을 것 같아서 리뷰하게 되었습니다.

여기까지 Segmentation에 대한 소개를 끝내고 본격적인 리뷰는 다음 페이지에서 하겠습니다.



-----------------------------------------------------------------------------
Reference

[0]: <https://ko.wikipedia.org/wiki/%EC%98%81%EC%83%81_%EB%B6%84%ED%95%A0>
[1]: <https://arxiv.org/pdf/1411.4038.pdf>
[2]: <http://research.sualab.com/introduction/2017/11/29/image-recognition-overview-2.html>


