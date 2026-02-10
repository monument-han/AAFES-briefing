# 🚀 AAFES 일일 조회 시스템 - GitHub Pages 배포 가이드

## 📋 목차
1. [준비물](#준비물)
2. [Step 1: 아이콘 생성](#step-1-아이콘-생성)
3. [Step 2: GitHub Repository 생성](#step-2-github-repository-생성)
4. [Step 3: 파일 업로드](#step-3-파일-업로드)
5. [Step 4: GitHub Pages 활성화](#step-4-github-pages-활성화)
6. [Step 5: 접속 및 설치](#step-5-접속-및-설치)
7. [문제 해결](#문제-해결)

---

## 준비물
- ✅ Google 계정 (GitHub 로그인에 사용)
- ✅ 이 폴더의 모든 파일
- ✅ Chrome 브라우저 (데스크탑 또는 모바일)

---

## Step 1: 아이콘 생성

### 1-1. 아이콘 생성 페이지 열기
1. `create-icons.html` 파일을 Chrome에서 열기
2. "192x192 아이콘 생성" 버튼 클릭 → `icon-192.png` 다운로드
3. "512x512 아이콘 생성" 버튼 클릭 → `icon-512.png` 다운로드

### 1-2. 아이콘 파일 이동
1. 다운로드한 두 개의 PNG 파일을 `icons` 폴더로 이동
2. 폴더 구조 확인:
```
Daily briefing/
├── index.html
├── manifest.json
├── service-worker.js
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── README-GitHub배포가이드.md
```

---

## Step 2: GitHub Repository 생성

### 2-1. GitHub 접속
1. https://github.com 접속
2. 오른쪽 상단 "Sign in" 클릭
3. Google 계정으로 로그인

### 2-2. 새 Repository 만들기
1. 로그인 후 오른쪽 상단 "+" 버튼 → "New repository" 클릭
2. 다음 정보 입력:
   - **Repository name**: `aafes-briefing` (원하는 이름으로 변경 가능)
   - **Description**: `AAFES Daily Briefing System`
   - **Public** 선택 (무료 GitHub Pages는 Public만 가능)
   - **Add a README file** 체크하지 않음
3. "Create repository" 클릭

---

## Step 3: 파일 업로드

### 3-1. 파일 업로드 방법 1 (웹 인터페이스 - 추천)
1. 새로 생성된 repository 페이지에서 "uploading an existing file" 링크 클릭
2. 다음 파일들을 드래그 앤 드롭:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
3. "Commit changes" 버튼 클릭

4. 다시 repository 메인 페이지로 이동
5. "Add file" → "Create new file" 클릭
6. 파일명에 `icons/icon-192.png` 입력 (폴더가 자동 생성됨)
7. 하단에 "Attach files by dragging & dropping..." 영역에 `icon-192.png` 드롭
8. "Commit new file" 클릭

9. 같은 방법으로 `icons/icon-512.png` 업로드

### 3-2. 파일 업로드 방법 2 (GitHub Desktop - 옵션)
1. GitHub Desktop 앱 다운로드 및 설치
2. Repository를 로컬로 클론
3. 모든 파일을 폴더에 복사
4. Commit 후 Push

---

## Step 4: GitHub Pages 활성화

### 4-1. Settings 접속
1. Repository 페이지 상단 "Settings" 탭 클릭
2. 왼쪽 메뉴에서 "Pages" 클릭

### 4-2. Pages 설정
1. **Source** 섹션에서:
   - Branch: `main` (또는 `master`) 선택
   - Folder: `/ (root)` 선택
2. "Save" 버튼 클릭

### 4-3. 배포 완료 대기
1. 페이지 상단에 파란색 알림이 표시됨:
   ```
   Your site is ready to be published at https://[username].github.io/aafes-briefing/
   ```
2. 1-2분 후 초록색으로 변경되면 배포 완료:
   ```
   ✅ Your site is published at https://[username].github.io/aafes-briefing/
   ```

---

## Step 5: 접속 및 설치

### 5-1. 웹 사이트 접속
1. 브라우저에서 `https://[username].github.io/aafes-briefing/` 접속
   - `[username]`을 본인의 GitHub 사용자명으로 변경
2. 앱이 정상적으로 로드되는지 확인

### 5-2. 모바일에서 PWA 설치 (Android)
1. 휴대폰 Chrome에서 위 URL 접속
2. 주소창 오른쪽 메뉴(⋮) → "앱 설치" 또는 "홈 화면에 추가" 선택
3. 설치 완료!

### 5-3. 모바일에서 PWA 설치 (iPhone)
1. 휴대폰 Safari에서 위 URL 접속
2. 하단 공유 버튼(□↑) → "홈 화면에 추가" 선택
3. 설치 완료!

---

## 문제 해결

### Q1: 404 Error가 발생해요
**A:** GitHub Pages 활성화 후 1-2분 기다려야 합니다. 시간이 지나도 안 되면:
1. Repository Settings → Pages에서 Branch가 올바르게 설정되었는지 확인
2. `index.html` 파일이 루트 폴더에 있는지 확인

### Q2: 아이콘이 표시되지 않아요
**A:**
1. `icons` 폴더 안에 `icon-192.png`와 `icon-512.png`가 있는지 확인
2. 파일명이 정확히 일치하는지 확인 (대소문자 구분)

### Q3: 음성이 작동하지 않아요
**A:**
1. HTTPS 연결인지 확인 (GitHub Pages는 자동으로 HTTPS 제공)
2. 브라우저에서 마이크 권한이 차단되지 않았는지 확인
3. 음성 선택 드롭다운에서 다른 음성 선택

### Q4: 날씨가 자동으로 로드되지 않아요
**A:**
1. 정상입니다! 날씨는 수동으로 입력하거나
2. `index.html` 파일의 `fetchWeather()` 함수에서 도시 이름을 변경할 수 있습니다

### Q5: 앱을 업데이트하려면?
**A:**
1. GitHub repository에서 파일을 수정하거나
2. 새 파일을 업로드하면
3. 자동으로 웹사이트에 반영됩니다 (1-2분 소요)

---

## 🎉 완료!

이제 노트북 없이 언제 어디서나 휴대폰만으로 AAFES 일일 조회를 사용할 수 있습니다!

**접속 URL**: `https://[username].github.io/aafes-briefing/`

### 주요 기능
- ✅ 한국어/English 전환
- ✅ AAFES 공식 모토 및 가치 포함
- ✅ 음성 읽기 (TTS)
- ✅ 조회 히스토리 저장
- ✅ PWA 설치 가능
- ✅ 오프라인 지원
- ✅ 완전 무료, 24시간 가동

---

## 📞 추가 도움말

- GitHub 공식 가이드: https://pages.github.com
- PWA 설치 방법: https://support.google.com/chrome/answer/9658361

**제작**: Claude AI + Han
**버전**: 1.0
**날짜**: 2026년 2월
