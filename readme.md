## 스마트디지털농업연구실 웹페이지

### 🧭 사이트 구조
- `_data/` : 사이트 내용 (인원, 논문, 수상, 연구 분야, 링크 등)
- `_posts/` : News 게시글
- `assets/img/` : 이미지
- `news.html`, `team.html` 등 : 각 페이지
- `_includes/`, `_layouts/` : 페이지 틀
- `.github/workflows/sync-sheets.yml` : 구글 시트를 `_data/presentations.csv`로 가져오는 자동 작업
- `_site/` : 빌드 결과물. 직접 수정하지 않습니다.

`main` 브랜치에 push하면 GitHub Pages가 자동으로 빌드해서 배포합니다.
구글 시트 내용은 매일 한 번 자동 작업이 가져와서 커밋하고, 이 커밋으로 다시 배포됩니다.

GitHub은 로컬과 다른 버전의 Jekyll(3.x)로 빌드합니다. 로컬에서는 되는데 사이트에 반영되지 않으면 `Actions` 탭의 `pages build and deployment`에서 오류를 확인합니다.

### 📍 수정할 곳 찾기

| 수정할 내용 | 위치 |
|---|---|
| 메인 슬라이드 사진 | `assets/img/header-carousel/` |
| 메인 사진 위 문구 | `_data/sitetext.yml`의 `header` |
| 메인 News, Publications 목록 | 수상, 논문 데이터에서 최신 5건을 자동으로 가져옵니다 |
| 상단 메뉴 | `_data/navigation.yml` |
| News 수상 목록 (학술발표) | 구글 시트 |
| News 수상 목록 (경진대회, 개인 수상) | `_data/awards_manual.yml` |
| 학회 이름 표기 | `_data/venues.yml` |
| News 게시글 | `_posts/` |
| 논문 | `_data/publications.csv` |
| 인원 | `_data/sitetext.yml`의 `team` |
| Research 연구 분야 | `_data/sitetext.yml`의 `research` |
| Links | `_data/sitetext.yml`의 `links` |
| 하단 문구 | `_includes/footer.html` |
| 사이트 제목, 기본 설정 | `_config.yml` |

### 🚀 실행방법

처음 한 번
1. Ruby 3.x를 설치합니다. Windows는 [RubyInstaller](https://rubyinstaller.org/downloads/)에서 Ruby+Devkit 버전을 받고, 설치 마지막의 `ridk install`까지 진행합니다.
2. 저장소 폴더에서 `bundle install`을 실행합니다.

수정할 때
1. `bundle exec jekyll serve`를 실행합니다.
2. 브라우저에서 `http://localhost:4000`을 엽니다.
3. 파일을 저장하면 자동으로 다시 빌드됩니다. `_config.yml`을 수정했을 때는 `Ctrl+C`로 끄고 다시 실행합니다.
4. 확인이 끝나면 커밋하고 `main` 브랜치에 push합니다.

### 🖼️ 메인 슬라이드 사진 교체 방법
1. `assets/img/header-carousel` 폴더에 사진을 넣거나 뺍니다.
2. 사진은 파일 이름 순서대로 5초마다 넘어갑니다. (예: `main1.jpg`, `main2.jpg`)
3. 사진 위 문구는 `_data/sitetext.yml`의 `header`에서 수정합니다.

### 📰 News 게시글 추가 방법
1. `_posts` 폴더에 `.md` 파일을 생성합니다.
2. 파일 이름 형식은 `YYYY-MM-DD-title.md`로 설정해야 합니다. (예: `2026-01-01-2026년.md`)
3. 파일 맨 위 설정에 `categories: news`를 적습니다. (기존 게시글 참고)
4. post에 사용할 이미지는 `assets/img/news` 폴더에 정리합니다.

게시글 목록은 `/posts.html`에 표시됩니다. News 페이지의 수상 목록은 게시글이 아니라 아래의 구글 시트와 `awards_manual.yml`로 만들어집니다.

### 🏆 학술발표와 수상 내역 수정 방법
학술발표와 수상 내역은 구글 시트에서 관리합니다.

1. [학술발표목록 시트](https://docs.google.com/spreadsheets/d/1ACLVJ368WL_rCHME4QSjUWlzEWsfSFPV0ayyamyYcU8/edit)에 한 줄을 추가합니다.
2. 매일 한 번 자동으로 사이트에 반영됩니다. 바로 반영하려면 GitHub 저장소의 `Actions` 탭에서 `Sync Google Sheets`를 선택하고 `Run workflow`를 누릅니다.

시트 작성 규칙
- `비고` 칸에 상 이름을 적은 행만 News 페이지의 수상 목록에 표시됩니다.
- `주저자`가 비어 있거나 `-`인 행은 수상 목록에 표시되지 않습니다.
- `학회`는 약칭으로 적어도 됩니다. 사이트에는 정식명칭으로 표시됩니다. (예: `농공학회`는 `한국농공학회`로 표시) 규칙에 맞지 않는 학회는 `_data/venues.yml`에 적습니다.
- `국문 제목`이 비어 있거나 `-`이면 `영문 제목`이 표시됩니다.
- 언론 보도가 있으면 `뉴스 기사1`, `뉴스 기사2` 칸에 주소를 그대로 붙여넣습니다. 셀에 하이퍼링크를 거는 방식은 사용하지 않습니다.
- `연도`는 네 자리 숫자로 적습니다.

열 이름이 바뀌었거나 `연도`, `주저자`, `학회`가 빈 행이 있으면 반영되지 않고 사이트는 이전 상태로 남습니다. 실패 여부는 `Actions` 탭에서 확인합니다.

### 🥇 경진대회와 개인 수상 추가 방법
학술발표가 아닌 수상(창업 경진대회, 아이디어 대회, 교수 개인 수상 등)은 `_data/awards_manual.yml`에 추가합니다.

```yaml
- year: "2025"
  season: 추계                           # 춘계/하계/추계/동계 (같은 연도 안 정렬용)
  who: 정재영·석승원·장은수              # 여러 명이면 가운뎃점(·)으로 연결
  title: 저수지 운영 인공지능 모델 개발     # 없으면 생략 가능
  venue: KSAE AX-Water Challenge 2025
  award: 대상(농림축산식품부 장관상)
  detail: /news/ksae-ax-water-2025/      # 상세 페이지가 있으면 (선택)
  links:                                 # 언론 보도가 있으면 (선택)
    - https://example.com/article
```

시트에서 가져온 수상 내역과 합쳐져 최신순으로 표시됩니다. 같은 연도 안에서는 시즌(동계→추계→하계→춘계) 순서로, 같은 시즌 안에서는 시트의 아래쪽 행(최근에 추가한 행)이 먼저, 그 다음 이 파일의 항목이 위에서부터 나옵니다. 새 항목은 파일 맨 위에 추가합니다.

### 📄 논문 추가 방법
`_data/publications.csv`에 한 줄을 추가합니다.

| 열 | 설명 | 예시 |
|---|---|---|
| `year` | 게재 연도 | `2026` |
| `title` | 논문 제목 | |
| `authors` | 전체 저자. 쉼표로 구분 | `석승원, 박혜성, 김태곤` |
| `journal` | 학술지명 | `생물환경조절학회지` |
| `volume` | 권(호). 없으면 비움 | `35(1)` |
| `pages` | 페이지. 없으면 비움 | `26-39` |
| `lang` | 제목 언어 (`ko` / `en`) | `ko` |

- 연구실 구성원 이름은 굵게 표시됩니다. `_data/sitetext.yml`의 인원 정보(`name` / `kor_name`)에 있는 이름만 해당합니다.
- 영문 제목 논문은 저자를 영문(`Taegon Kim`)으로, 국문 제목 논문은 한글(`김태곤`)로 적습니다.
- 제목이나 저자에 쉼표가 있으면 값 전체를 큰따옴표로 감쌉니다. (예: `"사회, 경제, 환경 영향 비교"`)
- 첫 줄(열 이름)은 수정하지 않습니다.

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
4. 여기에 등록된 이름(`name` / `kor_name`)이 논문 저자를 굵게 표시하는 기준으로 쓰입니다.

### 🔬 Research 페이지 수정 방법
1. `_data/sitetext.yml` 파일의 `research > fields` 아래에서 연구 분야를 수정합니다.
2. 각 항목은 아래 4개의 필드를 포함해야 합니다.
    - `title`: 분야 제목
    - `desc`: 설명
    - `image`: 대표 이미지 경로
    - `alt`: 대체 텍스트
3. 대표 이미지는 `assets/img/focus` 폴더에 정리합니다.
4. 이미지 파일 이름을 바꾸면 `image` 경로도 같이 수정합니다.

### 🔗 Links 페이지에 항목 추가 방법
1. `_data/sitetext.yml` 파일에서 `links > items` 아래에 링크 항목을 추가합니다.
2. 각 항목은 아래 4개의 필드를 포함해야 합니다.
    - `title`: 영어 제목
    - `text`: 한글 제목
    - `url`: 프로그램 주소(url)
    - `image`: 대표 이미지 경로
3. 대표 이미지는 `assets/img/links` 폴더에 정리합니다.
