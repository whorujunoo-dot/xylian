# 자일리앤 입냄새 관리 앱

## 파일 구성

배포에 필요한 파일을 **전부 한 번에** 업로드해야 한다.

| 파일명 | 용도 | 필수 |
|---|---|---|
| `index.html` | GitHub Pages 메인 페이지 | ✅ |
| `manifest.json` | PWA 설정 | ✅ |
| `favicon.ico` | 브라우저 탭 아이콘 | ✅ |
| `icon-16.png` | 브라우저 탭 | ✅ |
| `icon-32.png` | 브라우저 탭 | ✅ |
| `icon-180.png` | iOS 홈 화면 아이콘 | ✅ |
| `icon-192.png` | Android PWA 아이콘 | ✅ |
| `icon-512.png` | Android PWA 스플래시 | ✅ |
| `xylian-app.html` | 로컬 테스트용 복사본 | ❌ |

---

## GitHub Pages 배포 4단계

### 1. 저장소 만들기
1. https://github.com 로그인
2. 우상단 `+` → `New repository`
3. Repository name: `xylian`
4. **Public** 선택
5. `Create repository`

### 2. 파일 업로드
1. `Add file` → `Upload files`
2. 아래 파일 전부 드래그 앤 드롭:
   - index.html
   - manifest.json
   - favicon.ico
   - icon-16.png, icon-32.png, icon-180.png, icon-192.png, icon-512.png
3. `Commit changes`

### 3. Pages 활성화
1. `Settings` 탭 → 왼쪽 `Pages`
2. Source: Branch `main`, Folder `/ (root)`, `Save`
3. 1~2분 대기

### 4. URL 확인
```
https://(내_깃허브_아이디).github.io/xylian/
```
이 URL을 QR코드로 만들어 제품 패키지/상페에 첨부.

---

## 사용자용: 모바일 홈 화면에 추가

**iPhone (Safari)**
1. 배포 URL 접속
2. 하단 공유 버튼 → "홈 화면에 추가"

**Android (Chrome)**
1. 배포 URL 접속
2. 우상단 ⋮ → "홈 화면에 추가" 또는 "앱 설치"

추가 후 앱처럼 전체화면 실행된다.

---

## 파일 수정 방법

저장소에서 파일 클릭 → 연필 아이콘 → 수정 → `Commit changes`. 1분 내 반영.

---

## 재구매 링크

현재 설정:
```
https://m.site.naver.com/2510B
```

변경은 `index.html`의 `openStore()` 함수에서 URL만 교체.

---

## 기능 요약

- 📅 **날짜 수동 선택** — 홈 화면 상단에서 과거 날짜 기록 가능
- **기록 탭 클릭 편집** — 항목 누르면 해당 날짜로 이동
- **체크리스트** — 복용 + 양치 3회
- **슬라이더** — 냄새/자신감 1~10점
- **통계** — 주간/월간 라인+바 차트
- **백업/복원** — JSON
- **재구매/공유 배너** — 모든 화면에 고정
- **로컬 저장** — 서버 불필요
