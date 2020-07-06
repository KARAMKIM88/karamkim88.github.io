---
layout: post
title:  "Study of Fiducial Marker"
date:   2020-06-29 15:55:56 +0900
categories: jekyll update
---

영상에서 현재 카메라 포즈를 알면 다양한 Application을 만들수가 있습니다.

예를 들어서 AR도 할수 있고 Visual Servoing도 할 수 있습니다.

그래서 관련한 분야는 과거에도 그렇고 현재에도 많이 연구를 하고 있는데요.

카메라 포즈를 계산하는 데는 다양한 방법이 있는데 가장 손쉽게 현재 카메라 위치를 얻는 방법은 확실한 Visual Cue를 사용하는 것입니다.

아마 주변에서 쉽게 찾아볼 수 있다고 보는데요 아래와 같이 생겼습니다.

이렇게 생긴것을 Fiducial marker라고 합니다.

![(1)examples of fiducial markers](https://karamkim88.github.io/asset/fiducial_marker.png){: width="400", height="457"}

이러한 Marker를 사용하게 되면 장점이 빠르고 정확하게 카메라의 포즈를 잘 계산할수 있기 때문에 여전히 많이 사용되는 것 같습니다.

하지만 개인적으로는 마커의 외모가 매우 못생겨서..ㅠ(아 너무 못생겼어요..ㅠㅠ) 제 개인적인 생각으로는 널리 퍼지기에는 무리가 있지 않나 생각이 됩니다.

하지만 이런 마커를 사용하게 된다면 내부적으로 어떻게 Marker를 찾고 카메라 포즈 계산 하는지 알아야 한다고 생각합니다.

무엇보다도 Camera Pose를 어떻게 계산하는지 알 필요가 있습니다. 

Detection자체는 워낙 잘되기 때문에 간단하게 살펴 보겠습니다.
![(2)process of fiducial markers detection](https://karamkim88.github.io/asset/fiducial_marker_process.png)

인터넷에 좋은 그림이 있어서 잠깐 가져왔습니다. 적당한 임계값을 줘서 영역을 찾고 엣지를 찾아서 사각형 박스를 찾는 알고리즘을 이용하고 있습니다. 

많은 분들의 오해가 marker안에 있는 패턴이 pose를 계산하는데 사용될 것이라고 생각하시는데 전혀 그렇지 않습니다.(중요!)

사각형의 4점이 카메라 포즈를 계산하는 데 이용되게 됩니다.

안에 있는 패턴은 마커의 ID를 구분하는데 이용하게 됩니다.

네점을 이용해서 pose를 구하는 부분은 매우 중요한 부분이기 때문에 다음장에서 설명하겠습니다.






-----------------------------------------------------------------------------
Reference

(1) https://en.wikipedia.org/wiki/Fiducial_marker

(2) https://ria.ua.pt/bitstream/10773/23890/1/artigo.pdf





