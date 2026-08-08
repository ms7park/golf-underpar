# Gemini Code Assist 설정 가이드

## 1. 설치 완료 ✅
- 확장: `google.geminicodeassist` 설치됨

## 2. Google 계정 로그인 및 API 인증

### 방법 A: 자동 인증 (권장)
1. VS Code를 열고 **Command Palette** 실행 (`Cmd+Shift+P`)
2. `Gemini Code Assist: Sign in` 검색 및 실행
3. Google 계정으로 로그인
4. 요청된 권한 승인

### 방법 B: Google Cloud 콘솔에서 API 키 생성
1. [Google AI Studio](https://aistudio.google.com/apikey) 방문
2. "Get API key" 클릭하여 새 API 키 생성
3. VS Code의 Gemini 설정에서 API 키 입력:
   - Settings: `Cmd+,` → "gemini" 검색
   - "Gemini: API Key" 필드에 키 입력

## 3. 매크로 사용 방법

### 채팅
- **Command Palette** → `Gemini: Open Chat` 또는 측면바 Gemini 아이콘 클릭

### 인라인 코드 완성
- 코드를 작성하면 자동으로 제안 표시
- `Tab` 또는 `Enter`로 승인

### 코드 선택 후 작업
1. 코드 블록 선택
2. **Command Palette** → `Gemini: Generate`, `Gemini: Fix`, `Gemini: Explain` 등 사용

### 터미널 헬퍼
- **Command Palette** → `Gemini: Explain Terminal Command`
- 터미널의 에러 메시지 설명 받기

## 4. 주요 단축키

| 작업 | 단축키 |
|------|--------|
| Chat 열기 | `Cmd+Shift+G` (기본값 설정 시) |
| 선택 코드 설명 | Command Palette 사용 |
| 버그 수정 제안 | Command Palette → "Fix" |
| 단위 테스트 생성 | Command Palette → "Generate Tests" |

## 5. 설정 커스터마이징 (선택사항)

VS Code Settings (`Cmd+,`) → "Gemini" 검색:
- **Model**: 사용 모델 선택 (기본: Gemini 2.0 Flash)
- **Temperature**: 창의성 수준 (0-1)
- **Max Tokens**: 응답 길이 제한

## 6. 문제 해결

### 인증 실패
- "Reset Gemini authentication" 실행 후 다시 로그인
- Google 계정의 2단계 인증 확인

### API 할당량 초과
- [Google Cloud Console](https://console.cloud.google.com/apis/dashboard) 에서 할당량 확인
- 필요 시 유료 플랜 업그레이드

### 확장이 작동하지 않음
- VS Code 재시작: `Code > Quit VS Code` → 다시 실행
- 확장 활성화 확인: 확장 뷰에서 Gemini Code Assist 상태 확인

## 7. 다음 단계
- 샘플 코드로 테스트해보기
- 자주 사용할 명령어 찾기
- 팀 설정과 공유 (선택사항)

---

**더 자세한 정보**: [Google Gemini Code Assist 공식 문서](https://support.google.com/gemini/answer/13981801)
