# SuperClaude v3 🚀
[![Website Preview](https://img.shields.io/badge/Visit-Website-blue?logo=google-chrome)](https://superclaude-org.github.io/SuperClaude_Website/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PyPI version](https://img.shields.io/pypi/v/SuperClaude.svg)](https://pypi.org/project/SuperClaude/)
[![Version](https://img.shields.io/badge/version-3.0.0-blue.svg)](https://github.com/NomenAK/SuperClaude)
[![GitHub issues](https://img.shields.io/github/issues/NomenAK/SuperClaude)](https://github.com/NomenAK/SuperClaude/issues)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/NomenAK/SuperClaude/blob/master/CONTRIBUTING.md)
[![Contributors](https://img.shields.io/github/contributors/NomenAK/SuperClaude)](https://github.com/NomenAK/SuperClaude/graphs/contributors)
[![Website](https://img.shields.io/website?url=https://superclaude-org.github.io/SuperClaude_Website/)](https://superclaude-org.github.io/SuperClaude_Website/)

Claude Code를 특화된 명령어, 페르소나, MCP 서버 통합으로 확장하는 프레임워크입니다.

**📢 상태**: 초기 릴리스, 베타 버전에서 막 벗어났습니다! 계속 개선 중이므로 버그가 발생할 수 있습니다.

## SuperClaude란 무엇인가요? 🤔

SuperClaude는 다음과 같은 기능을 추가하여 Claude Code를 개발 작업에 더 유용하게 만들려고 시도합니다:
- 🛠️ **16개의 특화된 명령어** (일부는 다른 것보다 더 잘 작동합니다!)
- 🎭 **스마트 페르소나**는 보통 다른 도메인에 맞는 올바른 전문가를 선택합니다
- 🔧 **MCP 서버 통합**은 문서, UI 컴포넌트, 브라우저 자동화를 위한 것입니다
- 📋 **작업 관리**는 진행 상황을 추적하려고 시도합니다
- ⚡ **토큰 최적화**는 더 긴 대화를 돕습니다

이것이 우리가 개발 워크플로우를 더 원활하게 만들기 위해 구축해 온 것입니다. 아직 미흡한 점이 있지만, 점점 더 좋아지고 있습니다! 😊

## 현재 상태 📊

✅ **잘 작동하는 것:**
- 설치 스위트 (처음부터 다시 작성됨)
- 9개의 문서 파일을 포함한 핵심 프레임워크
- 다양한 개발 작업을 위한 16개의 슬래시 명령어
- MCP 서버 통합 (Context7, Sequential, Magic, Playwright)
- 쉬운 설정을 위한 통합 CLI 설치 프로그램

⚠️ **알려진 문제:**
- 이것은 초기 릴리스입니다 - 버그가 예상됩니다
- 일부 기능이 아직 완벽하게 작동하지 않을 수 있습니다
- 문서는 아직 개선 중입니다
- 후크 시스템이 제거되었습니다 (v4에서 다시 돌아올 예정)

## 주요 기능 ✨

### 명령어 🛠️
가장 일반적인 작업을 위해 16개의 필수 명령어에 집중했습니다:

**개발**: `/sc:implement`, `/sc:build`, `/sc:design`
**분석**: `/sc:analyze`, `/sc:troubleshoot`, `/sc:explain`
**품질**: `/sc:improve`, `/sc:test`, `/sc:cleanup`
**기타**: `/sc:document`, `/sc:git`, `/sc:estimate`, `/sc:task`, `/sc:index`, `/sc:load`, `/sc:spawn`

### 스마트 페르소나 🎭
관련성이 있을 때 개입하려고 시도하는 AI 전문가:
- 🏗️ **architect** - 시스템 설계 및 아키텍처 관련
- 🎨 **frontend** - UI/UX 및 접근성
- ⚙️ **backend** - API 및 인프라
- 🔍 **analyzer** - 디버깅 및 문제 파악
- 🛡️ **security** - 보안 문제 및 취약점
- ✍️ **scribe** - 문서 및 글쓰기
- *...그리고 5명의 추가 전문가*

*(항상 완벽하게 선택하지는 않지만, 보통은 맞습니다!)*

### MCP 통합 🔧
유용할 때 연결되는 외부 도구:
- **Context7** - 공식 라이브러리 문서 및 패턴 가져오기
- **Sequential** - 복잡한 다단계 사고 지원
- **Magic** - 최신 UI 컴포넌트 생성
- **Playwright** - 브라우저 자동화 및 테스트 관련

*(제대로 연결되면 꽤 잘 작동합니다! 🤞)*

## ⚠️ v2에서 업그레이드하시나요? 중요!

SuperClaude v2에서 오셨다면 먼저 정리해야 합니다:

1. **v2 제거** (사용 가능한 경우 제거 프로그램 사용)
2. **수동 정리** - 다음이 존재하면 삭제하세요:
   - `SuperClaude/`
   - `~/.claude/shared/`
   - `~/.claude/commands/`
   - `~/.claude/CLAUDE.md`
4. **그런 다음** 아래의 v3 설치를 진행하세요

이는 v3가 다른 구조를 가지고 있고 이전 파일이 충돌을 일으킬 수 있기 때문입니다.

### 🔄 **v2 사용자를 위한 주요 변경 사항**
**/build` 명령어가 변경되었습니다!** v2에서는 `/build`가 기능 구현에 사용되었습니다. v3에서는:
- `/sc:build` = 컴파일/패키징 전용
- `/sc:implement` = 기능 구현 (NEW!)

**마이그레이션**: `v2 /build myFeature`를 `v3 /sc:implement myFeature`로 바꾸세요

## 설치 📦

SuperClaude 설치는 **2단계 프로세스**입니다:
1. 먼저 Python 패키지를 설치합니다
2. 그런 다음 설치 프로그램을 실행하여 Claude Code 통합을 설정합니다

### 1단계: 패키지 설치

**옵션 A: PyPI에서 (권장)**
```bash
uv add SuperClaude
```

**옵션 B: 소스에서**
```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude
uv sync
```
### 🔧 UV / UVX 설정 가이드

SuperClaude v3는 [`uv`](https://github.com/astral-sh/uv) (더 빠르고 현대적인 Python 패키지 관리자) 또는 크로스 플랫폼 사용을 위한 `uvx`를 통한 설치도 지원합니다.

### 🌀 `uv`로 설치

`uv`가 설치되어 있는지 확인하세요:

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 또는 [https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)의 지침을 따르세요

`uv`가 사용 가능하면 다음과 같이 SuperClaude를 설치할 수 있습니다:

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ `uvx`로 설치 (크로스 플랫폼 CLI)

`uvx`를 사용하는 경우 다음을 실행하세요:

```bash
uvx pip install SuperClaude
```

### ✅ 설치 완료

설치 후 일반적인 설치 단계를 계속 진행하세요:

```bash
python3 -m SuperClaude install
```

또는 bash 스타일 CLI 사용:

```bash
SuperClaude install
```

### 🧠 참고:

* `uv`는 더 나은 캐싱과 성능을 제공합니다.
* Python 3.8+와 호환되며 SuperClaude와 원활하게 작동합니다.

---
**Python이 없나요?** 먼저 Python 3.7+를 설치하세요:
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS
brew install python3

# Windows
# https://python.org/downloads/에서 다운로드
```

### 2단계: 설치 프로그램 실행

패키지를 설치한 후 SuperClaude 설치 프로그램을 실행하여 Claude Code를 구성하세요 (어떤 방법이든 사용할 수 있습니다):
### ⚠️ 중요 참고
**SuperClaude 설치 후.**
**`SuperClaude commands`
, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다**
```bash
# 빠른 설정 (대부분의 사용자에게 권장)
python3 SuperClaude install

# 대화형 선택 (컴포넌트 선택)
python3 SuperClaude install --interactive

# 최소 설치 (핵심 프레임워크만)
python3 SuperClaude install --minimal

# 개발자 설정 (모든 것 포함)
python3 SuperClaude install --profile developer

# 사용 가능한 모든 옵션 보기
python3 SuperClaude install --help
```
### 또는 Python 모듈식 사용
```bash
# 빠른 설정 (대부분의 사용자에게 권장)
python3 -m SuperClaude install

# 대화형 선택 (컴포넌트 선택)
python3 -m SuperClaude install --interactive

# 최소 설치 (핵심 프레임워크만)
python3 -m SuperClaude install --minimal

# 개발자 설정 (모든 것 포함)
python3 -m SuperClaude install --profile developer

# 사용 가능한 모든 옵션 보기
python3 -m SuperClaude install --help
```
### 간단한 bash 명령어 사용
```bash
# 빠른 설정 (대부분의 사용자에게 권장)
SuperClaude install

# 대화형 선택 (컴포넌트 선택)
SuperClaude install --interactive

# 최소 설치 (핵심 프레임워크만)
SuperClaude install --minimal

# 개발자 설정 (모든 것 포함)
SuperClaude install --profile developer

# 사용 가능한 모든 옵션 보기
SuperClaude install --help
```

**이게 다입니다! 🎉** 설치 프로그램이 프레임워크 파일, MCP 서버, Claude Code 구성을 모두 처리합니다.

## 작동 방식 🔄

SuperClaude는 다음을 통해 Claude Code를 향상시키려고 시도합니다:

1. **프레임워크 파일** - Claude가 응답하는 방식을 안내하는 `~/.claude/`에 설치된 문서
2. **슬래시 명령어** - 다양한 개발 작업을 위한 16개의 특화된 명령어
3. **MCP 서버** - 추가 기능을 추가하는 외부 서비스 (작동할 때!)
4. **스마트 라우팅** - 당신이 하는 일에 따라 올바른 도구와 전문가를 선택하려고 시도합니다

대부분의 경우 Claude Code의 기존 기능과 잘 어울립니다. 🤝

## v4에 추가될 내용 🔮

다음 버전을 위해 다음 사항들을 작업할 예정입니다:
- **후크 시스템** - 이벤트 기반 기능 (v3에서 제거됨, 제대로 재설계하려고 노력 중)
- **MCP 스위트** - 더 많은 외부 도구 통합
- **더 나은 성능** - 더 빠르고 버그가 적도록 노력 중
- **더 많은 페르소나** - 아마도 몇 명의 도메인 전문가 추가
- **교차 CLI 지원** - 다른 AI 코딩 도우미와 작동할 수 있음

*(타임라인에 대한 약속은 없습니다 - 아직 v3를 파악 중입니다! 😅)*

## 구성 ⚙️

설치 후 다음을 편집하여 SuperClaude를 사용자 정의할 수 있습니다:
- `~/.claude/settings.json` - 주 구성
- `~/.claude/*.md` - 프레임워크 동작 파일

대부분의 사용자는 아마 아무것도 변경할 필요가 없을 것입니다 - 보통 기본적으로 잘 작동합니다. 🎛️

## 문서 📖

더 배우고 싶으신가요? 저희 가이드를 확인하세요:

- 📚 [**사용자 가이드**](https://github.com/NomenAK/SuperClaude/blob/master/Docs/superclaude-user-guide.md) - 전체 개요 및 시작하기
- 🛠️ [**명령어 가이드**](https://github.com/NomenAK/SuperClaude/blob/master/Docs/commands-guide.md) - 모든 16개 슬래시 명령어 설명
- 🏳️ [**플래그 가이드**](https://github.com/NomenAK/SuperClaude/blob/master/Docs/flags-guide.md) - 명령어 플래그 및 옵션
- 🎭 [**페르소나 가이드**](https://github.com/NomenAK/SuperClaude/blob/master/Docs/personas-guide.md) - 페르소나 시스템 이해
- 📦 [**설치 가이드**](https://github.com/NomenAK/SuperClaude/blob/master/Docs/installation-guide.md) - 상세 설치 지침

이 가이드들은 이 README보다 더 자세한 내용을 담고 있으며 최신 상태로 유지됩니다.

## 기여 🤝

기여를 환영합니다! 도움이 필요한 분야:
- 🐛 **버그 보고** - 무엇이 깨졌는지 알려주세요
- 📝 **문서** - 더 잘 설명할 수 있도록 도와주세요
- 🧪 **테스트** - 다양한 설정에 대한 더 많은 테스트 커버리지
- 💡 **아이디어** - 새로운 기능이나 개선 제안

코드베이스는 매우 간단한 Python + 문서 파일입니다.

## 프로젝트 구조 📁

```
SuperClaude/
├── setup.py               # pypi 설정 파일
├── SuperClaude/           # 프레임워크 파일
│   ├── Core/              # 동작 문서 (COMMANDS.md, FLAGS.md 등)
│   ├── Commands/          # 16개 슬래시 명령어 정의
│   └── Settings/          # 구성 파일
├── setup/                 # 설치 시스템
└── profiles/              # 설치 프로필 (quick, minimal, developer)
```

## 아키텍처 노트 🏗️

v3 아키텍처는 다음에 중점을 둡니다:
- **단순성** - 가치를 더하지 않는 복잡성 제거
- **신뢰성** - 더 나은 설치 및 더 적은 파괴적인 변경
- **모듈성** - 원하는 구성 요소만 선택
- **성능** - 더 스마트한 캐싱으로 더 빠른 작업

v2에서 많은 것을 배웠고 주요 문제점을 해결하려고 노력했습니다.

## FAQ 🙋

**Q: 왜 후크 시스템이 제거되었나요?**
A: 복잡하고 버그가 많아지고 있었습니다. v4를 위해 제대로 재설계하고 있습니다.

**Q: 다른 AI 도우미와 작동하나요?**
A: 현재는 Claude Code만 지원하지만, v4는 더 넓은 호환성을 가질 것입니다.

**Q: 일상적인 사용에 충분히 안정적인가요?**
A: 기본적인 것들은 꽤 잘 작동하지만, 새로운 릴리스이므로 약간의 미흡한 점을 예상해야 합니다. 실험용으로는 괜찮을 것입니다! 🧪

## SuperClaude 기여자

[![Contributors](https://contrib.rocks/image?repo=NomenAk/SuperClaude)](https://github.com/NomenAK/SuperClaude/graphs/contributors)

## 라이선스

MIT - [자세한 내용은 LICENSE 파일 참조](https://opensource.org/licenses/MIT)

## 스타 히스토리

<a href="https://www.star-history.com/#NomenAK/SuperClaude&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=NomenAK/SuperClaude&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=NomenAK/SuperClaude&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=NomenAK/SuperClaude&type=Date" />
 </picture>
</a>
---

*일반적인 응답에 지친 개발자들이 만들었습니다. 유용하게 사용하시길 바랍니다! 🙂*

---
