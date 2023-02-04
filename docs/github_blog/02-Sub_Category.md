---
layout: default
title: 2. Sub Category
parent: Github Blog
nav_order: 2
---

# Sub Category
이번 글에서는 [Just the Docs](https://pmarsceill.github.io/just-the-docs/) 테마에서 Sub Category 기능을 사용하는 방법을 알아보겠습니다.
![Just the Docs](/assets/images/github_blog/02-sub-category/categories.png)
## 포스팅 글의 구성
먼저, 서브 카테고리 기능을 사용하기 위해선, 깃허브 블로그의 포스팅 글의 구성을 알아야 합니다.  
깃허브 블로그 포스팅을 작성하기 위해서는 본문을 작성하기 전 기입되는 **헤더 부분**이 존재합니다.  
헤더 부분에는 layout, title, parent, nav_order 등의 정보가 들어가게 됩니다.  
- layout : **레이아웃**을 지정합니다.
- title : 포스팅 **글의 제목**을 지정합니다.
- parent : 포스팅 글의 **부모 카테고리**를 지정합니다.
- nav_order : 포스팅 **글의 순서**를 지정합니다.
### 최상단 Parent Category
제 블로그 최상단 카테고리 중 하나인 Camera Sensor 카테고리의 포스팅 글의 헤더 부분은 다음과 같습니다.
```
---
layout: default
title: Camera Sensor
nav_order: 2
has_children: true
permalink: docs/camera
---
```
최상단 카테고리의 본문이기 때문에 **parent 항목이 존재 하지 않고, has_children 항목이 true**로 되어 있습니다.
### Child Category
Camera Sensor 카테고리의 자식 Category인 Camera Coordinate 카테고리의 헤더 부분은 다음과 같습니다.
```
---
layout: default
title: Camera Coordinate
parent: Camera Sensor
nav_order: 1
has_children: true
permalink: docs/camera/coordinate
---
```
Camera Coordinate 카테고리 또한 child Category를 가질 수 있기 때문에 **has_children 항목이 true**로 되어 있고 부모 카테고리인 Camera Sensor 카테고리를 **parent 항목**으로 지정하고 있습니다.
### Child Category의 글
마지막으로 가장 아래에 있는 Camera Coordinate 카테고리의 포스팅 글의 헤더 부분은 다음과 같습니다.
```
---
layout: default
title: Introduction
parent: Camera Coordinate
grand_parent: Camera Sensor
nav_order: 1
---
```
Camera Coordinate 카테고리의 글이기 때문에 **parent 항목**으로 Camera Coordinate 카테고리를 지정하고 있고, **grand_parent 항목**으로 Camera Sensor 카테고리를 지정하고 있습니다.  
이렇게 parent와 grand_parent를 지정하면, 상위, 하위 카테고리 관계를 표현할 수 있어 서브 카테고리 기능을 구현할 수 있습니다.

---
참고로, 제 블로그의 소스 코드는 [여기](https://github.com/JongRok-Lee/JongRok-Lee.github.io)에서 확인하실 수 있습니다.