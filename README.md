# plugin-creator

> "플러그인 만들어줘"라고 말하면 Claude Code 플러그인을 대화형으로 만들어주는 메타 플러그인

## 설치

```bash
# 1. 마켓플레이스 추가
/plugin marketplace add yongbin-lab/plugin-creator

# 2. 플러그인 설치
/plugin install plugin-creator@yongbin-lab-plugins
```

또는 로컬에서 바로 테스트:

```bash
claude --plugin-dir ./plugin-creator
```

## 사용법

### 자동 트리거 (Skill)

Claude에게 자연스럽게 말하면 자동으로 플러그인 생성을 시작합니다:

- "코드 리뷰 해주는 플러그인 만들어줘"
- "git 커밋 메시지 자동 생성 플러그인 만들고 싶어"
- "I want to create a plugin that formats code on save"

### 직접 호출 (Command)

```bash
/plugin-creator:create <설명>
```

예시:
```bash
/plugin-creator:create API 테스트 자동화 플러그인
```

## 동작 흐름

1. 사용자의 설명에서 요구사항 파악 (이름, 목적, 필요 컴포넌트)
2. 플러그인 구조를 보여주고 확인
3. 모든 파일 생성 (plugin.json, commands, skills, agents, hooks 등)
4. 테스트 방법 안내

## 플러그인 구조

```
plugin-creator/
├── .claude-plugin/
│   └── plugin.json
├── commands/
│   └── create.md
└── skills/
    └── create-plugin/
        ├── SKILL.md
        └── references/
            └── plugin-structure.md
```

## 라이선스

MIT
