# 🎤 AAFES 일일 조회 시스템

**Army & Air Force Exchange Service Daily Briefing System**

> Family Serving Family | We Go Where You Go

## 🌟 주요 기능

### ✅ AAFES 공식 컨텐츠
- **Mission**: "We go where you go to improve the quality of your lives"
- **Core Values**: Family Serving Family, Respect Everyone, Courage to Use Good Judgment
- **Motto**: "We Go Where You Go"

### ✅ 핵심 기능
- 🌐 **이중 언어**: 한국어 ↔ English 전환
- 🎙️ **음성 읽기**: Web Speech API를 통한 TTS
- 📝 **조회 작성**: AAFES 가치 기반 인사말 및 포커스
- 🔑 **키워드 관리**: 업무 분야별 키워드 추가
- 📚 **히스토리**: 조회 기록 저장 및 불러오기
- 📱 **PWA**: 앱으로 설치 가능
- ⚡ **오프라인 지원**: Service Worker를 통한 오프라인 작동

### ✅ AAFES 업무 키워드
- Customer Service Excellence (고객 서비스 우수성)
- Safety First (안전 제일)
- Teamwork (팀워크)
- Quality Control (품질 관리)
- Supporting Military Families (군인 가족 지원)
- Inventory Management (재고 관리)
- Store Cleanliness (매장 청결)
- Staff Training (직원 교육)
- Communication (커뮤니케이션)

## 🚀 사용 방법

### 로컬 테스트
```bash
cd "Daily briefing"
python3 -m http.server 8000
```
브라우저에서 `http://localhost:8000` 접속

### GitHub Pages 배포
`README-GitHub배포가이드.md` 파일을 참고하세요.

## 📱 설치

### Android
1. Chrome에서 사이트 접속
2. 메뉴(⋮) → "앱 설치" 선택
3. 홈 화면에서 앱 실행

### iOS
1. Safari에서 사이트 접속
2. 공유 버튼(□↑) → "홈 화면에 추가"
3. 홈 화면에서 앱 실행

## 📂 파일 구조
```
Daily briefing/
├── index.html              # 메인 HTML 파일
├── manifest.json           # PWA manifest
├── service-worker.js       # Service Worker
├── create-icons.html       # 아이콘 생성 도구
├── icons/
│   ├── icon-192.png       # 작은 아이콘
│   └── icon-512.png       # 큰 아이콘
├── README.md              # 이 파일
└── README-GitHub배포가이드.md
```

## 🛠️ 기술 스택
- HTML5
- CSS3 (Flexbox, Grid)
- JavaScript (ES6+)
- Web Speech API
- Service Worker API
- LocalStorage API
- PWA (Progressive Web App)

## 📝 라이선스
MIT License

## 👤 제작
Claude AI + Han

## 📅 버전
v1.0 - 2026.02.09

---

**🔗 GitHub Pages**: `https://[username].github.io/aafes-briefing/`
