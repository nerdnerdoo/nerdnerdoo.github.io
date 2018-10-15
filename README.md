# Nerd? 너두! Blog

## 글 쓰는 방법

### 일반 글

`/_posts` 디렉토리에 `YYYY-MM-DD-{title}.md` 형태로 텍스트 파일을 생성 후 아래 템플릿을 참고하여 글을 작성한다.

    ---
    layout: single
    title: '이 글의 제목'
    tag: # 태깅 정보
    categories: 'news' # 'news', 'blog', ...
    author: # 이 글의 작성자 정보
    author_profile: false # 작성자 정보를 보여줄지 여부
    toc: false # table of contents 를 보여줄지 여부
    ---
    여기서부터는 자유롭게 Markdown 형태로 작성

### 프로젝트 글

`/_projects` 디렉토리에 글 작성. 일반 글과 같은 형태로 작성하면 됨.

## Test

### github.io 에서 직접 확인

글을 작성 후 바로 github에 commit한 후 홈페이지에서 확인.

[https://nerdnerdoo.github.io](https://nerdnerdoo.github.io)

### Local server 에서 확인 후 업로드

로컬에서 Jekyll 서버를 실행시켜 글이 잘 나오는지 확인 후 github에 commit

#### Jekyll 로컬 설정

    $ sudo apt-get install ruby ruby-all-dev

    # .bashrc or .zshrc
    export GEM_HOME=$HOME/gems
    export PATH=$HOME/gems/bin:$PATH

    # bundler 설치
    $ gem install bundler

    # 블로그 전체 다운로드
    $ git clone https://github.com/nerdnerdoo/nerdnerdoo.github.io
    $ cd nerdnerdoo.github.io

    # 필요한 패키지 설치
    $ bundle

#### Jekyll 로컬 실행

    # 아래 명령을 실행하면 웹서버가 실행된다. http://localhost:4000 으로 접속하면 내용을 볼 수 있다.
    $ jekyll serve

_posts/ 또는 _projects/ 의 파일이 변경되면 자동으로 업데이트가 된다. 단 _config.yml이나 기타 파일들의 경우 jekyll serve를 Ctrl + C로 중지시키고 다시 실행해야 반영된다.
