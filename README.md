# 태권도 통합 관리 (배포용)

이 저장소는 앱 화면 파일을 올려 두는 곳입니다. 여기서 직접 고치지 마세요.
원본은 https://github.com/gyeoltaro/gyeoltaro 의 `claude/wonderful-turing-qwjqzr` 브랜치 `www/` 폴더이고, `node tools/deploy.mjs` 로 올립니다.

`push-server/` 는 앱 푸시를 보내는 서버 프로그램(Firebase Cloud Functions)이에요. 각 도장이 자기 Firebase 프로젝트에 설치합니다.

```bash
cd push-server
npm --prefix functions install
npx firebase-tools login
npx firebase-tools deploy --only functions --project 프로젝트ID
```

마지막 배포: 84303a1
