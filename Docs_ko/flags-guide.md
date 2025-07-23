# SuperClaude 플래그 사용자 가이드 🏁

## 🤖 대부분의 플래그는 자동으로 활성화됩니다 - 스트레스 받지 마세요!

**솔직한 진실**: 이 플래그들을 외울 필요가 없습니다. SuperClaude는 보통 당신이 하는 일에 따라 유용한 플래그를 추가하려고 시도합니다!

**실제로 일어나는 일:**
- `/analyze auth.js`를 입력합니다
- SuperClaude는 그것이 보안 관련 코드임을 감지합니다
- **보통** `--persona-security`, `--focus security`, `--validate`를 추가합니다
- 당신은 종종 플래그를 관리하지 않고도 전문적인 보안 분석을 받게 됩니다

**언제 수동으로 플래그를 사용할까요?**
- SuperClaude가 선택한 것을 **덮어쓰고** 싶을 때 (드묾)
- 특정 측면에 대해 **궁금할** 때 (`--focus performance`)
- 다른 접근 방식을 **실험하고** 싶을 때

**결론**: 그냥 기본 명령어를 사용하고 자동 활성화가 작동하도록 두세요. 이 플래그들은 당신이 필요할 때가 아니라 원할 때 여기에 있습니다. 🎯

---

## 🚀 그냥 이것들을 시도해보세요 (플래그 지식 필요 없음)

```bash
# 이것들은 플래그 지식 없이도 잘 작동합니다:
/sc:analyze src/ # 올바른 분석 플래그를 자동으로 선택합니다
/sc:build # 프로젝트에 따라 자동으로 최적화합니다
/sc:improve messy-code.js # 품질 및 안전 플래그를 자동으로 활성화합니다
/sc:troubleshoot "weird error" # 디버깅 및 분석 플래그를 자동으로 활성화합니다
```

**보셨죠? 플래그가 필요 없습니다.** 아래의 모든 내용은 배후에서 무슨 일이 일어나고 있는지 궁금해질 때를 위한 것입니다.

---

SuperClaude의 플래그 시스템에 대한 실용적인 가이드입니다. 플래그는 SuperClaude의 동작 방식을 변경하는 명령줄 옵션과 같습니다 - 명령어의 초능력이라고 생각하세요.

## 플래그란 무엇인가요? 🤔

**플래그는 수정자**로서 SuperClaude가 요청을 처리하는 방식을 변경합니다. 명령어 뒤에 오며 `--`로 시작합니다.

**기본 구문** (하지만 보통 이것을 알 필요는 없습니다):
```bash
/sc:command --flag-name
/sc:command --flag-name value
/sc:analyze src/ --focus security --depth deep
```

**실제로 플래그가 작동하는 방식**:
1. **자동 활성화** - SuperClaude가 컨텍스트에 따라 추가합니다 (이것이 주요 방식입니다! 🎯)
2. **수동 재정의** - 다른 동작을 원할 경우 명시적으로 추가할 수 있습니다

**플래그가 존재하는 이유** (주로 자동적인 이점):
- 더 좋고 집중된 결과를 얻습니다
- 올바른 사고 깊이를 자동으로 활성화합니다
- 유용할 때 특별한 기능에 연결합니다
- 작업에 따라 속도나 세부 사항을 최적화합니다
- 실제로 작업하는 것에 주의를 집중시킵니다

**핵심**: SuperClaude는 플래그 선택을 지능적으로 처리하므로 당신이 그것에 대해 생각할 필요가 없습니다! 🧠

## 플래그 카테고리 📂

### 계획 및 분석 플래그 🧠

이것들은 SuperClaude가 요청에 대해 얼마나 깊이 생각하는지를 제어합니다.

#### `--plan`
**기능**: 무언가를 하기 전에 실행 계획을 보여줍니다
**사용 시기**: SuperClaude가 먼저 무엇을 할지 보고 싶을 때
**예시**: `/build --plan` - 실행하기 전에 빌드 단계를 봅니다

#### `--think`
**기능**: 다중 파일 분석 (~4K 토큰)
**사용 시기**: 여러 파일을 포함하는 복잡한 문제
**자동 활성화**: 5개 이상의 파일 가져오기 체인, 10개 이상의 참조를 가진 모듈 간 호출
**예시**: `/analyze complex-system/ --think`

#### `--think-hard`
**기능**: 심층 아키텍처 분석 (~10K 토큰)
**사용 시기**: 시스템 전반의 문제, 아키텍처 결정
**자동 활성화**: 시스템 리팩토링, 3개 이상의 모듈에 걸친 병목 현상
**예시**: `/improve legacy-system/ --think-hard`

#### `--ultrathink`
**기능**: 최대 깊이 분석 (~32K 토큰)
**사용 시기**: 중요한 시스템 재설계, 복잡한 디버깅
**자동 활성화**: 레거시 현대화, 심각한 취약점
**예시**: `/troubleshoot "entire auth system broken" --ultrathink`

**💡 팁**: `--think`로 시작하고, 필요한 경우에만 더 깊이 들어가세요. 더 많이 생각할수록 느리지만 더 철저합니다.

---

### 효율성 및 제어 플래그 ⚡

출력 스타일, 안전성, 성능을 제어합니다.

#### `--uc` / `--ultracompressed`
**기능**: 기호를 사용하여 60-80% 토큰 감소
**사용 시기**: 대규모 작업, 컨텍스트가 가득 찰 때
**자동 활성화**: 컨텍스트 사용량 >75%, 대규모 작업
**예시**: `/analyze huge-codebase/ --uc`

#### `--safe-mode`
**기능**: 최대 유효성 검사, 보수적인 실행
**사용 시기**: 프로덕션 환경, 위험한 작업
**자동 활성화**: 리소스 사용량 >85%, 프로덕션 환경
**예시**: `/improve production-code/ --safe-mode`

#### `--validate`
**기능**: 작업 전 유효성 검사 및 위험 평가
**사용 시기**: 변경하기 전에 확인하고 싶을 때
**자동 활성화**: 위험 점수 >0.7
**예시**: `/cleanup legacy/ --validate`

#### `--verbose`
**기능**: 최대 세부 정보 및 설명
**사용 시기**: 학습, 디버깅, 전체 컨텍스트가 필요할 때
**예시**: `/build --verbose` - 모든 빌드 단계를 봅니다

#### `--answer-only`
**기능**: 작업 생성 없이 직접적인 응답
**사용 시기**: 빠른 질문, 워크플로우 자동화를 원하지 않을 때
**예시**: `/explain React hooks --answer-only`

**💡 팁**: `--uc`는 큰 작업에 좋습니다. `--safe-mode`는 중요한 모든 것에 좋습니다. `--verbose`는 학습할 때 좋습니다.

---

### MCP 서버 플래그 🔧

MCP 서버를 통해 특수 기능을 활성화합니다.

#### `--c7` / `--context7`
**기능**: 공식 라이브러리 문서를 위해 Context7을 활성화합니다
**사용 시기**: 프레임워크 작업, 공식 문서가 필요할 때
**자동 활성화**: 외부 라이브러리 가져오기, 프레임워크 질문
**예시**: `/build react-app/ --c7` - React 모범 사례를 얻습니다

#### `--seq` / `--sequential`
**기능**: 복잡한 다단계 분석을 위해 Sequential을 활성화합니다
**사용 시기**: 복잡한 디버깅, 시스템 설계
**자동 활성화**: 복잡한 디버깅, `--think` 플래그
**예시**: `/troubleshoot "auth flow broken" --seq`

#### `--magic`
**기능**: UI 컴포넌트 생성을 위해 Magic을 활성화합니다
**사용 시기**: UI 컴포넌트 생성, 디자인 시스템
**자동 활성화**: UI 컴포넌트 요청, 프론트엔드 페르소나
**예시**: `/build dashboard --magic` - 최신 UI 컴포넌트를 얻습니다

#### `--play` / `--playwright`
**기능**: 브라우저 자동화 및 테스트를 위해 Playwright를 활성화합니다
**사용 시기**: E2E 테스트, 성능 모니터링
**자동 활성화**: 테스트 워크플로우, QA 페르소나
**예시**: `/test e2e --play`

#### `--all-mcp`
**기능**: 모든 MCP 서버를 동시에 활성화합니다
**사용 시기**: 복잡한 다중 도메인 문제
**자동 활성화**: 문제 복잡도 >0.8, 다중 도메인 지표
**예시**: `/analyze entire-app/ --all-mcp`

#### `--no-mcp`
**기능**: 모든 MCP 서버를 비활성화하고, 네이티브 도구만 사용합니다
**사용 시기**: 더 빠른 실행, 특수 기능이 필요 없을 때
**예시**: `/analyze simple-script.js --no-mcp`

**💡 팁**: MCP 서버는 기능을 추가하지만 더 많은 토큰을 사용합니다. 문서는 `--c7`, 생각은 `--seq`, UI는 `--magic`입니다.

---

### 고급 오케스트레이션 플래그 🎭

복잡한 작업 및 워크플로우용.

#### `--delegate [files|folders|auto]`
**기능**: 병렬 처리를 위해 하위 에이전트 위임을 활성화합니다
**사용 시기**: 대규모 코드베이스, 복잡한 분석
**자동 활성화**: >7개 디렉토리 또는 >50개 파일
**옵션**:
- `files` - 개별 파일 분석 위임
- `folders` - 디렉토리 수준 분석 위임
- `auto` - 스마트 위임 전략

**예시**: `/analyze monorepo/ --delegate auto`

#### `--wave-mode [auto|force|off]`
**기능**: 복합 지능을 사용한 다단계 실행
**사용 시기**: 복잡한 개선, 체계적인 분석
**자동 활성화**: 복잡도 >0.8 및 파일 >20 및 작업 유형 >2
**예시**: `/improve legacy-system/ --wave-mode force`

#### `--loop`
**기능**: 반복적인 개선 모드
**사용 시기**: 품질 개선, 구체화 작업
**자동 활성화**: 다듬기, 구체화, 향상 키워드
**예시**: `/improve messy-code.js --loop`

#### `--concurrency [n]`
**기능**: 최대 동시 하위 에이전트 제어 (1-15)
**사용 시기**: 리소스 사용량 제어
**예시**: `/analyze --delegate auto --concurrency 3`

**💡 팁**: 이것들은 강력하지만 복잡합니다. 큰 프로젝트에는 `--delegate auto`로 시작하고, 개선에는 `--loop`를 사용하세요.

---

### 초점 및 범위 플래그 🎯

SuperClaude의 주의를 특정 영역으로 향하게 합니다.

#### `--scope [level]`
**옵션**: file, module, project, system
**기능**: 분석 범위를 설정합니다
**예시**: `/analyze --scope module auth/`

#### `--focus [domain]`
**옵션**: performance, security, quality, architecture, accessibility, testing
**기능**: 특정 도메인에 분석을 집중합니다
**예시**: `/analyze --focus security --scope project`

#### 페르소나 플래그
**사용 가능한 페르소나**: architect, frontend, backend, analyzer, security, mentor, refactorer, performance, qa, devops, scribe
**기능**: 전문가 행동 패턴을 활성화합니다
**예시**: `/analyze --persona-security` - 보안 중심 분석

**💡 팁**: `--focus`는 대상 분석에 좋습니다. 페르소나는 자동으로 활성화되지만 수동 제어가 도움이 됩니다.

---

## 일반적인 플래그 패턴 🔄

### 빠른 분석
```bash
/sc:analyze src/ --focus quality # 빠른 품질 확인
/sc:analyze --uc --focus security # 빠른 보안 스캔
```

### 심층 조사
```bash
/sc:troubleshoot "bug" --think --seq # 체계적인 디버깅
/sc:analyze --think-hard --focus architecture # 아키텍처 분석
```

### 대규모 프로젝트 작업
```bash
/sc:analyze monorepo/ --delegate auto --uc # 효율적인 대규모 분석
/sc:improve legacy/ --wave-mode auto --safe-mode # 안전한 체계적 개선
```

### 학습 및 문서화
```bash
/sc:explain React hooks --c7 --verbose # 문서와 함께 상세한 설명
/sc:document api/ --persona-scribe # 전문적인 문서화
```

### 성능 중심
```bash
/sc:analyze --focus performance --play # 테스트와 함께 성능 분석
/sc:build --uc --no-mcp # 추가 기능 없는 빠른 빌드
```

### 보안 중심
```bash
/sc:analyze --focus security --think --validate # 철저한 보안 분석
/sc:scan --persona-security --safe-mode # 보수적인 보안 스캔
```

## 실제 예시 💡

### 전/후: 기본 분석
**전** (기본):
```bash
/sc:analyze auth.js
# → 간단한 파일 분석
```

**후** (플래그 사용):
```bash
/sc:analyze auth.js --focus security --think --c7
# → 심층적인 사고와 공식 문서를 사용한 보안 중심 분석
# → 훨씬 더 철저하고, 보안 패턴을 찾고, 모범 사례와 비교 확인
```

### 전/후: 대규모 프로젝트
**전** (느림):
```bash
/sc:analyze huge-monorepo/
# → 모든 것을 한 번에 분석하려고 시도하여 시간 초과 또는 너무 많은 토큰을 사용할 수 있음
```

**후** (효율적):
```bash
/sc:analyze huge-monorepo/ --delegate auto --uc --focus architecture
# → 작업을 하위 에이전트에게 위임하고, 출력을 압축하고, 아키텍처에 집중
# → 더 빠르고, 더 집중되고, 더 나은 결과
```

### 전/후: 개선 작업
**전** (위험):
```bash
/sc:improve legacy-system/
# → 너무 많은 변경을 하여 문제를 일으킬 수 있음
```

**후** (안전):
```bash
/sc:improve legacy-system/ --safe-mode --loop --validate --preview
# → 안전한 변경만, 반복적인 접근, 먼저 유효성 검사, 미리보기 표시
# → 훨씬 더 안전하고, 점진적인 개선
```

## 자동 활성화 예시 🤖

SuperClaude는 보통 컨텍스트에 따라 플래그를 추가합니다. 다음은 시도하는 경우입니다:

### 복잡도 기반
```bash
/sc:analyze huge-codebase/
# 자동 추가: --delegate auto --uc
# 이유: >50개 파일 감지, 컨텍스트 관리 필요

/sc:troubleshoot "complex system issue"
# 자동 추가: --think --seq
# 이유: 다중 컴포넌트 문제 감지
```

### 도메인 기반
```bash
/sc:build react-app/
# 자동 추가: --c7 --persona-frontend
# 이유: 프론트엔드 프레임워크 감지

/sc:analyze --focus security
# 자동 추가: --persona-security --validate
# 이유: 보안 초점이 보안 전문가를 트리거함
```

### 성능 기반
```bash
# 컨텍스트 사용량 >75%일 때
/sc:analyze large-project/
# 자동 추가: --uc
# 이유: 토큰 최적화 필요

# 위험 점수 >0.7일 때
/sc:improve production-code/
# 자동 추가: --safe-mode --validate
# 이유: 고위험 작업 감지
```

## 고급 사용법 🚀

### 복잡한 플래그 조합

**포괄적인 코드 검토**:
```bash
/sc:review codebase/ --persona-qa --think-hard --focus quality --validate --c7
# → QA 전문가 + 심층 사고 + 품질 초점 + 유효성 검사 + 문서
```

**레거시 시스템 현대화**:
```bash
/sc:improve legacy/ --wave-mode force --persona-architect --safe-mode --loop --c7
# → 웨이브 오케스트레이션 + 아키텍트 관점 + 안전성 + 반복 + 문서
```

**보안 감사**:
```bash
/sc:scan --persona-security --ultrathink --focus security --validate --seq
# → 보안 전문가 + 최대 사고 + 보안 초점 + 유효성 검사 + 체계적인 분석
```

### 성능 최적화

**속도를 위해**:
```bash
/sc:analyze --no-mcp --uc --scope file
# → 추가 기능 비활성화, 출력 압축, 범위 제한
```

**철저함을 위해**:
```bash
/sc:analyze --all-mcp --think-hard --delegate auto
# → 모든 기능, 심층 사고, 병렬 처리
```

### 맞춤형 워크플로우

**버그 조사 워크플로우**:
```bash
/sc:troubleshoot "specific error" --seq --think --validate
/sc:analyze affected-files/ --focus quality --persona-analyzer
/sc:test --play --coverage
```

**기능 개발 워크플로우**:
```bash
/sc:design new-feature --persona-architect --c7
/sc:build --magic --persona-frontend --validate
/sc:test --play --coverage
/sc:document --persona-scribe --c7
```

## 빠른 참조 📋

### 가장 유용한 플래그
| 플래그 | 목적 | 사용 시기 |
|---|---|---|
| `--think` | 더 깊은 분석 | 복잡한 문제 |
| `--uc` | 출력 압축 | 대규모 작업 |
| `--safe-mode` | 보수적인 실행 | 중요한 코드 |
| `--c7` | 공식 문서 | 프레임워크 작업 |
| `--seq` | 체계적인 분석 | 디버깅 |
| `--focus security` | 보안 초점 | 보안 문제 |
| `--delegate auto` | 병렬 처리 | 대규모 코드베이스 |
| `--validate` | 조치 전 확인 | 위험한 작업 |

### 잘 작동하는 플래그 조합
```bash
# 안전한 개선
--safe-mode --validate --preview

# 심층 분석
--think --seq --c7

# 대규모 프로젝트
--delegate auto --uc --focus

# 학습
--verbose --c7 --persona-mentor

# 보안 작업
--persona-security --focus security --validate

# 성능 작업
--persona-performance --focus performance --play
```

### 자동 활성화 트리거
- **--think**: 복잡한 가져오기, 모듈 간 호출
- **--uc**: 컨텍스트 >75%, 대규모 작업
- **--safe-mode**: 리소스 사용량 >85%, 프로덕션
- **--delegate**: >7개 디렉토리 또는 >50개 파일
- **--c7**: 프레임워크 가져오기, 문서화 요청
- **--seq**: 디버깅 키워드, --think 플래그
- **페르소나**: 도메인별 키워드 및 패턴

## 플래그 문제 해결 🚨

### 일반적인 문제

**"플래그가 작동하지 않는 것 같습니다"**
- 철자 확인 (일반적인 오타: `--ultracompresed`, `--persona-fronted`)
- 일부 플래그는 값이 필요합니다: `--scope project`, `--focus security`
- 플래그 충돌: `--no-mcp`는 `--c7`, `--seq` 등을 재정의합니다.

**"작업이 너무 느립니다"**
- 압축을 위해 `--uc`를 시도해보세요
- 추가 기능을 비활성화하려면 `--no-mcp`를 사용하세요
- 범위 제한: `--scope project` 대신 `--scope file`

**"출력이 너무 많습니다"**
- 압축을 위해 `--uc`를 추가하세요
- 있는 경우 `--verbose`를 제거하세요
- 간단한 질문에는 `--answer-only`를 사용하세요

**"충분히 철저하지 않습니다"**
- `--think` 또는 `--think-hard`를 추가하세요
- 관련 MCP 서버 활성화: `--seq`, `--c7`
- 적절한 페르소나 사용: `--persona-analyzer`

**"변경이 너무 위험합니다"**
- 중요한 코드에는 항상 `--safe-mode`를 사용하세요
- 먼저 확인하려면 `--validate`를 추가하세요
- 적용하기 전에 변경 사항을 보려면 `--preview`를 사용하세요

### 플래그 충돌

**다른 것을 재정의하는 것들**:
- `--no-mcp`는 모든 MCP 플래그 (`--c7`, `--seq` 등)를 재정의합니다.
- `--safe-mode`는 최적화 플래그를 재정의합니다.
- 마지막 페르소나 플래그가 이깁니다: `--persona-frontend --persona-backend` → 백엔드

**우선 순위**:
1. 안전 플래그 (`--safe-mode`)가 최적화를 이깁니다
2. 명시적 플래그가 자동 활성화를 이깁니다
3. 사고 깊이: `--ultrathink` > `--think-hard` > `--think`
4. 범위: system > project > module > file

## 효과적인 플래그 사용 팁 💡

### 시작하기 (솔직한 진실)
1. **처음에는 플래그를 무시하세요** - 자동 활성화가 대부분의 경우를 꽤 잘 처리합니다
2. **자동 활성화되는 것을 지켜보세요** - SuperClaude가 선택하는 것을 보면서 배우게 될 것입니다
3. **궁금할 때 `--help`를 사용하세요** - 많은 명령어가 사용 가능한 플래그를 보여줍니다
4. **자동화를 신뢰하세요** - SuperClaude는 보통 합리적인 기본값을 선택합니다

### 고급화하기 (원한다면)
1. **재정의를 실험해보세요** - 다른 관점을 위해 보안이 아닌 코드에 `--persona-security`를 시도해보세요
2. **유용한 조합을 배우세요** - 중요한 것에는 `--safe-mode --validate`
3. **성능 트레이드오프를 이해하세요** - 빠름 (`--uc --no-mcp`) 대 철저함 (`--think-hard --all-mcp`)
4. **학습을 위해 플래그를 사용하세요** - 무슨 일이 일어나고 있는지 이해하고 싶을 때 `--verbose`

### 성능 팁 (파워 유저용)
- **속도를 위해**: `--uc --no-mcp --scope file`
- **철저함을 위해**: `--think-hard --all-mcp --delegate auto`
- **안전성을 위해**: `--safe-mode --validate --preview`
- **학습을 위해**: `--verbose --c7 --persona-mentor`

---

## 최종 참고 사항 📝

**플래그에 대한 진짜 진실** 💯:
- **자동 활성화는 보통 수동 플래그 선택에 비해 꽤 잘 작동합니다**
- **이 가이드의 대부분을 무시하고** 기본 명령어만 사용해도 됩니다
- **플래그는 필요할 때가 아니라 원할 때 여기에 있습니다**
- **학습은 가이드를 공부하는 것이 아니라 사용을 통해 자연스럽게 이루어집니다** 😊

**압도당하지 마세요** 🧘‍♂️:
- SuperClaude는 플래그 지식 없이도 잘 작동하도록 노력합니다
- 위의 상세 정보는 필요성이 아니라 호기심을 위한 것입니다
- 자동 활성화는 사용 패턴에 따라 계속해서 더 똑똑해집니다
- 플래그를 외우지 않는다고 해서 놓치는 것은 없습니다

**실제로 플래그가 필요할 때**:
- 자동 활성화 재정의 (드묾)
- 다른 접근 방식 실험 (재미)
- 특정 성능 요구에 맞게 최적화 (고급)
- 무슨 일이 일어났는지에 대해 배우기 (교육적)

**간단하게 시작하고, 간단하게 유지하세요** 🎯:
- 기본 명령어 사용: `/analyze`, `/build`, `/improve`
- 자동 활성화가 복잡성을 처리하도록 두세요
- 실험하고 싶을 때만 수동 플래그를 추가하세요
- SuperClaude가 무엇을 하는지 알고 있다고 믿으세요

---

*기억하세요: 이 모든 명백한 복잡성 뒤에, SuperClaude는 실제로 사용하기 간단합니다. 그냥 명령어를 입력하기 시작하세요! 🚀*
