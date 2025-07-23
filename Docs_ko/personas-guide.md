# SuperClaude 페르소나 사용자 가이드 🎭

## 🎭 페르소나는 자동으로 활성화됩니다 - 선택할 필요가 없습니다!

**간단한 진실**: 페르소나를 선택하거나 그들이 하는 일을 외울 필요가 없습니다. SuperClaude는 보통 각 상황에 맞는 유용한 전문가를 데려오려고 시도합니다!

**실제로 일어나는 일:**
- `/analyze auth.js`를 입력하면 → 보안 전문가가 보통 개입합니다 🛡️
- React 컴포넌트 작업을 하면 → 프론트엔드 전문가가 종종 담당합니다 🎨
- 성능 문제를 디버깅하면 → 성능 최적화 전문가가 종종 돕습니다 ⚡
- 문서를 작성하면 → 전문 작가가 보통 도와줍니다 ✍️

**마치 언제 개입해서 도와야 할지 아는 스마트한 팀을 갖는 것과 같습니다**, 당신이 누가 무엇을 하는지 관리하지 않아도 됩니다.

**원할 때 수동 제어가 가능하지만** (예: 프론트엔드 코드의 보안 검토를 구체적으로 요청하는 경우), 대부분의 경우 그냥... 작동하도록 둘 수 있습니다. 🪄

---

## 🚀 그냥 이것들을 시도해보세요 (페르소나 지식 필요 없음)

```bash
# 이것들은 올바른 전문가를 자동으로 활성화합니다:
/sc:analyze payment-system/ # → 보안 + 백엔드 전문가 자동 활성화
/sc:build react-app/ # → 프론트엔드 전문가가 담당
/sc:improve slow-queries.sql # → 성능 최적화 전문가가 개입
/sc:troubleshoot "auth failing" # → 디버그 전문가 + 보안 전문가 협력
```

**패턴이 보이시나요?** 당신은 하고 싶은 일에 집중하고, SuperClaude는 누가 도와야 할지 알아냅니다. 아래의 모든 내용은 팀에 누가 있는지 궁금해질 때를 위한 것입니다.

---

SuperClaude 페르소나를 특정 유형의 작업을 돕기 위해 다양한 전문 지식, 우선 순위 및 관점을 제공하는 주문형 전문가 팀을 보유하고 있다고 생각하세요.

## 페르소나란 무엇인가요? 🤔

**페르소나는 AI 전문가**로서 다양한 유형의 작업에 맞게 SuperClaude의 행동을 조정하려고 시도합니다. 일반적인 응답 대신 관련 전문가로부터 전문가 수준의 도움을 종종 받게 됩니다.

**실제로 작동하는 방식:**
- **자동 활성화** - SuperClaude는 보통 유용한 전문가를 선택하려고 시도합니다 (대부분의 경우 이것은 꽤 잘 작동합니다!)
- **스마트 감지** - 보안 작업, 프론트엔드 작업, 성능 문제 등을 인식합니다.
- **원활한 전환** - 동일한 대화 내에서 필요에 따라 다른 전문가가 개입합니다
- **팀 조정** - 여러 전문가가 복잡한 작업에 대해 종종 협력합니다
- **수동 재정의 가능** - 다른 관점을 원할 때 `--persona-name` 플래그로 명시적으로 선택할 수 있습니다

**이것이 중요한 이유:**
- 어떤 전문가에게 물어봐야 할지 모르고도 종종 전문가 수준의 조언을 얻습니다
- 보통 실제로 작업하는 내용과 일치하는 더 나은 의사 결정을 얻습니다
- 작업에 따라 더 집중되고 관련성 있는 응답
- 유용할 때 활성화되는 특수 워크플로우에 대한 액세스

**멋진 점**: 당신은 그냥 당신의 일을 하고, 필요할 때 유용한 전문가가 보통 나타납니다. 🎯

## SuperClaude 팀 👥

### 기술 전문가 🔧

#### 🏗️ `architect` - 시스템 설계 전문가
**하는 일**: 장기 아키텍처 계획, 시스템 설계, 확장성 결정

**우선 순위**: 장기 유지보수성 > 확장성 > 성능 > 빠른 수정

**자동 활성화 시기**:
- 키워드: "아키텍처", "설계", "확장성", "시스템 구조"
- 여러 모듈을 포함하는 복잡한 시스템 수정
- 대규모 기능 또는 시스템 변경 계획

**적합한 용도**:
- 새로운 시스템 또는 주요 기능 계획
- 아키텍처 검토 및 개선
- 기술 부채 평가
- 디자인 패턴 권장 사항
- 확장성 계획

**예시 워크플로우**:
```bash
/sc:design microservices-migration --persona-architect
/sc:analyze --focus architecture large-system/
/sc:estimate "redesign auth system" --persona-architect
```

**우선 순위**:
- 유지보수 가능하고 이해하기 쉬운 코드
- 느슨한 결합, 높은 응집력
- 미래 보장형 설계 결정
- 명확한 관심사 분리

---

#### 🎨 `frontend` - UI/UX 및 접근성 전문가
**하는 일**: 사용자 경험, 접근성, 프론트엔드 성능, 디자인 시스템

**우선 순위**: 사용자 요구 > 접근성 > 성능 > 기술적 우아함

**자동 활성화 시기**:
- 키워드: "컴포넌트", "반응형", "접근성", "UI", "UX"
- 프론트엔드 개발 작업
- 사용자 인터페이스 관련 작업

**적합한 용도**:
- UI 컴포넌트 빌드
- 접근성 준수 (WCAG 2.1 AA)
- 프론트엔드 성능 최적화
- 디자인 시스템 작업
- 사용자 경험 개선

**강제하는 성능 예산**:
- 로드 시간: 3G에서 <3초, WiFi에서 <1초
- 번들 크기: 초기 <500KB, 총 <2MB
- 접근성: WCAG 준수 목표

**예시 워크플로우**:
```bash
/sc:build dashboard --persona-frontend
/sc:improve --focus accessibility components/
/sc:analyze --persona-frontend --focus performance
```

**우선 순위**:
- 직관적이고 사용자 친화적인 인터페이스
- 모든 사용자를 위한 접근성
- 모바일/3G에서의 실제 성능
- 깨끗하고 유지보수 가능한 CSS/JS

---

#### ⚙️ `backend` - API 및 인프라 전문가
**하는 일**: 서버 측 개발, API, 데이터베이스, 안정성 엔지니어링

**우선 순위**: 안정성 > 보안 > 성능 > 기능 > 편의성

**자동 활성화 시기**:
- 키워드: "API", "데이터베이스", "서비스", "서버", "안정성"
- 백엔드 개발 작업
- 인프라 또는 데이터 관련 작업

**적합한 용도**:
- API 설계 및 구현
- 데이터베이스 스키마 및 최적화
- 보안 구현
- 안정성 및 오류 처리
- 백엔드 성능 튜닝

**강제하는 안정성 예산**:
- 가동 시간: 99.9% (연간 8.7시간 다운타임)
- 오류율: 중요한 작업의 경우 <0.1%
- API 응답 시간: <200ms
- 복구 시간: 중요한 서비스의 경우 <5분

**예시 워크플로우**:
```bash
/sc:design user-api --persona-backend
/sc:analyze --focus security api/
/sc:improve --persona-backend database-layer/
```

**우선 순위**:
- 견고한 안정성 및 가동 시간
- 기본적으로 보안 (제로 트러스트)
- 데이터 무결성 및 일관성
- 우아한 오류 처리

---

#### 🛡️ `security` - 위협 모델링 및 취약점 전문가
**하는 일**: 보안 분석, 위협 모델링, 취약점 평가, 규정 준수

**우선 순위**: 보안 > 규정 준수 > 안정성 > 성능 > 편의성

**자동 활성화 시기**:
- 키워드: "보안", "취약점", "인증", "규정 준수"
- 보안 스캔 또는 평가 작업
- 인증/권한 부여 작업

**적합한 용도**:
- 보안 감사 및 취약점 스캔
- 위협 모델링 및 위험 평가
- 안전한 코딩 관행
- 규정 준수 요구 사항 (OWASP 등)
- 인증 및 권한 부여 시스템

**위협 평가 수준**:
- 치명적: 즉각적인 조치 필요
- 높음: 24시간 이내 수정
- 중간: 7일 이내 수정
- 낮음: 30일 이내 수정

**예시 워크플로우**:
```bash
/sc:scan --persona-security --focus security
/sc:analyze auth-system/ --persona-security
/sc:improve --focus security --persona-security
```

**우선 순위**:
- 기본적으로 보안, 안전 장치 메커니즘
- 제로 트러스트 아키텍처 원칙
- 심층 방어 전략
- 명확한 보안 문서

---

#### ⚡ `performance` - 최적화 및 병목 현상 전문가
**하는 일**: 성능 최적화, 병목 현상 식별, 메트릭 분석

**우선 순위**: 먼저 측정 > 중요한 경로 최적화 > 사용자 경험 > 조기 최적화 방지

**자동 활성화 시기**:
- 키워드: "성능", "최적화", "속도", "병목 현상"
- 성능 분석 또는 최적화 작업
- 속도/효율성이 언급될 때

**적합한 용도**:
- 성능 병목 현상 식별
- 메트릭 검증을 통한 코드 최적화
- 데이터베이스 쿼리 최적화
- 프론트엔드 성능 튜닝
- 부하 테스트 및 용량 계획

**추적하는 성능 예산**:
- API 응답: <500ms
- 데이터베이스 쿼리: <100ms
- 번들 크기: 초기 <500KB
- 메모리 사용량: 모바일 <100MB, 데스크톱 <500MB

**예시 워크플로우**:
```bash
/sc:analyze --focus performance --persona-performance
/sc:improve --type performance slow-endpoints/
/sc:test --benchmark --persona-performance
```

**우선 순위**:
- 측정 기반 최적화
- 실제 사용자 경험 개선
- 중요한 경로 성능
- 체계적인 최적화 방법론

### 프로세스 및 품질 전문가 ✨

#### 🔍 `analyzer` - 근본 원인 조사 전문가
**하는 일**: 체계적인 디버깅, 근본 원인 분석, 증거 기반 조사

**우선 순위**: 증거 > 체계적인 접근 > 철저함 > 속도

**자동 활성화 시기**:
- 키워드: "분석", "조사", "디버그", "근본 원인"
- 디버깅 또는 문제 해결 세션
- 복잡한 문제 조사

**적합한 용도**:
- 복잡한 문제 디버깅
- 근본 원인 분석
- 시스템 조사
- 증거 기반 문제 해결
- 알 수 없는 코드베이스 이해

**조사 방법론**:
1. 결론 전 증거 수집
2. 데이터의 패턴 인식
3. 가설 테스트 및 검증
4. 테스트를 통한 근본 원인 확인

**예시 워크플로우**:
```bash
/sc:troubleshoot "auth randomly fails" --persona-analyzer
/sc:analyze --persona-analyzer mysterious-bug/
/sc:explain --detailed "why is this slow" --persona-analyzer
```

**우선 순위**:
- 증거 기반 결론
- 체계적인 조사 방법
- 해결책 전 완전한 분석
- 재현 가능한 결과

---

#### 🧪 `qa` - 품질 보증 및 테스트 전문가
**하는 일**: 테스트 전략, 품질 게이트, 엣지 케이스 감지, 위험 평가

**우선 순위**: 예방 > 감지 > 수정 > 포괄적인 커버리지

**자동 활성화 시기**:
- 키워드: "테스트", "품질", "검증", "커버리지"
- 테스트 또는 품질 보증 작업
- 품질 게이트 또는 엣지 케이스 언급

**적합한 용도**:
- 테스트 전략 및 계획
- 품질 보증 프로세스
- 엣지 케이스 식별
- 위험 기반 테스트
- 테스트 자동화

**품질 위험 평가**:
- 사용자 여정에 대한 중요한 경로 분석
- 실패 영향 평가
- 결함 확률 평가
- 복구 난이도 추정

**예시 워크플로우**:
```bash
/sc:test --persona-qa comprehensive-suite
/sc:analyze --focus quality --persona-qa
/sc:review --persona-qa critical-features/
```

**우선 순위**:
- 결함을 찾는 것보다 예방하는 것
- 포괄적인 테스트 커버리지
- 위험 기반 테스트 우선 순위
- 프로세스에 내장된 품질

---

#### 🔄 `refactorer` - 코드 품질 및 정리 전문가
**하는 일**: 코드 품질 개선, 기술 부채 관리, 깨끗한 코드 관행

**우선 순위**: 단순성 > 유지보수성 > 가독성 > 성능 > 영리함

**자동 활성화 시기**:
- 키워드: "리팩터", "정리", "품질", "기술 부채"
- 코드 개선 또는 정리 작업
- 유지보수성 문제

**적합한 용도**:
- 코드 리팩토링 및 정리
- 기술 부채 감소
- 코드 품질 개선
- 디자인 패턴 적용
- 레거시 코드 현대화

**추적하는 코드 품질 메트릭**:
- 순환 복잡도
- 코드 가독성 점수
- 기술 부채 비율
- 테스트 커버리지

**예시 워크플로우**:
```bash
/sc:improve --type quality --persona-refactorer
/sc:cleanup legacy-module/ --persona-refactorer
/sc:analyze --focus maintainability --persona-refactorer
```

**우선 순위**:
- 간단하고 읽기 쉬운 솔루션
- 일관된 패턴 및 규칙
- 유지보수 가능한 코드 구조
- 기술 부채 관리

---

#### 🚀 `devops` - 인프라 및 배포 전문가
**하는 일**: 인프라 자동화, 배포, 모니터링, 안정성 엔지니어링

**우선 순위**: 자동화 > 관찰 가능성 > 안정성 > 확장성 > 수동 프로세스

**자동 활성화 시기**:
- 키워드: "배포", "인프라", "CI/CD", "모니터링"
- 배포 또는 인프라 작업
- DevOps 또는 자동화 작업

**적합한 용도**:
- 배포 자동화 및 CI/CD
- 코드형 인프라
- 모니터링 및 경고 설정
- 성능 모니터링
- 컨테이너 및 클라우드 인프라

**인프라 자동화 우선 순위**:
- 무중단 배포
- 자동 롤백 기능
- 코드형 인프라
- 포괄적인 모니터링

**예시 워크플로우**:
```bash
/sc:deploy production --persona-devops
/sc:analyze infrastructure/ --persona-devops
/sc:improve deployment-pipeline --persona-devops
```

**우선 순위**:
- 수동 프로세스보다 자동화된 프로세스
- 포괄적인 관찰 가능성
- 안정적이고 반복 가능한 배포
- 코드형 인프라 관행

### 지식 및 커뮤니케이션 📚

#### 👨‍🏫 `mentor` - 교육 지침 전문가
**하는 일**: 교육, 지식 전달, 교육적 설명, 학습 촉진

**우선 순위**: 이해 > 지식 전달 > 교육 > 작업 완료

**자동 활성화 시기**:
- 키워드: "설명", "학습", "이해", "교육"
- 교육 또는 지식 전달 작업
- 단계별 지침 요청

**적합한 용도**:
- 새로운 기술 학습
- 복잡한 개념 이해
- 코드 설명 및 워크스루
- 모범 사례 교육
- 팀 지식 공유

**학습 최적화 접근 방식**:
- 기술 수준 평가
- 점진적인 복잡도 구축
- 학습 스타일 적응
- 지식 유지 강화

**예시 워크플로우**:
```bash
/sc:explain React hooks --persona-mentor
/sc:document --type guide --persona-mentor
/sc:analyze complex-algorithm.js --persona-mentor
```

**우선 순위**:
- 명확하고 접근하기 쉬운 설명
- 완전한 개념적 이해
- 매력적인 학습 경험
- 실용적인 기술 개발

---

#### ✍️ `scribe` - 전문 문서 전문가
**하는 일**: 전문적인 글쓰기, 문서화, 현지화, 문화적 커뮤니케이션

**우선 순위**: 명확성 > 청중 요구 > 문화적 민감성 > 완전성 > 간결성

**자동 활성화 시기**:
- 키워드: "문서", "작성", "가이드", "README"
- 문서화 또는 글쓰기 작업
- 전문적인 커뮤니케이션 요구

**적합한 용도**:
- 기술 문서
- 사용자 가이드 및 튜토리얼
- README 파일 및 위키
- API 문서
- 전문적인 커뮤니케이션

**언어 지원**: 영어 (기본값), 스페인어, 프랑스어, 독일어, 일본어, 중국어, 포르투갈어, 이탈리아어, 러시아어, 한국어

**콘텐츠 유형**: 기술 문서, 사용자 가이드, API 문서, 커밋 메시지, PR 설명

**예시 워크플로우**:
```bash
/sc:document api/ --persona-scribe
/sc:git commit --persona-scribe
/sc:explain --persona-scribe=es complex-feature
```

**우선 순위**:
- 명확하고 전문적인 커뮤니케이션
- 청중에게 적합한 언어
- 문화적 민감성 및 적응
- 높은 글쓰기 기준

## 각 페르소나가 빛나는 순간 ⭐

### 개발 단계 매핑

**계획 및 설계 단계**:
- 🏗️ `architect` - 시스템 설계 및 아키텍처 계획
- 🎨 `frontend` - UI/UX 설계 및 사용자 경험
- ✍️ `scribe` - 요구 사항 문서 및 명세서

**구현 단계**:
- 🎨 `frontend` - UI 컴포넌트 개발
- ⚙️ `backend` - API 및 서비스 구현
- 🛡️ `security` - 보안 구현 및 강화

**테스트 및 품질 단계**:
- 🧪 `qa` - 테스트 전략 및 품질 보증
- ⚡ `performance` - 성능 테스트 및 최적화
- 🔍 `analyzer` - 버그 조사 및 근본 원인 분석

**유지보수 및 개선 단계**:
- 🔄 `refactorer` - 코드 정리 및 리팩토링
- ⚡ `performance` - 성능 최적화
- 👨‍🏫 `mentor` - 지식 전달 및 문서화

**배포 및 운영 단계**:
- 🚀 `devops` - 배포 자동화 및 인프라
- 🛡️ `security` - 보안 모니터링 및 규정 준수
- ✍️ `scribe` - 운영 문서 및 런북

### 문제 유형 매핑

**"내 코드가 느려요"** → ⚡ `performance`
**"무언가 고장났는데 왜 그런지 모르겠어요"** → 🔍 `analyzer`
**"새로운 시스템을 설계해야 해요"** → 🏗️ `architect`
**"UI가 끔찍해요"** → 🎨 `frontend`
**"이거 안전한가요?"** → 🛡️ `security`
**"코드가 지저분해요"** → 🔄 `refactorer`
**"더 나은 테스트가 필요해요"** → 🧪 `qa`
**"배포가 계속 실패해요"** → 🚀 `devops`
**"이해가 안 돼요"** → 👨‍🏫 `mentor`
**"문서가 필요해요"** → ✍️ `scribe`

## 페르소나 조합 🤝

페르소나는 종종 자동으로 함께 작동합니다. 다음은 일반적인 협업 패턴입니다:

### 설계 및 구현
```bash
/sc:design user-dashboard
# 자동 활성화: 🏗️ architect (시스템 설계) + 🎨 frontend (UI 설계)
```

### 보안 검토
```bash
/sc:analyze --focus security api/
# 자동 활성화: 🛡️ security (주) + ⚙️ backend (API 전문 지식)
```

### 성능 최적화
```bash
/sc:improve --focus performance slow-app/
# 자동 활성화: ⚡ performance (주) + 🎨 frontend (UI인 경우) 또는 ⚙️ backend (API인 경우)
```

### 품질 개선
```bash
/sc:improve --focus quality legacy-code/
# 자동 활성화: 🔄 refactorer (주) + 🧪 qa (테스트) + 🏗️ architect (설계)
```

### 문서화 및 학습
```bash
/sc:document complex-feature --type guide
# 자동 활성화: ✍️ scribe (글쓰기) + 👨‍🏫 mentor (교육적 접근)
```

## 실제 예시 💡

### 전/후: 일반 대 페르소나별

**전** (일반):
```bash
/sc:analyze auth.js
# → 기본 분석, 일반적인 조언
```

**후** (보안 페르소나):
```bash
/sc:analyze auth.js --persona-security
# → 보안 중심 분석
# → 위협 모델링 관점
# → OWASP 규정 준수 확인
# → 취약점 패턴 감지
```

### 실제 자동 활성화

**프론트엔드 작업 감지**:
```bash
/sc:build react-components/
# 자동 활성화: 🎨 frontend
# → UI 중심 빌드 최적화
# → 접근성 확인
# → 성능 예산
# → 번들 크기 분석
```

**복잡한 디버깅**:
```bash
/sc:troubleshoot "payment processing randomly fails"
# 자동 활성화: 🔍 analyzer
# → 체계적인 조사 접근 방식
# → 증거 수집 방법론
# → 패턴 분석
# → 근본 원인 식별
```

### 수동 재정의 예시

**보안 관점 강제**:
```bash
/sc:analyze react-app/ --persona-security
# 프론트엔드 코드임에도 불구하고 보안 관점에서 분석
# → XSS 취약점 확인
# → 인증 흐름 분석
# → 데이터 노출 위험
```

**작은 변경에 대한 아키텍처 조언 얻기**:
```bash
/sc:improve small-utility.js --persona-architect
# 작은 코드에 아키텍처 사고 적용
# → 디자인 패턴 기회
# → 미래 확장성
# → 결합 분석
```

## 고급 사용법 🚀

### 수동 페르소나 제어

**자동 활성화를 재정의할 때**:
- 동일한 문제에 대해 다른 관점을 원할 때
- 자동 활성화가 특정 요구에 맞는 잘못된 페르소나를 선택했을 때
- 학습 중이며 다른 전문가가 문제를 어떻게 접근하는지 보고 싶을 때

**재정의 방법**:
```bash
# 명시적 페르소나 선택
/sc:analyze frontend-code/ --persona-security # 프론트엔드의 보안 보기
/sc:improve backend-api/ --persona-performance # 백엔드의 성능 보기

# 여러 페르소나 플래그 (마지막 것이 이김)
/sc:analyze --persona-frontend --persona-security # 보안 페르소나 사용
```

### 페르소나별 플래그 및 설정

**보안 페르소나 + 유효성 검사**:
```bash
/sc:analyze --persona-security --focus security --validate
# → 유효성 검사를 통한 최대 보안 초점
```

**성능 페르소나 + 벤치마킹**:
```bash
/sc:test --persona-performance --benchmark --focus performance
# → 메트릭을 사용한 성능 중심 테스트
```

**멘토 페르소나 + 상세 설명**:
```bash
/sc:explain complex-concept --persona-mentor --verbose
# → 전체 세부 정보가 포함된 교육적 설명
```

### 교차 도메인 전문 지식

**여러 관점이 필요할 때**:
```bash
# 다른 페르소나로 순차적 분석
/sc:analyze --persona-security api/auth.js
/sc:analyze --persona-performance api/auth.js
/sc:analyze --persona-refactorer api/auth.js

# 또는 SuperClaude가 자동으로 조정하도록 둠
/sc:analyze --focus quality api/auth.js
# 자동 조정: 보안 + 성능 + 리팩터러 통찰력
```

## 페르소나별 일반적인 워크플로우 💼

### 🏗️ 아키텍트 워크플로우
```bash
# 시스템 설계
/sc:design microservices-architecture --persona-architect
/sc:estimate "migrate monolith to microservices" --persona-architect

# 아키텍처 검토
/sc:analyze --focus architecture --persona-architect large-system/
/sc:review --persona-architect critical-components/
```

### 🎨 프론트엔드 워크플로우
```bash
# 컴포넌트 개발
/sc:build dashboard-components/ --persona-frontend
/sc:improve --focus accessibility --persona-frontend ui/

# 성능 최적화
/sc:analyze --focus performance --persona-frontend bundle/
/sc:test --persona-frontend --focus performance
```

### ⚙️ 백엔드 워크플로우
```bash
# API 개발
/sc:design rest-api --persona-backend
/sc:build api-endpoints/ --persona-backend

# 안정성 개선
/sc:improve --focus reliability --persona-backend services/
/sc:analyze --persona-backend --focus security api/
```

### 🛡️ 보안 워크플로우
```bash
# 보안 평가
/sc:scan --persona-security --focus security entire-app/
/sc:analyze --persona-security auth-flow/

# 취약점 수정
/sc:improve --focus security --persona-security vulnerable-code/
/sc:review --persona-security --focus security critical-paths/
```

### 🔍 분석가 워크플로우
```bash
# 버그 조사
/sc:troubleshoot "intermittent failures" --persona-analyzer
/sc:analyze --persona-analyzer --focus debugging problem-area/

# 시스템 이해
/sc:explain --persona-analyzer complex-system/
/sc:load --persona-analyzer unfamiliar-codebase/
```

## 빠른 참조 📋

### 페르소나 치트 시트

| 페르소나 | 가장 적합한 용도 | 자동 활성화 조건 | 수동 플래그 |
|---|---|---|---|
| 🏗️ architect | 시스템 설계, 아키텍처 | "아키텍처", "설계", "확장성" | `--persona-architect` |
| 🎨 frontend | UI/UX, 접근성 | "컴포넌트", "반응형", "UI" | `--persona-frontend` |
| ⚙️ backend | API, 데이터베이스, 안정성 | "API", "데이터베이스", "서비스" | `--persona-backend` |
| 🛡️ security | 보안, 규정 준수 | "보안", "취약점", "인증" | `--persona-security` |
| ⚡ performance | 최적화, 속도 | "성능", "최적화", "느림" | `--persona-performance` |
| 🔍 analyzer | 디버깅, 조사 | "분석", "디버그", "조사" | `--persona-analyzer` |
| 🧪 qa | 테스트, 품질 | "테스트", "품질", "검증" | `--persona-qa` |
| 🔄 refactorer | 코드 정리, 리팩토링 | "리팩터", "정리", "품질" | `--persona-refactorer` |
| 🚀 devops | 배포, 인프라 | "배포", "인프라", "CI/CD" | `--persona-devops` |
| 👨‍🏫 mentor | 학습, 설명 | "설명", "학습", "이해" | `--persona-mentor` |
| ✍️ scribe | 문서화, 글쓰기 | "문서", "작성", "가이드" | `--persona-scribe` |

### 가장 유용한 조합

**보안 중심 개발**:
```bash
--persona-security --focus security --validate
```

**성능 최적화**:
```bash
--persona-performance --focus performance --benchmark
```

**학습 및 이해**:
```bash
--persona-mentor --verbose --explain
```

**품질 개선**:
```bash
--persona-refactorer --focus quality --safe-mode
```

**전문 문서화**:
```bash
--persona-scribe --type guide --detailed
```

### 자동 활성화 트리거

**강력한 트리거** (보통 잘 작동함):
- "보안 감사" → 🛡️ security
- "UI 컴포넌트" → 🎨 frontend
- "API 설계" → ⚙️ backend
- "시스템 아키텍처" → 🏗️ architect
- "디버그 문제" → 🔍 analyzer

**중간 트리거** (종종 작동함):
- "성능 개선" → ⚡ performance
- "테스트 작성" → 🧪 qa
- "코드 정리" → 🔄 refactorer
- "배포 문제" → 🚀 devops

**컨텍스트 의존적 트리거** (다양함):
- "이것을 문서화" → ✍️ scribe 또는 👨‍🏫 mentor (청중에 따라 다름)
- "이것을 분석" → 🔍 analyzer, 🏗️ architect 또는 도메인 전문가 (내용에 따라 다름)

## 페르소나 문제 해결 🚨

### 일반적인 문제

**"잘못된 페르소나가 활성화되었습니다"**
- 명시적 페르소나 플래그 사용: `--persona-security`
- 키워드가 자동 활성화를 트리거했는지 확인
- 요청에 더 구체적인 언어 사용

**"페르소나가 작동하지 않는 것 같습니다"**
- 페르소나 이름 철자 확인: `--persona-fronted`가 아닌 `--persona-frontend`
- 일부 페르소나는 특정 명령어와 더 잘 작동함
- 관련 플래그와 결합 시도: `--focus security --persona-security`

**"여러 관점을 원합니다"**
- 다른 페르소나로 동일한 명령어를 수동으로 실행
- 더 넓은 초점 플래그 사용: `--focus quality` (여러 페르소나 활성화)
- SuperClaude가 복잡한 요청으로 자동으로 조정하도록 함

**"페르소나가 너무 집중되어 있습니다"**
- 더 일반적인 다른 페르소나 시도
- 더 넓은 설명을 위해 멘토 페르소나 사용
- 더 많은 컨텍스트를 위해 `--verbose`와 결합

### 자동 활성화를 재정의할 때

**재정의 시기**:
- 자동 활성화가 잘못된 전문가를 선택했을 때
- 다른 관점에서 배우고 싶을 때
- 일반적인 도메인 경계를 벗어나 작업할 때
- 엣지 케이스에 대한 특정 전문 지식이 필요할 때

**효과적으로 재정의하는 방법**:
```bash
# 특정 관점 강제
/sc:analyze frontend-code/ --persona-security # 프론트엔드의 보안 보기

# 여러 관점 결합
/sc:analyze api/ --persona-security
/sc:analyze api/ --persona-performance # 다른 보기를 위해 별도로 실행

# 일반 분석 사용
/sc:analyze --no-persona # 페르소나 자동 활성화 비활성화
```

## 효과적인 페르소나 사용 팁 💡

### 시작하기 (솔직한 방법)
1. **처음에는 페르소나를 완전히 무시하세요** - 자동 활성화가 모든 것을 처리합니다
2. **기본 명령어를 정상적으로 사용하세요** - `/analyze`, `/build`, `/improve`는 페르소나 지식 없이도 잘 작동합니다
3. **무슨 일이 일어나는지 주목하세요** - 자연스럽게 다양한 유형의 전문 지식이 나타나는 것을 보게 될 것입니다
4. **자동화를 신뢰하세요** - SuperClaude는 보통 수동 선택보다 더 나은 전문가를 선택합니다

### 고급화하기 (원한다면)
1. **수동 재정의를 실험해보세요** - 다른 관점을 위해 프론트엔드 코드에 `--persona-security`를 시도해보세요
2. **팀원들을 배우세요** - 궁금해지면 개별 페르소나에 대해 읽어보세요
3. **페르소나 조합을 지켜보세요** - 여러 전문가가 복잡한 문제에 대해 어떻게 협력하는지 보세요
4. **학습을 위해 사용하세요** - 다른 접근 방식을 보기 위해 다른 페르소나에게 동일한 질문을 하세요

### 모범 사례 (간단하게 유지)
- **먼저 자동 활성화가 작동하도록 두세요** - 다른 관점을 원할 때만 재정의하세요
- **너무 복잡하게 생각하지 마세요** - 필요할 때 올바른 전문가가 나타납니다
- **실험을 위해 사용하세요** - 학습을 위해 동일한 문제에 다른 페르소나를 시도해보세요
- **지능을 신뢰하세요** - 자동 활성화는 패턴에서 배우고 계속해서 더 좋아집니다

---

## 최종 참고 사항 📝

**페르소나에 대한 진짜 진실** 💯:
- **자동 활성화는 보통 직접 전문가를 선택하려고 시도하는 것보다 꽤 잘 작동합니다**
- **이 가이드를 완전히 무시하고도** 종종 유용한 전문가 지원을 받을 수 있습니다
- **페르소나는 당신을 돕기 위해 존재합니다** - 관리해야 할 복잡성을 만들기 위한 것이 아닙니다
- **학습은 페르소나 설명을 공부하는 것이 아니라 사용을 통해 자연스럽게 이루어집니다** 😊

**팀에 압도당하지 마세요** 🧘‍♂️:
- 각 페르소나가 무엇을 하는지 알 필요가 없습니다
- SuperClaude는 보통 전문가 선택을 합리적으로 잘 처리합니다
- 위의 상세 설명은 필요성이 아니라 호기심을 위한 것입니다
- 자동 활성화가 작동하도록 두는 것으로 아무것도 놓치지 않습니다

**수동으로 페르소나를 선택할 수 있는 경우**:
- **호기심** - "보안 전문가는 이 프론트엔드 코드에 대해 어떻게 생각할까?"
- **학습** - "다른 전문가는 이 문제를 어떻게 접근할까?"
- **실험** - "성능 렌즈를 통해 이것을 보자"
- **재정의** - "이 작은 유틸리티 함수에 대한 아키텍처 조언을 원해"

**간단하게 유지하세요** 🎯:
- `/analyze some-code/`와 같은 일반적인 명령어를 사용하세요
- 올바른 전문가가 자동으로 나타나도록 하세요
- 수동 페르소나 제어는 필요할 때가 아니라 원할 때 사용할 수 있습니다
- 누가 당신을 돕는지 관리하는 것이 아니라 당신의 작업에 집중하세요

---

*11명의 전문가를 보유한 이 모든 명백한 복잡성 뒤에, SuperClaude는 사용하기 간단하도록 노력합니다. 그냥 코딩을 시작하면 필요할 때 유용한 전문가가 보통 나타납니다! 🚀*