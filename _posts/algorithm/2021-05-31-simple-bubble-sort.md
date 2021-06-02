---
layout: post
title: "[알고리즘] 단순 정렬" ## 타이틀
date: 2021-05-31
excerpt: "" ## 설명
tags: [python, algorithm, sort, bubble sort]
category : Algorithm  ## 카테고리
comments: true
---

## 단순 정렬 알고리즘 종류

 1. 버블 정렬 (V)
 2. 삽입 정렬
 3. 선택 정렬

## 이론


## Python 코드

```python
N = 10
a = [9, 21, 51, 61, 2, 33, 48, 26, 1, 74]

for i in range(N-1):
    for j in range(i+1, N):
        if a[i] > a[j]:
            tmp = a[i]
            a[i] = a[j]
            a[j] = tmp 

for i in range(N):
    print(a[i], end=' ')
```

 - Output

```C#
 1 2 9 21 26 33 48 51 61 74
```