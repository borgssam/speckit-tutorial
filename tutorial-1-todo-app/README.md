# Tutorial 1: 기초편 - ToDo 앱

## 목표

spec-kit의 기본적인 워크플로우를 이해하고, 심플한 ToDo 리스트 애플리케이션을 사양 정의부터 구현까지 완성합니다.

## 소요 시간

약 30분

## 학습 내용

* spec-kit의 기본 명령어
* 사양 기반 개발의 기본 흐름
* Constitution → Specify → Plan → Tasks → Implement의 사이클

## Step 1: 프로젝트 초기화

먼저 spec-kit 프로젝트를 초기화합니다.

```bash
cd tutorial-1-todo-app
specify init todo-app --ai claude

```

이 명령어는 `.speckit/` 디렉토리를 생성하며, 이후 spec-kit의 슬래시 명령어를 사용할 수 있게 됩니다.

## Step 2: Constitution (헌법) 작성

프로젝트의 원칙과 제약을 정의합니다. Claude Code 또는 Cursor 등의 AI 에이전트에서 아래 명령어를 실행해 주세요.

```
/speckit.constitution

```

아래 내용을 포함하도록 지시합니다:

**지시 예시**:

```
ToDo 앱의 개발 원칙을 정의해 주세요:
- 심플하고 직관적인 UI
- 데이터는 로컬 스토리지(LocalStorage)에 저장
- 바닐라 자바스크립트 (프레임워크 미사용)
- 반응형 디자인
- 웹 접근성 고려

```

생성되는 파일: `.speckit/constitution.md`

### 확인 포인트

* [ ] `.speckit/constitution.md` 파일이 생성되었는가
* [ ] 프로젝트의 원칙이 명확하게 기재되어 있는가
* [ ] 기술적 제약 사항이 정의되어 있는가

## Step 3: Specification (사양) 작성

기능 요구사항을 정의합니다.

```
/speckit.specify

```

**지시 예시**:

```
ToDo 리스트 앱의 기능 사양을 정의해 주세요:

필수 기능:
1. ToDo 아이템 추가
2. ToDo 아이템 완료/미완료 상태 전환
3. ToDo 아이템 삭제
4. ToDo 리스트 표시
5. 완료된 아이템 필터링

사용자 스토리:
- 사용자로서 새로운 태스크를 추가할 수 있다
- 사용자로서 태스크를 완료 상태로 표시할 수 있다
- 사용자로서 불필요한 태스크를 삭제할 수 있다
- 사용자로서 전체/미완료/완료된 태스크를 필터링하여 볼 수 있다

```

생성되는 파일: `.speckit/specifications/todo-app.md`

### 확인 포인트

* [ ] 기능 요구사항이 명확하게 정의되어 있는가
* [ ] 사용자 스토리가 포함되어 있는가
* [ ] 인수 조건(Acceptance Criteria)이 기재되어 있는가

## Step 4: Plan (계획) 작성

기술적인 구현 계획을 세웁니다.

```
/speckit.plan

```

**지시 예시**:

```
ToDo 앱의 기술 구현 계획을 작성해 주세요:

고려 사항:
- HTML 파일 구조
- CSS 스타일링 방향성
- JavaScript 데이터 관리 방식
- LocalStorage 활용 방법
- 이벤트 핸들링 구조

```

생성되는 파일: `.speckit/plans/todo-app-implementation.md`

### 확인 포인트

* [ ] 파일 구조가 정의되어 있는가
* [ ] 데이터 모델이 명확한가
* [ ] 구현 접근 방식이 기재되어 있는가

## Step 5: Tasks (태스크) 생성

구현 가능한 단위로 태스크를 분해합니다.

```
/speckit.tasks

```

생성되는 파일: `.speckit/tasks/todo-app-tasks.md`

### 예상되는 태스크 예시

1. HTML 기본 구조 작성
2. CSS 스타일 구현
3. ToDo 아이템 데이터 모델 정의
4. LocalStorage 연동 로직 구현
5. 아이템 추가 기능 구현
6. 아이템 삭제 기능 구현
7. 완료 상태 토글 기능 구현
8. 필터링 기능 구현

### 확인 포인트

* [ ] 태스크가 적절한 크기(粒度)로 분해되어 있는가
* [ ] 태스크에 우선순위가 매겨져 있는가
* [ ] 각 태스크가 즉시 구현 가능한 단위인가

## Step 6: Implement (구현)

태스크를 하나씩 차례대로 구현해 나갑니다.

```
/speckit.implement

```

**지시 예시**:

```
todo-app-tasks.md의 태스크를 순서대로 구현해 주세요

```

생성되는 파일:

* `index.html` - 메인 HTML 파일
* `styles.css` - 스타일시트
* `app.js` - 애플리케이션 로직

### 확인 포인트

* [ ] 모든 파일이 정상적으로 생성되었는가
* [ ] 사양서에서 정의한 기능이 모두 구현되었는가
* [ ] 코드가 constitution(헌법)의 원칙을 따르고 있는가

## Step 7: 동작 확인

브라우저에서 애플리케이션을 열어 동작을 확인합니다.

```bash
# 심플한 HTTP 서버 실행
python3 -m http.server 8000
# 또는
npx serve .

```

브라우저에서 `http://localhost:8000` 주소로 접속합니다.

### 동작 확인 체크리스트

* [ ] ToDo 아이템을 추가할 수 있는가
* [ ] 아이템을 완료 상태로 변경할 수 있는가
* [ ] 아이템을 삭제할 수 있는가
* [ ] 필터링 기능이 정상적으로 동작하는가
* [ ] 페이지를 새로고침해도 데이터가 유지되는가

## Step 8: Clarify (명확화) - 옵션

사양이 불분명한 부분이 있다면 명확하게 정의합니다.

```
/speckit.clarify

```

**사용 예시**:

```
아래 내용들을 명확하게 정의해 주세요:
- ToDo 아이템의 최대 글자 수 제한은?
- 수정(편집) 기능이 필요한가?
- 우선순위 설정 기능이 필요한가?

```

## 배운 내용

본 튜토리얼을 통해 다음 내용을 학습했습니다:

1. **Constitution**: 프로젝트 원칙 및 제약 사항 정의
2. **Specify**: 기능 요구사항 및 사용자 스토리 작성
3. **Plan**: 기술적인 구현 계획 수립
4. **Tasks**: 구현 가능한 단위로 태스크 분해
5. **Implement**: 사양에 기반한 코드 구현
6. **Clarify**: 모호한 사양 명확화 (옵션)

## 다음 단계

Tutorial 2로 이동하여 조금 더 복잡한 RESTful API 서비스 개발 방법을 배워보세요.

## 트러블슈팅

### spec-kit 명령어를 찾을 수 없는 경우

```bash
# spec-kit 재설치
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git

```

### 슬래시 명령어가 동작하지 않는 경우

* Claude Code 또는 Cursor 등의 AI 에이전트 환경 내부에서 실행했는지 확인해 주세요.
* 프로젝트 디렉토리에 `.speckit/` 폴더가 정상적으로 존재하는지 확인해 주세요.

### 생성된 코드가 예상과 다른 경우

* `/speckit.clarify`를 사용하여 사양을 더 명확하게 다듬어 보세요.
* constitution이나 specification 파일을 검토하여 요구사항을 더 자세하게 보완해 보세요.
