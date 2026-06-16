# Spec-Kit 튜토리얼 가이드

spec-kit을 단계별로 배울 수 있는 3가지 튜토리얼 프로젝트입니다.

## 개요

spec-kit은 사양 기반 개발(Spec-Driven Development)을 실현하기 위한 툴킷입니다.
기존의 "코드를 먼저 작성하고 사양을 확인하는" 접근 방식 대신, "사양을 실행 가능하게 만들고 그로부터 코드를 생성하는" 접근 방식을 채택하고 있습니다.

## 전제 조건

```bash
# spec-kit 설치
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git

```

## 튜토리얼 구성

### Tutorial 1: 기초편 - ToDo 앱

**소요 시간**: 30분
**학습 내용**:

* spec-kit의 기본적인 워크플로우
* `/speckit.constitution` - 프로젝트 원칙 설정
* `/speckit.specify` - 요구사항 정의
* `/speckit.plan` - 기술 계획
* `/speckit.tasks` - 태스크 분해
* `/speckit.implement` - 구현

**프로젝트**: 심플한 ToDo 리스트 관리 앱

### Tutorial 2: 중급편 - RESTful API 서비스

**소요 시간**: 60분
**학습 내용**:

* 여러 사양 파일 관리
* `/speckit.clarify` - 사양 명확화
* `/speckit.analyze` - 일관성 체크
* 이터레이티브(반복적)한 사양 개선

**프로젝트**: 블로그 게시글 관리 RESTful API

### Tutorial 3: 응용편 - 마이크로서비스 연동

**소요 시간**: 90분
**학습 내용**:

* 복잡한 시스템 아키텍처의 사양화
* `/speckit.checklist` - 요구사항 완전성 검증
* 단계적인 구현 및 리팩토링
* 브라운필드(기존) 개발에 적용

**프로젝트**: 사용자 인증 및 데이터 서비스 연동 시스템

## 디렉토리 구조

```
speckit-tutorial/
├── README.md (이 파일)
├── tutorial-1-todo-app/
│   ├── README.md
│   ├── .speckit/
│   └── (생성되는 코드)
├── tutorial-2-api-service/
│   ├── README.md
│   ├── .speckit/
│   └── (생성되는 코드)
└── tutorial-3-microservices/
    ├── README.md
    ├── .speckit/
    └── (생성되는 코드)

```

## 권장 학습 순서

1. Tutorial 1부터 순서대로 진행하는 것을 권장합니다.
2. 각 튜토리얼은 독립되어 있지만, 이전 튜토리얼의 지식을 전제로 합니다.
3. 각 단계에서 생성된 산출물을 확인하며 이해를 넓혀가세요.

## 서포트

각 튜토리얼 디렉토리에 상세한 README.md가 있습니다.
스텝 바이 스텝으로 진행할 수 있도록 설계되어 있습니다.

## spec-kit 기본 워크플로우

```
1. Constitution (헌법) → 프로젝트 원칙 및 제약 정의
2. Specification (사양) → 무엇을 만들지 정의
3. Plan (계획) → 어떻게 만들지 정의
4. Tasks (태스크) → 구현 가능한 단위로 분해
5. Implement (구현) → 코드 생성 및 구현

```

이 사이클을 반복함으로써 고품질의 소프트웨어를 효율적으로 개발할 수 있습니다.

## 각 튜토리얼의 특징

### Tutorial 1: 기초 다지기

* spec-kit의 전체적인 워크플로우 체험
* 심플한 프로젝트를 통해 각 명령어의 역할 이해
* 사양에서 코드까지의 흐름을 실감
* **산출물**: 브라우저에서 동작하는 ToDo 앱

### Tutorial 2: 실전 스킬 습득

* 더욱 복잡한 백엔드 API 설계
* 여러 사양 파일을 관리하는 방법 학습
* 사양 명확화와 일관성 체크의 중요성 이해
* **산출물**: RESTful API 서버 (테스트 포함)

### Tutorial 3: 엔터프라이즈 레벨 개발

* 마이크로서비스 아키텍처 사양화
* 대규모 시스템 요구사항 관리
* 단계적인 구현 및 리팩토링
* 이벤트 기반 아키텍처 설계
* **산출물**: Docker Compose로 동작하는 마이크로서비스 시스템

## 학습 진행 방법

### 처음이신 분

1. **Tutorial 1**에서 기본 배우기 (필수)
2. **Tutorial 2**에서 실전 스킬 습득
3. 실제 소규모 프로젝트에서 spec-kit 시도해보기
4. **Tutorial 3**에서 엔터프라이즈 레벨 설계 배우기

### API 개발 경험자

* Tutorial 1은 가볍게 훑어봐도 OK
* **Tutorial 2**부터 본격적으로 시작
* Tutorial 3에서 마이크로서비스 설계 배우기

### 아키텍트・상급자

* Tutorial 1, 2는 참고 정도로 확인
* **Tutorial 3**에서 spec-kit을 사용한 대규모 시스템 설계 배우기
* 기존 프로젝트에 spec-kit 도입 검토

## 자주 묻는 질문 (FAQ)

### Q: spec-kit은 한국어로 사용할 수 있나요?

A: 네, AI 에이전트(Claude Code, Cursor 등)에서 한국어로 지시를 내릴 수 있습니다. 사양도 한국어로 작성 가능합니다.

### Q: 기존 프로젝트에 spec-kit을 도입할 수 있나요?

A: 네, 가능합니다. Tutorial 3에서 브라운필드 개발에 적용하는 방법을 배울 수 있습니다. 기존 코드의 사양화부터 시작하는 것을 추천합니다.

### Q: 팀 개발에서 spec-kit을 사용할 수 있나요?

A: 네, spec-kit은 특히 팀 개발에서 효과를 발휘합니다. 사양이 명확해짐으로써 멤버 간의 인식 차이를 줄일 수 있습니다.

### Q: 어떤 AI 에이전트를 추천하나요?

A: Claude Code, Cursor, GitHub Copilot 등이 권장됩니다. 이 튜토리얼은 Claude Code를 전제로 하고 있지만, 다른 에이전트에서도 동일하게 동작합니다.

### Q: spec-kit 학습 시간은 얼마나 걸리나요?

A:

* 기본 습득: Tutorial 1 (30분)
* 실전 레벨: Tutorial 1-2 (90분)
* 상급 레벨: Tutorial 1-3 (3시간)

### Q: 구현하지 않고 사양만 만드는 것도 가능한가요?

A: 네, 가능합니다. spec-kit은 사양 작성부터 구현까지 유연하게 사용할 수 있습니다. 사양 리뷰만 진행하고, 구현은 다른 방법으로 하는 것도 가능합니다.

## 리소스

* **공식 리포지토리**: [https://github.com/github/spec-kit](https://github.com/github/spec-kit)
* **문서**: 리포지토리의 README.md
* **커뮤니티**: GitHub Discussions

## 트러블슈팅

### spec-kit 명령어를 찾을 수 없음

```bash
# 설치 확인
uv tool list

# 재설치
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git

```

### 슬래시 명령어가 동작하지 않음

* Claude Code나 Cursor 등의 AI 에이전트 내부에서 실행해 주세요.
* 프로젝트 디렉토리에 `.speckit/` 폴더가 있는지 확인해 주세요.
* AI 에이전트를 재시작해 보세요.

### 생성된 코드가 예상과 다름

1. `constitution.md`를 검토하여 더 상세한 원칙 추가
2. `specification/*.md`를 검토하여 요구사항 명확화
3. `/speckit.clarify`를 사용하여 불명확한 점을 명확화
4. AI 에이전트에게 구체적인 예시 제시

## 피드백

이 튜토리얼 가이드에 대한 피드백이나 개선 제안은 언제나 환영합니다.
GitHub의 Issue나 Pull Request로 알려주세요.

## 라이선스

이 튜토리얼 가이드는 MIT 라이선스 하에 공개되어 있습니다.
spec-kit 본체의 라이선스는 공식 리포지토리를 참조해 주세요.

## 다음 단계

자, Tutorial 1부터 시작해 볼까요?

```bash
cd tutorial-1-todo-app
cat README.md

```
