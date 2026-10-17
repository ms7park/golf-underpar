# CLAUDE.md - golf-underpar Workspace Guide

## 📌 Project Overview
- **Project Name**: `golf-underpar`
- **Description**: 싱글 핸디캡 달성을 위한 개인 골프 레슨 일지, 스윙 분석, 클럽별 스탯 및 필드/파3 가이드 웹 애플리케이션
- **Tech Stack**: HTML5, Tailwind CSS, Vanilla JavaScript, Vercel Deployment

---

## ⚡ Execution & Permissions (Auto-Approve)
- **No Confirmation Prompts**: All file creations (`write_to_file`), edits (`replace_file_content`), and non-destructive terminal commands should execute automatically without asking the user for confirmation.
- Mode is set to `accept-edits` / `auto`.

---

## 🛠️ Code & Content Guidelines
1. **Single Page Architecture**:
   - `index.html`은 HTML, Tailwind CSS, Vanilla JS를 일관성 있게 유지합니다.
   - Par3 가이드 등 독립 서브페이지는 `par3/index.html` 등 모듈형 구조를 따릅니다.
2. **Data Consistency**:
   - `docs/` 하위의 원본 텍스트 데이터(`docs/lesson/`, `docs/practice/`, `docs/fieldnotes/`, `docs/par3-practice/`, `docs/main.txt`)와 웹페이지 내용이 항상 일치하도록 동기화합니다.
3. **Change Log Maintenance**:
   - 중요한 변경 사항은 항상 [HELP](file:///Users/user/CursorProjects/golf-underpar/HELP) 파일 하단에 작업 날짜와 내용을 기록합니다.
