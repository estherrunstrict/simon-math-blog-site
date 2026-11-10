# 시몬의 수학 작업실

**블로그:** https://estherrunstrict.github.io/simon-math-blog-site/

GitHub Pages가 Markdown 글을 정적 페이지로 만들고 직접 제공합니다.
독자에게 ITDO 서버, 데이터베이스, 로그인, AI 호출은 필요하지 않습니다.
`main`에 변경을 저장하면 GitHub의 Pages 빌드가 실행됩니다. 예약 작업은 없습니다.

## 새 글 쓰기

1. [`_templates/post.md`](./_templates/post.md)의 내용을 복사합니다.
2. **Add file → Create new file**을 눌러 `_posts/YYYY-MM-DD-my-story.md` 형식으로 파일을 만듭니다. 날짜와 `my-story`를 실제 날짜와 짧은 영문 제목으로 바꿉니다.
3. 제목, 날짜, 주제, 짧은 소개와 시몬이 직접 쓴 설명을 넣습니다.
4. 보호자가 공개할 내용을 확인한 뒤 `published: true`로 바꾸고 **Commit changes**로 `main`에 저장합니다.
5. **Actions → pages build and deployment**가 초록색으로 끝나면 블로그에서 확인합니다.

이 저장소는 공개입니다. 공개해도 되는 글과 사진만 올리세요. `published: false`는
블로그에서만 숨기며 저장소나 Git 기록을 비공개로 만들지 않습니다. 개인 초안은
로컬 파일에 보관하고, 확인한 글만 업로드합니다.

## 사진 넣기

보호자가 확인한 사진을 `assets/posts/`에 업로드하고 글에서 다음처럼 연결합니다.

```markdown
![직접 쓴 풀이]({{ '/assets/posts/my-working.jpg' | relative_url }})
```

사진 속 이름, 학교 등 공개하지 않을 정보는 업로드 전에 제거합니다.
다른 서버의 사진 주소를 연결할 필요가 없습니다.

## 수정하거나 내리기

- 수정: `_posts/`의 글을 고쳐 `main`에 저장합니다.
- 블로그에서 내리기: `published: false`로 바꾸거나 해당 글을 삭제하고 저장합니다.
- 사용하지 않는 사진도 삭제합니다. Pages 배포가 끝난 뒤 실제 주소를 확인합니다.
- 공개 저장소의 Git 기록이나 이미 내려받은 사본까지 삭제되는 것은 아닙니다.

## 운영

- Pages source: **Deploy from a branch → main → / (root)**.
- Jekyll이 `_config.yml`, `_layouts/`, `_posts/`를 빌드합니다.
- `_templates/`와 README는 사이트에 배포하지 않습니다.
- 첫 배포에는 실제 글이 없습니다. 예시 글을 시몬의 작업처럼 표시하지 않습니다.
- 현재 디자인과 원도 이미지를 유지합니다. 원본 사진, 개인 학습 기록, 인증 정보,
  ITDO 서버 코드는 이 저장소에 포함하지 않습니다.
- 기존 `simon-math-blog` 비공개 저장소는 이전 ITDO 연동 코드의 보관용입니다.
  이 사이트는 그 저장소나 ITDO API를 실행하거나 동기화하지 않습니다.

기존 ITDO 앱의 공개 기능은 이 GitHub 블로그를 갱신하지 않습니다.
새 블로그의 글 작성과 공개는 위의 Markdown 절차를 사용합니다.

참고: [GitHub의 Jekyll 글 작성 안내](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll).
