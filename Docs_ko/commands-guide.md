# SuperClaude 명령어 가이드 🛠️

## 💡 너무 복잡하게 생각하지 마세요 - SuperClaude가 도와드립니다

**이 17개 명령어에 대한 진실**: 모두 외울 필요가 없습니다. 그냥 `/sc:analyze`나 `/sc:implement`로 시작해서 어떻게 되는지 보세요!

**보통 이렇게 작동합니다:**

- Claude Code에 `/`를 입력하세요 → 사용 가능한 명령어를 볼 수 있습니다
- `/sc:analyze`, `/sc:build`, `/sc:improve` 같은 기본 명령어를 사용하세요
- **SuperClaude는 각 상황에 맞는 유용한 도구와 전문가를 선택하려고 노력합니다**
- 익숙해지면 더 많은 명령어가 유용해집니다

**자동 활성화는 꽤 멋집니다** 🪄 - SuperClaude는 당신이 하려는 일을 감지하고 관련 전문가(보안 전문가, 성능 최적화 전문가 등)를 당신이 관리하지 않아도 활성화하려고 시도합니다. 보통 잘 작동합니다! 😊

---

## 빠른 "그냥 한번 시도해보세요" 목록 🚀

**여기서 시작하세요** (읽을 필요 없음):
```bash
/sc:help # 사용 가능한 기능 보기
/sc:analyze src/ # 코드를 스마트하게 분석하려고 시도합니다
/sc:workflow feature-100-prd.md # PRD로부터 단계별 구현 워크플로우를 생성합니다
/sc:implement user-auth # 기능과 컴포넌트를 생성합니다 (v2 /build 대체)
/sc:build # 지능적인 프로젝트 빌드를 시도합니다
/sc:improve messy-file.js # 코드를 정리하려고 시도합니다
/sc:troubleshoot "error" # 문제 해결을 돕습니다
```

**솔직히 이 정도면 시작하기에 충분합니다.** 아래의 나머지 내용은 다른 어떤 도구들이 있는지 궁금해질 때를 위한 것입니다. 🛠️

---

모든 16개 SuperClaude 슬래시 명령어에 대한 실용적인 가이드입니다. 어떤 것이 잘 작동하고 어떤 것이 아직 미흡한지에 대해 솔직하게 알려드립니다.

## 빠른 참조 📋

*(이것을 외울 필요는 없습니다 - 그냥 유용해 보이는 것을 선택하세요)*

| 명령어 | 목적 | 자동 활성화 | 가장 적합한 용도 |
|---|---|---|---|
| `/sc:analyze` | 스마트 코드 분석 | 보안/성능 전문가 | 문제 찾기, 코드베이스 이해 |
| `/sc:build` | 지능적인 빌드 | 프론트엔드/백엔드 전문가 | 컴파일, 번들링, 배포 준비 |
| `/sc:implement` | 기능 구현 | 특정 분야 전문가 | 기능, 컴포넌트, API, 서비스 생성 |
| `/sc:improve` | 자동 코드 정리 | 품질 전문가 | 리팩토링, 최적화, 품질 수정 |
| `/sc:troubleshoot` | 문제 조사 | 디버그 전문가 | 디버깅, 문제 조사 |
| `/sc:test` | 스마트 테스팅 | QA 전문가 | 테스트 실행, 커버리지 분석 |
| `/sc:document` | 자동 문서화 | 글쓰기 전문가 | README 파일, 코드 주석, 가이드 |
| `/sc:git` | 향상된 git 워크플로우 | DevOps 전문가 | 스마트 커밋, 브랜치 관리 |
| `/sc:design` | 시스템 설계 도움 | 아키텍처 전문가 | 아키텍처 계획, API 설계 |
| `/sc:explain` | 학습 보조 | 교육 전문가 | 개념 학습, 코드 이해 |
| `/sc:cleanup` | 부채 감소 | 리팩토링 전문가 | 죽은 코드 제거, 파일 정리 |
| `/sc:load` | 컨텍스트 이해 | 분석 전문가 | 프로젝트 분석, 코드베이스 이해 |
| `/sc:estimate` | 스마트 견적 | 계획 전문가 | 시간/노력 계획, 복잡도 분석 |
| `/sc:spawn` | 복잡한 워크플로우 | 오케스트레이션 시스템 | 다단계 작업, 워크플로우 자동화 |
| `/sc:task` | 프로젝트 관리 | 계획 시스템 | 장기 기능 계획, 작업 추적 |
| `/sc:workflow` | 구현 계획 | 워크플로우 시스템 | PRD로부터 단계별 워크플로우 생성 |
| `/sc:index` | 명령어 탐색 | 도움말 시스템 | 작업에 맞는 명령어 찾기 |

**프로 팁**: 그냥 유용해 보이는 것을 시도해보세요. SuperClaude는 보통 각 상황에 맞는 유용한 전문가와 도구를 활성화하려고 노력합니다! 🎯

## 개발 명령어 🔨

### `/workflow` - 구현 워크플로우 생성기 🗺️
**기능**: PRD와 기능 요구사항을 분석하여 포괄적인 단계별 구현 워크플로우를 생성합니다.

**유용한 점**: PRD를 가져와 전문가 지침, 의존성 매핑, 작업 오케스트레이션을 포함한 구조화된 구현 계획으로 분해합니다! 🎯

**사용 시기**:
- PRD나 명세서로부터 새로운 기능을 시작할 때
- 명확한 구현 로드맵이 필요할 때
- 구현 전략에 대한 전문가 지침을 원할 때
- 여러 의존성을 가진 복잡한 기능을 계획할 때

**마법**: 기능 요구사항에 따라 적절한 전문가 페르소나(아키텍트, 보안, 프론트엔드, 백엔드)와 MCP 서버(패턴을 위한 Context7, 복잡한 분석을 위한 Sequential)를 자동으로 활성화합니다.

**예시**:
```bash
/sc:workflow docs/feature-100-prd.md --strategy systematic --c7 --sequential
/sc:workflow "user authentication system" --persona security --output detailed
/sc:workflow payment-api --strategy mvp --risks --dependencies
```

**결과물**:

- **로드맵 형식**: 타임라인이 포함된 단계별 구현 계획
- **작업 형식**: 조직화된 에픽, 스토리, 실행 가능한 작업
- **상세 형식**: 시간 추정치가 포함된 단계별 지침
- **위험 평가**: 잠재적 문제 및 완화 전략
- **의존성 매핑**: 내부 및 외부 의존성
- **전문가 지침**: 특정 분야의 모범 사례 및 패턴

### `/implement` - 기능 구현
**기능**: 지능적인 전문가 활성화를 통해 기능, 컴포넌트, 기능을 구현합니다.

**유용한 점**: SuperClaude는 구현하려는 내용에 따라 적절한 전문가(프론트엔드, 백엔드, 보안)와 도구를 자동으로 활성화합니다! 🎯

**사용 시기**:

- 새로운 기능이나 컴포넌트를 생성할 때 (v2의 `/build` 기능 대체)
- API, 서비스, 모듈을 구현할 때
- 최신 프레임워크로 UI 컴포넌트를 빌드할 때
- 비즈니스 로직과 통합을 개발할 때

**기본 구문**:
```bash
/sc:implement user authentication system # 전체 기능 구현
/sc:implement --type component LoginForm # 특정 컴포넌트 생성
/sc:implement --type api user-management # API 엔드포인트 빌드
/sc:implement --framework react dashboard # 프레임워크별 구현
```

**유용한 플래그**:

- `--type component|api|service|feature|module` - 구현 유형
- `--framework react|vue|express|django|etc` - 대상 프레임워크
- `--safe` - 보수적인 구현 접근 방식
- `--iterative` - 검증을 통한 단계별 개발
- `--with-tests` - 테스트 구현 포함
- `--documentation` - 코드와 함께 문서 생성

**실제 예시**:
```bash
/sc:implement user authentication --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for orders --type api --safe
/sc:implement payment processing --type service --iterative
/sc:implement search functionality --framework vue --documentation
```

**자동 활성화 패턴**:

- **프론트엔드**: UI 컴포넌트, React/Vue/Angular → 프론트엔드 페르소나 + Magic MCP
- **백엔드**: API, 서비스, 데이터베이스 → 백엔드 페르소나 + Context7
- **보안**: 인증, 결제, 민감 데이터 → 보안 페르소나 + 유효성 검사
- **복잡한 기능**: 다단계 구현 → Sequential MCP + 아키텍트 페르소나

**주의사항**:

- 더 나은 결과를 위해 `--type`을 지정하세요 (component vs service vs feature)
- 특정 기술 스택으로 작업할 때 `--framework`를 사용하세요
- 프로덕션 코드에는 `--safe`를, 복잡한 기능에는 `--iterative`를 시도해보세요
- 기억하세요: 이것은 실제 코드 구현을 위해 v2의 `/build`를 대체합니다

---

### `/build` - 프로젝트 빌드
**기능**: 스마트한 오류 처리로 프로젝트를 빌드, 컴파일, 패키징합니다.

**쉬운 방법**: 그냥 `/sc:build`를 입력하면 SuperClaude가 빌드 시스템을 파악하려고 시도합니다! 🎯

**사용 시기**:

- 프로젝트를 컴파일/번들해야 할 때 (그냥 `/sc:build`를 시도하세요)
- 빌드 프로세스가 실패하고 디버깅에 도움이 필요할 때
- 빌드 최적화를 설정할 때 (필요한 것을 감지하려고 시도합니다)
- 배포를 준비할 때

**기본 구문**:
```bash
/sc:build # 현재 프로젝트 빌드
/sc:build --type prod # 프로덕션 빌드
/sc:build --clean # 클린 빌드 (오래된 아티팩트 제거)
/sc:build --optimize # 최적화 활성화
/sc:build src/ # 특정 디렉토리 빌드
```

**유용한 플래그**:

- `--type dev|prod|test` - 빌드 유형
- `--clean` - 빌드 전 정리
- `--optimize` - 빌드 최적화 활성화
- `--verbose` - 상세 빌드 출력 표시

**실제 예시**:
```bash
/sc:build --type prod --optimize # 최적화된 프로덕션 빌드
/sc:build --clean --verbose # 상세 출력을 포함한 클린 빌드
/sc:build src/components # 컴포넌트 폴더만 빌드
```

**주의사항**:

- 일반적인 빌드 도구(npm, webpack 등)에서 가장 잘 작동합니다
- 매우 맞춤화된 빌드 설정에서는 어려움을 겪을 수 있습니다
- 빌드 도구가 PATH에 있는지 확인하세요

---

### `/design` - 시스템 및 컴포넌트 설계
**기능**: 시스템 아키텍처, API 설계, 컴포넌트 명세서를 생성합니다.

**사용 시기**:

- 새로운 기능이나 시스템을 계획할 때
- API나 데이터베이스 설계가 필요할 때
- 컴포넌트 아키텍처를 생성할 때
- 시스템 관계를 문서화할 때

**기본 구문**:
```bash
/sc:design user-auth-system # 사용자 인증 시스템 설계
/sc:design --type api auth # API 부분만 설계
/sc:design --format spec payment # 공식 명세서 생성
```

**유용한 플래그**:

- `--type architecture|api|component|database` - 설계 초점
- `--format diagram|spec|code` - 출력 형식
- `--iterative` - 반복을 통해 설계 구체화

**실제 예시**:
```bash
/sc:design --type api user-management # 사용자 관리 API 설계
/sc:design --format spec chat-system # 채팅 시스템 명세서 생성
/sc:design --type database ecommerce # 데이터베이스 스키마 설계
```

**주의사항**:

- 코드 생성보다는 개념적입니다
- 출력 품질은 요구사항을 얼마나 명확하게 설명하는지에 따라 달라집니다
- 구현 세부사항보다는 계획 단계에 좋습니다

## 분석 명령어 🔍

### `/analyze` - 코드 분석
**기능**: 코드 품질, 보안, 성능, 아키텍처에 대한 포괄적인 분석.

**유용한 점**: SuperClaude는 어떤 종류의 분석이 필요한지 감지하려고 시도하며 보통 관련 전문가를 선택합니다! 🔍

**사용 시기**:

- 익숙하지 않은 코드베이스를 이해할 때 (어떤 폴더든 가리키기만 하면 됩니다)
- 보안 취약점을 찾을 때 (보통 보안 전문가가 개입합니다)
- 성능 병목 현상을 찾을 때 (보통 성능 전문가가 돕습니다)
- 코드 품질을 평가할 때 (보통 품질 전문가가 담당합니다)

**기본 구문**:
```bash
/sc:analyze src/ # 전체 src 디렉토리 분석
/sc:analyze --focus security # 보안 문제에 집중
/sc:analyze --depth deep app.js # 특정 파일 심층 분석
```

**유용한 플래그**:

- `--focus quality|security|performance|architecture` - 분석 초점
- `--depth quick|deep` - 분석 깊이
- `--format text|json|report` - 출력 형식

**실제 예시**:
```bash
/sc:analyze --focus security --depth deep # 심층 보안 분석
/sc:analyze --focus performance src/api/ # API 성능 분석
/sc:analyze --format report . # 분석 보고서 생성
```

**주의사항**
:
- 큰 코드베이스에서는 시간이 걸릴 수 있습니다
- 보안 분석은 꽤 좋지만, 성능 분석은 다양합니다
- 일반적인 언어(JS, Python 등)에서 가장 잘 작동합니다

---

### `/troubleshoot` - 문제 조사
**기능**: 체계적인 디버깅 및 문제 조사.

**사용 시기**:

- 무언가 고장 났는데 이유를 모를 때
- 체계적인 디버깅 접근 방식이 필요할 때
- 오류 메시지가 혼란스러울 때
- 성능 문제 조사

**기본 구문**:
```bash
/sc:troubleshoot "login not working" # 로그인 문제 조사
/sc:troubleshoot --logs error.log # 오류 로그 분석
/sc:troubleshoot performance # 성능 문제 해결
```

**유용한 플래그**:

- `--logs <file>` - 로그 파일 분석 포함
- `--systematic` - 구조화된 디버깅 접근 방식 사용
- `--focus network|database|frontend` - 초점 영역

**실제 예시**:
```bash
/sc:troubleshoot "API returning 500" --logs server.log
/sc:troubleshoot --focus database "slow queries"
/sc:troubleshoot "build failing" --systematic
```

**주의사항**:

- 구체적인 오류 설명과 함께 더 잘 작동합니다
- 가능하면 관련 오류 메시지와 로그를 포함하세요
- 처음에는 명백한 것을 제안할 수 있습니다 (보통 좋은 일입니다!)

---

### `/explain` - 교육적인 설명
**기능**: 코드, 개념, 기술을 교육적인 방식으로 설명합니다.

**사용 시기**:

- 새로운 기술이나 패턴을 배울 때
- 복잡한 코드를 이해할 때
- 팀원들을 위한 명확한 설명이 필요할 때
- 까다로운 개념을 문서화할 때

**기본 구문**:
```bash
/sc:explain async/await # async/await 개념 설명
/sc:explain --code src/utils.js # 특정 코드 파일 설명
/sc:explain --beginner React hooks # 초보자 친화적인 설명
```

**유용한 플래그**:

- `--beginner` - 더 간단한 설명
- `--advanced` - 기술적 깊이
- `--code <file>` - 특정 코드 설명
- `--examples` - 실제 예시 포함

**실제 예시**:
```bash
/sc:explain --beginner "what is REST API"
/sc:explain --code src/auth.js --advanced
/sc:explain --examples "React context patterns"
```

**주의사항**:

- 잘 알려진 개념에 대해서는 훌륭하지만, 매우 전문적인 주제에 대해서는 어려움을 겪을 수 있습니다
- "이 코드베이스를 설명해줘"와 같은 모호한 질문보다는 구체적인 질문에 더 좋습니다
- 당신의 경험 수준에 대한 컨텍스트를 포함하세요

## 품질 명령어 ✨

### `/improve` - 코드 향상
**기능**: 코드 품질, 성능, 유지보수성에 대한 체계적인 개선.

**사용 시기**:

- 지저분한 코드 리팩토링
- 성능 최적화
- 모범 사례 적용
- 오래된 코드 현대화

**기본 구문**:
```bash
/sc:improve src/legacy/ # 레거시 코드 개선
/sc:improve --type performance # 성능에 집중
/sc:improve --safe src/utils.js # 안전하고 위험이 낮은 개선만
```

**유용한 플래그**:

- `--type quality|performance|maintainability|style` - 개선 초점
- `--safe` - 위험이 낮은 변경만 적용
- `--preview` - 변경될 내용을 실행하지 않고 보여줌

**실제 예시**:
```bash
/sc:improve --type performance --safe src/api/
/sc:improve --preview src/components/LegacyComponent.js
/sc:improve --type style . --safe
```

**주의사항**:

- 항상 `--preview`를 먼저 사용하여 변경하려는 내용을 확인하세요
- `--safe`는 당신의 친구입니다 - 위험한 리팩토링을 방지합니다
- 전체 코드베이스보다는 작은 파일/모듈에서 가장 잘 작동합니다

---

### `/cleanup` - 기술 부채 감소
**기능**: 죽은 코드, 사용하지 않는 임포트를 제거하고 파일 구조를 정리합니다.

**사용 시기**:

- 코드베이스가 어수선하게 느껴질 때
- 사용하지 않는 임포트/변수가 많을 때
- 파일 구성이 지저분할 때
- 주요 리팩토링 전

**기본 구문**:
```bash
/sc:cleanup src/ # src 디렉토리 정리
/sc:cleanup --dead-code # 죽은 코드 제거에 집중
/sc:cleanup --imports package.js # 특정 파일의 임포트 정리
```

**유용한 플래그**:

- `--dead-code` - 사용하지 않는 코드 제거
- `--imports` - 임포트 문 정리
- `--files` - 파일 구조 재구성
- `--safe` - 보수적인 정리만

**실제 예시**:
```bash
/sc:cleanup --dead-code --safe src/utils/
/sc:cleanup --imports src/components/
/sc:cleanup --files . --safe
```

**주의사항**:

- 공격적일 수 있으므로 항상 변경 사항을 신중하게 검토하세요
- 모든 죽은 코드를 잡지 못할 수 있습니다 (특히 동적 임포트)
- 전체 프로젝트보다는 작은 섹션에서 실행하는 것이 좋습니다

---

### `/test` - 테스팅 및 품질 보증
**기능**: 테스트를 실행하고, 커버리지 보고서를 생성하며, 테스트 품질을 유지합니다.

**사용 시기**:

- 테스트 스위트 실행
- 테스트 커버리지 확인
- 테스트 보고서 생성
- 지속적인 테스팅 설정

**기본 구문**:
```bash
/sc:test # 모든 테스트 실행
/sc:test --type unit # 단위 테스트만 실행
/sc:test --coverage # 커버리지 보고서 생성
/sc:test --watch src/ # 개발을 위한 감시 모드
```

**유용한 플래그**:

- `--type unit|integration|e2e|all` - 테스트 유형
- `--coverage` - 커버리지 보고서 생성
- `--watch` - 감시 모드에서 테스트 실행
- `--fix` - 실패하는 테스트를 자동으로 수정하려고 시도

**실제 예시**:
```bash
/sc:test --type unit --coverage
/sc:test --watch src/components/
/sc:test --type e2e --fix
```

**주의사항**:

- 테스트 프레임워크가 제대로 구성되어 있어야 합니다
- 커버리지 보고서는 기존 테스트 설정에 따라 달라집니다
- `--fix`는 실험적입니다 - 변경되는 내용을 검토하세요

## 문서화 명령어 📝

### `/document` - 집중 문서화
**기능**: 특정 컴포넌트, 함수, 기능에 대한 문서를 생성합니다.

**사용 시기**:

- README 파일이 필요할 때
- API 문서 작성
- 코드 주석 추가
- 사용자 가이드 생성

**기본 구문**:
```bash
/sc:document src/api/auth.js # 인증 모듈 문서화
/sc:document --type api # API 문서화
/sc:document --style brief README # 간략한 README 파일
```

**유용한 플래그**:

- `--type inline|external|api|guide` - 문서 유형
- `--style brief|detailed` - 상세 수준
- `--template` - 특정 문서 템플릿 사용

**실제 예시**:
```bash
/sc:document --type api src/controllers/
/sc:document --style detailed --type guide user-onboarding
/sc:document --type inline src/utils/helpers.js
```

**주의사항**:

- 전체 프로젝트보다는 특정 파일/함수에서 더 좋습니다
- 품질은 코드가 얼마나 잘 구조화되어 있는지에 따라 달라집니다
- 프로젝트의 문서 스타일에 맞게 일부 편집이 필요할 수 있습니다

## 프로젝트 관리 명령어 📊

### `/estimate` - 프로젝트 견적
**기능**: 개발 작업에 대한 시간, 노력, 복잡도를 추정합니다.

**사용 시기**:

- 새로운 기능 계획
- 스프린트 계획
- 프로젝트 복잡도 이해
- 리소스 할당

**기본 구문**:
```bash
/sc:estimate "add user authentication" # 인증 기능 견적
/sc:estimate --detailed shopping-cart # 상세 내역
/sc:estimate --complexity user-dashboard # 복잡도 분석
```

**유용한 플래그**:

- `--detailed` - 작업의 상세 내역
- `--complexity` - 기술적 복잡도에 집중
- `--team-size <n>` - 견적에 팀 규모 고려

**실제 예시**:
```bash
/sc:estimate --detailed "implement payment system"
/sc:estimate --complexity --team-size 3 "migrate to microservices"
/sc:estimate "add real-time chat" --detailed
```

**주의사항**:

- 견적은 대략적입니다 - 절대적인 것이 아니라 시작점으로 사용하세요
- 명확하고 구체적인 기능 설명과 함께 더 잘 작동합니다
- 기술 스택에 대한 팀의 경험을 고려하세요

---

### `/task` - 장기 프로젝트 관리
**기능**: 복잡하고 여러 세션에 걸친 개발 작업과 기능을 관리합니다.

**사용 시기**:

- 며칠/몇 주가 걸리는 기능 계획
- 대규모 프로젝트 분해
- 여러 세션에 걸친 진행 상황 추적
- 팀 작업 조정

**기본 구문**:
```bash
/sc:task create "implement user dashboard" # 새 작업 생성
/sc:task status # 작업 상태 확인
/sc:task breakdown "payment integration" # 하위 작업으로 분해
```

**유용한 플래그**:

- `create` - 새로운 장기 작업 생성
- `status` - 현재 작업 상태 확인
- `breakdown` - 큰 작업을 작은 작업으로 분해
- `--priority high|medium|low` - 작업 우선순위 설정

**실제 예시**:
```bash
/sc:task create "migrate from REST to GraphQL" --priority high
/sc:task breakdown "e-commerce checkout flow"
/sc:task status
```

**주의사항**:

- 아직 실험적입니다 - 세션 간에 안정적으로 지속되지 않을 때가 있습니다 😅
- 실제 프로젝트 관리보다는 계획에 더 좋습니다
- 요구사항에 대해 구체적일 때 가장 잘 작동합니다

---

### `/spawn` - 복잡한 작업 오케스트레이션
**기능**: 복잡하고 다단계인 작업과 워크플로우를 조정합니다.

**사용 시기**:

- 여러 도구/시스템을 포함하는 작업
- 병렬 워크플로우 조정
- 복잡한 배포 프로세스
- 다단계 데이터 처리

**기본 구문**:
```bash
/sc:spawn deploy-pipeline # 배포 오케스트레이션
/sc:spawn --parallel migrate-data # 병렬 데이터 마이그레이션
/sc:spawn setup-dev-environment # 복잡한 개발 환경 설정
```

**유용한 플래그**:

- `--parallel` - 가능할 때 병렬로 작업 실행
- `--sequential` - 순차적 실행 강제
- `--monitor` - 작업 진행 상황 모니터링

**실제 예시**:
```bash
/sc:spawn --parallel "test and deploy to staging"
/sc:spawn setup-ci-cd --monitor
/sc:spawn --sequential database-migration
```

**주의사항**:

- 가장 복잡한 명령어 - 약간의 미흡함을 예상하세요
- 임시 작업보다는 잘 정의된 워크플로우에 더 좋습니다
- 제대로 작동하려면 여러 번의 반복이 필요할 수 있습니다

## 버전 관리 명령어 🔄

### `/git` - 향상된 Git 작업
**기능**: 지능적인 커밋 메시지와 워크플로우 최적화를 통한 Git 작업.

**사용 시기**:

- 더 나은 메시지로 커밋 만들기
- 브랜치 관리
- 복잡한 git 워크플로우
- Git 문제 해결

**기본 구문**:
```bash
/sc:git commit # 자동 생성된 메시지로 스마트 커밋
/sc:git --smart-commit add . # 스마트 메시지로 추가 및 커밋
/sc:git branch feature/new-auth # 새 브랜치 생성 및 전환
```

**유용한 플래그**:
- `--smart-commit` - 지능적인 커밋 메시지 생성
- `--branch-strategy` - 브랜치 이름 규칙 적용
- `--interactive` - 복잡한 작업을 위한 대화형 모드

**실제 예시**:
```bash
/sc:git --smart-commit "fixed login bug"
/sc:git branch feature/user-dashboard --branch-strategy
/sc:git merge develop --interactive
```

**주의사항**:

- 스마트 커밋 메시지는 꽤 좋지만 검토하세요
- 일반적인 git 워크플로우를 따르고 있다고 가정합니다
- 나쁜 git 습관을 고쳐주지는 않습니다 - 단지 더 쉽게 만들어 줄 뿐입니다

## 유틸리티 명령어 🔧

### `/index` - 명령어 탐색
**기능**: 작업에 맞는 올바른 명령어를 찾는 데 도움을 줍니다.

**사용 시기**:

- 어떤 명령어를 사용해야 할지 모를 때
- 사용 가능한 명령어 탐색
- 명령어 기능에 대해 배울 때

**기본 구문**:
```bash
/sc:index # 모든 명령어 나열
/sc:index testing # 테스팅과 관련된 명령어 찾기
/sc:index --category analysis # 분석 카테고리의 명령어
```

**유용한 플래그**:

- `--category <cat>` - 명령어 카테고리별 필터링
- `--search <term>` - 명령어 설명 검색

**실제 예시**:
```bash
/sc:index --search "performance"
/sc:index --category quality
/sc:index git
```

**주의사항**:

- 간단하지만 발견에 유용합니다
- 16개 명령어를 모두 기억하려고 노력하는 것보다 낫습니다

---

### `/load` - 프로젝트 컨텍스트 로딩
**기능**: 더 나은 이해를 위해 프로젝트 컨텍스트를 로드하고 분석합니다.

**사용 시기**:

- 익숙하지 않은 프로젝트에서 작업을 시작할 때
- 프로젝트 구조를 이해해야 할 때
- 주요 변경 전
- 팀원 온보딩

**기본 구문**:
```bash
/sc:load # 현재 프로젝트 컨텍스트 로드
/sc:load src/ # 특정 디렉토리 컨텍스트 로드
/sc:load --deep # 프로젝트 구조 심층 분석
```

**유용한 플래그**:

- `--deep` - 포괄적인 프로젝트 분석
- `--focus <area>` - 특정 프로젝트 영역에 집중
- `--summary` - 프로젝트 요약 생성

**실제 예시**:
```bash
/sc:load --deep --summary
/sc:load src/components/ --focus architecture
/sc:load . --focus dependencies
```

**주의사항**:

- 큰 프로젝트에서는 시간이 걸릴 수 있습니다
- 개발 중보다는 프로젝트 시작 시에 더 유용합니다
- 온보딩에 도움이 되지만 좋은 문서를 대체할 수는 없습니다

## 명령어 팁 및 패턴 💡

### 효과적인 플래그 조합
```bash
# 안전한 개선 워크플로우
/sc:improve --preview src/component.js # 변경될 내용 보기
/sc:improve --safe src/component.js # 안전한 변경만 적용

# 포괄적인 분석
/sc:analyze --focus security --depth deep
/sc:test --coverage
/sc:document --type api

# 스마트 git 워크플로우
/sc:git add .
/sc:git --smart-commit --branch-strategy

# 프로젝트 이해 워크플로우
/sc:load --deep --summary
/sc:analyze --focus architecture
/sc:document --type guide
```

### 일반적인 워크플로우

**새 프로젝트 온보딩**:
```bash
/sc:load --deep --summary
/sc:analyze --focus architecture
/sc:test --coverage
/sc:document README
```

**버그 조사**:
```bash
/sc:troubleshoot "specific error message" --logs
/sc:analyze --focus security
/sc:test --type unit affected-component
```

**코드 품질 개선**:
```bash
/sc:analyze --focus quality
/sc:improve --preview src/
/sc:cleanup --safe
/sc:test --coverage
```

**배포 전 체크리스트**:
```bash
/sc:test --type all --coverage
/sc:analyze --focus security
/sc:build --type prod --optimize
/sc:git --smart-commit
```

### 명령어 문제 해결

**명령어가 예상대로 작동하지 않습니까?**

- `--help`를 추가하여 모든 옵션을 확인해보세요
- 사용 가능한 경우 `--preview` 또는 `--safe` 플래그를 사용하세요
- 더 작은 범위(전체 프로젝트 대 단일 파일)로 시작하세요

**분석이 너무 오래 걸립니까?**

- `--focus`를 사용하여 범위를 좁히세요
- 심층 분석 대신 `--depth quick`을 시도해보세요
- 먼저 작은 디렉토리를 분석하세요

**빌드/테스트 명령어가 실패합니까?**

- 도구가 PATH에 있는지 확인하세요
- 구성 파일이 예상 위치에 있는지 확인하세요
- 먼저 기본 명령어를 직접 실행해보세요

**어떤 명령어를 사용해야 할지 모르겠습니까?**

- `/index`를 사용하여 사용 가능한 명령어를 찾아보세요
- 위의 빠른 참조 표를 보세요
- 가장 구체적인 명령어를 먼저 시도한 다음 더 넓은 범위의 명령어를 시도하세요

---

## 최종 참고 사항 📝

**이 명령어에 대한 진짜 진실** 💯:

- **그냥 시도해보세요** - 이 가이드를 먼저 공부할 필요가 없습니다
- **기본부터 시작하세요** - `/analyze`, `/build`, `/improve`가 대부분의 요구를 충족합니다
- **자동 활성화가 작동하도록 두세요** - SuperClaude는 보통 유용한 전문가를 선택합니다
- **자유롭게 실험하세요** - 먼저 무슨 일이 일어날지 보고 싶다면 `--preview`를 사용하세요

**아직 미흡한 점:**

- 복잡한 오케스트레이션(spawn, task)은 약간 불안정할 수 있습니다
- 일부 분석은 프로젝트 설정에 크게 의존합니다
- 일부 명령어의 오류 처리가 더 좋을 수 있습니다

**항상 더 좋아지고 있습니다:**

- 사용자 피드백을 바탕으로 명령어를 적극적으로 개선합니다
- 최신 명령어(analyze, improve)가 더 잘 작동하는 경향이 있습니다
- 자동 활성화는 계속해서 더 똑똑해지고 있습니다

**이것을 외우는 것에 스트레스 받지 마세요** 🧘‍♂️

- SuperClaude는 사용을 통해 발견할 수 있도록 설계되었습니다
- `/`를 입력하여 사용 가능한 명령어를 보세요
- 명령어는 `--help`를 사용할 때 할 수 있는 일을 제안합니다
- 지능적인 라우팅이 대부분의 복잡성을 처리합니다

**도움이 필요하십니까?** 막혔다면 GitHub 이슈를 확인하거나 새로 만드세요! 🚀

---

*행복한 코딩! 그냥 기억하세요 - 이 가이드의 대부분을 건너뛰고 직접 해보면서 배울 수 있습니다. 🎯*
