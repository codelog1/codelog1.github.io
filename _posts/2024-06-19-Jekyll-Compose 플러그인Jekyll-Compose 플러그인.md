## Jekyll-Compose 플러그인

Jekyll-Compose 플러그인은 Jekyll을 사용하여 블로그 또는 정적 사이트를 관리할 때 유용하게 사용할 수 있는 플러그인입니다. 이 플러그인은 여러 가지 하위 명령어를 추가하여 포스트, 페이지, 초안을 생성하고 관리하는 작업을 훨씬 간편하게 만들어 줍니다.

### 주요 기능

1. **포스트 생성**: 새로운 블로그 포스트를 생성할 수 있습니다. 예를 들어, `jekyll post "새로운 포스트"` 명령어를 사용하면 자동으로 포스트 파일을 생성합니다.
2. **초안 작성**: 아직 완성되지 않은 포스트를 초안으로 저장할 수 있습니다. `jekyll draft "초안 제목"` 명령어로 쉽게 사용할 수 있습니다.
3. **퍼블리싱**: 초안 상태의 포스트를 실제 게시글로 퍼블리싱할 수 있습니다. `jekyll publish _drafts/초안파일.md` 명령어로 가능합니다.
4. **페이지 생성**: 블로그 포스트뿐만 아니라 웹사이트의 페이지도 쉽게 생성할 수 있습니다.

### 설치 및 설정 방법

Jekyll-Compose 플러그인을 설치하려면 `Gemfile`에 다음과 같이 추가합니다:

```ruby
group :jekyll_plugins do
  gem 'jekyll-compose'
end
```

그런 다음 아래 명령어를 실행하여 설치합니다:

```bash
bundle install
```

`_config.yml` 파일의 `jekyll_compose` 섹션에서 기본 설정을 수정할 수 있습니다. 예를 들어, 새 초안이나 포스트를 생성할 때 자동으로 텍스트 에디터가 열리도록 설정할 수 있습니다[0][1].

https://github.com/jekyll/jekyll-compose

https://jekyllrb.com/docs/plugins/your-first-plugin/

### 예시 명령어

- 새로운 포스트 생성:
    
    ```bash
    jekyll post "포스트 제목"
    
    ```
    
- 새로운 초안 작성:
    
    ```bash
    jekyll draft "초안 제목"
    
    ```
    
- 초안 퍼블리싱:
    
    ```bash
    jekyll publish _drafts/초안제목.md
    
    ```
    
- 페이지 생성:
    
    ```bash
    jekyll page "페이지 제목"
    
    ```
    

Jekyll-Compose를 사용하면 이러한 작업을 통해 콘텐츠 관리가 보다 효율적이고 체계적으로 이루어질 수 있습니다[3][4][6].

https://planetjekyll.github.io/plugins/

https://jekyllrb-ko.github.io/docs/plugins/your-first-plugin/

https://learn.cloudcannon.com/jekyll/using-jekyll-plugins/

---

## **Jekyll-Compose 플러그인을 사용한 포스트 및 페이지 관리**

Jekyll-Compose는 Jekyll 웹사이트에서 포스트나 페이지, 초안을 쉽게 생성할 수 있도록 도와주는 플러그인입니다. 이 플러그인을 설치하고 사용하는 방법은 다음과 같습니다.

### 설치

Gemfile에 Jekyll-Compose를 추가합니다:

```ruby
group :jekyll_plugins do
  gem "jekyll-compose"
end
```

이후 `bundle install` 명령어를 실행하여 플러그인을 설치합니다.

### 사용법

### 포스트 생성

다음 명령어를 사용하여 새로운 포스트를 생성할 수 있습니다:

```bash
bundle exec jekyll post "포스트 제목"
```

이 명령어를 실행하면 `_posts` 디렉토리에 새로운 마크다운 파일이 생성됩니다.

### 페이지 생성

새로운 페이지를 생성하려면 다음 명령어를 사용합니다:

```bash
bundle exec jekyll page "페이지 이름"
```

이 명령어를 실행하면 사이트의 루트 디렉토리에 새로운 페이지 파일이 생성됩니다.

### 초안 생성

초안은 `_drafts` 디렉토리에 생성됩니다. 생성하려면 다음 명령어를 사용합니다:

```bash
bundle exec jekyll draft "초안 제목"

```

초안 파일은 `_drafts` 폴더에 저장되며, 아직 게시되지 않은 상태로 유지됩니다.

### 초안 게시

생성된 초안을 게시하려면 다음 명령어를 사용합니다:

```bash
bundle exec jekyll publish _drafts/초안-제목.md
```

이 명령어를 실행하면 초안 파일이 `_posts` 디렉토리로 이동되고, 현재 날짜가 포스트의 날짜로 설정됩니다.

### 예시

다음은 `jekyll post` 명령어를 사용하여 새 포스트를 생성하는 예시입니다:

```bash
bundle exec jekyll post "My New Post"
```

이 명령어는 `_posts/YYYY-MM-DD-my-new-post.md` 파일을 생성하고, 기본적인 YAML 헤더를 자동으로 추가합니다.

이와 같은 명령어들을 통해 Jekyll-Compose 플러그인을 사용하면 포스트와 페이지, 초안을 손쉽게 관리할 수 있습니다.
