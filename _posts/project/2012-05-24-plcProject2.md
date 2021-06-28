---
layout: post
title: "Window Application 제작 with PLC 통신 (2)" ## 타이틀
date: 2021-02-22
excerpt: "MX Component를 활용한 C#과 PLC간의 통신" ## 설명
tags: [PLC, C#, Python, Mitsubishi, communication, MX Component, MX, 파이썬, winform, ui]
category : Project  ## 카테고리
comments: true
---

# 1. PC <=> PLC Ethernet 통신

 PC와 Mitsubishi PLC가 Ethernet 통신하는 방법은 크게 두 가지가 있다.
  
 1. MX Component에서 제공하는 라이브러리 활용
 2. MC 프로토콜로 

<figure>
	<img src="/img/project/systemConfigImage.PNG">
	<figcaption>System Configuration</figcaption>
</figure>

 위처럼 시스템을 구성한 대표적인 이유는 아래와 같다.
  
## Q) 왜 C#을 사용했는가?
  1. MX Component에서 제공하는 32bit dll을 사용하기 위해 (MELSEC에서 32bit dll만 제공)
  2. C#의 안정성 및 속도 때문에
  3. 풍부한 UI Design 예제 및 관련 자료 때문에

## Q) 왜 Algorithm을 Python으로 구성했는가?
 1. Python의 높은 **생산성** 때문에 (프로토타입의 빠른 제작 및 빈번한 알고리즘 수정에 대한 대응)
 2. 학습한 Deep Learning Model을 적용하기 위해
 3. 이후 Server 배포 시 구현하고자 하는 Django/Flask 프로그램에 대한 확장성 때문에

### 　

# 2. 프로그램 개발 일정
  
<figure>
	<img src="/img/project/schedule.png">
	<figcaption>Schedule</figcaption>
</figure>

### 　

# 3. UI Concept

 '[2021 UI Trend](https://www.youtube.com/watch?v=5RluSnRPRbI)'를 참고하여 가장 깔끔하다고 생각되는 'Colors on White Surface'로 초기 컨셉을 구성했으나, 
 현장 Monitor의 설치 위치가 User와 거리가 멀어 Contents의 가독성이 떨어지는 이유로 'Dark Mode'로 변경하였다. 상단 Mainmenu bar로 User 타입에 따라 보는 
 페이지를 구분하였고, 좌측 Submenu Bar로 별도 페이지 내 구분을 표기하였다.

 제공하는 컨텐츠가 적음에도 하기와 같이 구성한 이유는 추후 제작하게 될 UI나 현재 프로그램의 Contents 추가 요청 시 좀 더 쉽게 대응하기 위해 이처럼 구성하였다.

<figure>
	<img src="/img/project/ui1.png">
	<figcaption>UI Description</figcaption>
</figure>

<figure class="half">
	<img src="/img/project/uiStatus.png">
	<img src="/img/project/uiDashboard.png">
</figure>

<figure class="half">
	<img src="/img/project/uiGraph.png">
	<img src="/img/project/uiStatic.png">
    <figcaption>UI Pages</figcaption>
</figure>

