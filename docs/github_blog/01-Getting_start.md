---
layout: default
title: 1. Getting started
parent: Github Blog
nav_order: 1
---

# 1. Getting started
## Just the Docs 테마 가져오기
첫번째로 해야 할 것은, [Just the Docs](https://pmarsceill.github.io/just-the-docs/) 테마를 가져오는 것입니다. 
![Just the Docs](/assets/images/github_blog/01-getting-started/start_icon.png)
위 버튼을 누르면 아래와 같은 화면이 나오며 레포지토리의 이름을 username.github.io로 설정해야 합니다. 
![Just the Docs](/assets/images/github_blog/01-getting-started/repository_name.png)
그럼 이제 레포지토리가 생성되었으며, 이제 레포지토리를 클론하여 로컬에서 블로그 꾸미기 작업을 하면 됩니다.
# 기초 `config.yml` 설정
기본적으로 `_config.yml` 파일에서는 블로그의 기본적인 설정을 할 수 있으며, 아래와 같은 설정을 해주어야 합니다.

```yml
title: OpenJR
description: I hope my knowledge is helpful to many people.
theme: just-the-docs
url: https://JongRok-Lee.github.io/

# Enable or disable the site search
search_enabled: false
search:
  # Split pages into sections that can be searched individually
  # Supports 1 - 6, default: 2
  heading_level: 2
  # Maximum amount of previews per search result
  # Default: 3
  previews: 3
  # Maximum amount of words to display before a matched word in the preview
  # Default: 5
  preview_words_before: 3
  # Maximum amount of words to display after a matched word in the preview
  # Default: 10
  preview_words_after: 3
  # Set the search token separator
  # Default: /[\s\-/]+/
  # Example: enable support for hyphenated search words
  tokenizer_separator: /[\s/]+/
  # Display the relative url in search results
  # Supports true (default) or false
  rel_url: true
  # Enable or disable the search button that appears in the bottom right corner of every page
  # Supports true or false (default)
  button: false

# For copy button on code
enable_copy_code_button: true

# Color scheme currently only supports "dark", "light"/nil (default), or a custom scheme that you define
color_scheme: "dark"

# Enable or disable heading anchors
heading_anchors: false

callouts_level: quiet # or loud
callouts:
  highlight:
    color: yellow
  important:
    title: Important
    color: blue
  new:
    title: New
    color: green
  note:
    title: Note
    color: purple
  warning:
    title: Warning
    color: red
```
각 설명들은 Just the Docs의 [Configuration](https://just-the-docs.github.io/just-the-docs/docs/configuration/)를 참고하시면 됩니다.

자 그럼 기본적인 설정은 끝났으니, 다음 글 부터는 블로그를 커스터 마이징 하는 방법들을 알아보겠습니다.