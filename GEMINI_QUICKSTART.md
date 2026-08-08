# Gemini Code Assist 빠른 시작 가이드

## ✅ 설치 완료!

VS Code에 **Gemini Code Assist** (`google.geminicodeassist`)가 설치되었습니다.

---

## 🚀 지금 바로 시작하기

### 1단계: 인증 (첫 실행 시 **필수**)
```
Command Palette (Cmd+Shift+P) → "Gemini: Sign in"
↓
Google 계정으로 로그인 → 권한 승인
```

### 2단계: 테스트해보기
- [test-gemini.js](test-gemini.js) 파일 열기
- 각 섹션의 주석을 따라 Gemini 기능 체험

### 3단계: 자신의 코드에 사용
- **Code Assist**: 코드 작성 중 자동 제안 기다리기 (Tab으로 승인)
- **Chat**: Cmd+Shift+P → `Gemini: Open Chat` → 질문하기
- **명령어**: 코드 선택 후 우클릭 또는 Command Palette에서 선택

---

## 📚 주요 사용 방법

| 기능 | 방법 |
|------|------|
| **채팅** | Cmd+Shift+P → "Gemini: Open Chat" |
| **코드 설명** | 코드 선택 → "Gemini: Explain" |
| **버그 수정** | 코드 선택 → "Gemini: Fix" |
| **테스트 생성** | 함수 선택 → "Gemini: Generate Tests" |
| **문제 해결** | 터미널 에러 → "Gemini: Explain Terminal Command" |
| **자동 완성** | 코드 입력 중 제안 나타나면 Tab/Enter |

---

## 🎯 실무 활용 팁

1. **복잡한 함수 설명받기**
   ```javascript
   // 아래 함수를 선택하고 "Gemini: Explain" 실행
   function complexAlgorithm() { ... }
   ```

2. **리팩토링 요청**
   - 코드 선택 → Chat 열기 → "이 코드 리팩토링해줄래?"

3. **테스트 자동 생성**
   - 함수 선택 → "Gemini: Generate Tests"

4. **정규식 설명 받기**
   - 정규식 선택 → "Gemini: Explain"

---

## 🔧 자주 묻는 질문 (FAQ)

**Q: 로그인이 안 됩니다**
- A: Command Palette → "Gemini: Reset Authentication" → 다시 로그인

**Q: 제안이 안 나타납니다**
- A: 
  1. 설정에서 Gemini 활성화 확인 (Cmd+, → "gemini")
  2. VS Code 재시작
  3. 구글 계정 로그인 확인

**Q: 오프라인에서도 사용 가능한가요?**
- A: 아니요, 온라인 연결 필수 (Google 서버와 통신)

**Q: 무료인가요?**
- A: Google AI Studio의 Free Tier 사용 (월 할당량 제한)
  - [가격 정보](https://ai.google.dev/pricing)

---

## 📖 더 알아보기

- [GEMINI_SETUP.md](GEMINI_SETUP.md) - 상세 설정 가이드
- [test-gemini.js](test-gemini.js) - 테스트 코드 예제
- [Google Gemini 공식 문서](https://ai.google.dev/)

---

**설정이 완료되었습니다! 이제 Gemini와 함께 더 빠르게 코딩하세요! 🚀**
