# Pi Agent Development Workflow

這個 Repository 用來記錄與實驗 **Pi Agent 在實際軟體開發流程中的應用**。

目前主要想法是讓 Pi Agent 先理解既有專案的架構、程式風格與開發規範，整理成可重複使用的 **Skill**，之後再利用這些 Skill 協助進行功能開發、Code Review 與專案維護。

## Workflow

```text
Clone Existing Project
        ↓
Pi Agent Analyze Project
        ↓
Understand
- Project Structure
- Coding Style
- Architecture
- Naming Convention
- API Design
- Database Convention
- Git / Development Rules
        ↓
Generate Development Skills
        ↓
Use Skills for Future Development
        ↓
Implement Feature / Fix Bug / Refactor
```

## 1. Clone Project

首先將既有公司專案 Clone 到本地環境。

```bash
git clone <repository-url>
cd <project>
```

## 2. Let Pi Agent Analyze the Project

讓 Pi Agent 閱讀現有專案，理解目前的開發方式，例如：

- Project structure
- Controller / Service / Repository pattern
- DTO / Entity naming
- Exception handling
- API response format
- Database access pattern
- Logging convention
- Testing style
- Git / branch convention

例如：

```text
Analyze this project and summarize the development conventions.

Focus on:

1. Project architecture
2. Package structure
3. Naming conventions
4. Controller / Service / Repository patterns
5. DTO and Entity conventions
6. Exception handling
7. API response format
8. Database patterns
9. Logging
10. Testing conventions
```

## 3. Generate Skills

將分析結果整理成 Pi Agent 可以重複使用的 Skill。

例如：

```text
skills/
├── backend-development/
│   └── SKILL.md
│
├── api-design/
│   └── SKILL.md
│
├── database/
│   └── SKILL.md
│
└── testing/
    └── SKILL.md
```

Skill 中可以記錄：

```text
Project Convention

Controller
- Only handle HTTP request / response
- Business logic should be placed in Service

Service
- Contains business logic
- Use transaction when necessary

Repository
- Only responsible for database access

Naming
- Request DTO: XxxRequest
- Response DTO: XxxResponse

API
- Follow existing response structure
- Follow existing error code convention
```

## 4. Development with Skills

之後開發新功能時，Pi Agent 不需要每次重新理解整個專案，而是先讀取對應 Skill。

```text
Requirement
    ↓
Load Project Skills
    ↓
Analyze Existing Code
    ↓
Implement Feature
    ↓
Run Tests
    ↓
Review Changes
```

例如：

```text
Implement this feature.

Before coding:

1. Read the project development skills.
2. Follow the existing project architecture.
3. Follow naming and API conventions.
4. Reuse existing components when possible.
5. Run tests after implementation.
6. Review the final diff.
```

## Goal

希望建立一套：

```text
Existing Project
      ↓
Project Knowledge
      ↓
Reusable Skills
      ↓
AI-assisted Development
```

讓 Pi Agent 不只是單純產生程式碼，而是能夠**依照既有專案規範進行開發**。
