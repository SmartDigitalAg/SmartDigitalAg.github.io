## 스마트디지털농업연구실 웹페이지

### 🚀실행방법

>bundle exec jekyll serve

### 📰 News 페이지에 Post 추가 방법
1. `_posts` 폴더에 `.md` 파일을 생성합니다.
2. 파일 이름 형식은 `YYYY-MM-DD-title.md`로 설정해야 합니다. (예: `2026-01-01-2026년.md`)
3. post에 사용할 이미지는 `assets/img/news` 폴더에 정리합니다.

### 👥 인원 수정 방법
1. `_data/sitetext.yml` 파일에서 인원 정보를 수정합니다.
2. `number_educ` 필드를 통해 다음과 같이 구분합니다.
    - `1`: 교수님
    - `2`: 박사님
    - `4`: 석사 과정
    - `5`: 학부 연구생
    - `6`: 스태프
    - `7`: 졸업생
3. 인원의 이미지는 `assets/img/team` 폴더에 정리합니다.

### 🔗 Links 페이지에 항목 추가 방법
1. `_data/sitetext.yml` 파일에서 `links > items` 아래에 링크 항목을 추가합니다.
2. 각 항목은 아래 4개의 필드를 포함해야 합니다.
    - `title`: 영어 제목
    - `text`: 한글 제목
    - `url`: 프로그램 주소(url)
    - `image`: 대표 이미지 경로
3. 대표 이미지는 `assets/img/links` 폴더에 정리합니다.