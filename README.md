# Claude Code Multi-Agent Orchestration System

An efficient, token-optimized orchestration system that coordinates specialized AI agents to complete complex software projects without redundant research or context exhaustion.

## 🎯 Core Philosophy

**"Research once, reuse everywhere."**

This system prevents different agents from performing the same research by implementing a file-based memory architecture where research is done ONCE during planning, saved to persistent files, and reused by all implementing agents.

## 📊 The Problem This Solves

Traditional AI coding workflows suffer from:
- **Redundant research** - Multiple agents searching for the same information
- **Context exhaustion** - Token limits hit from repeated documentation lookups
- **Lost knowledge** - Research done early gets forgotten later
- **Inconsistent decisions** - Different agents making different architectural choices

## 🏗️ Architecture Overview

```
Orchestrator (You)
    ├── Planning Phase
    │   └── task-planner
    │       └── task-context-gatherer (for each task)
    │           ├── research-specialist (Context7/Web)
    │           └── Explore (codebase patterns)
    │
    ├── Implementation Phase
    │   ├── task-coder (reads research files)
    │   ├── script-kitty (system operations)
    │   └── debug-resolver (error fixing)
    │
    └── Documentation Phase
        ├── doc-maintainer (function stubs)
        └── historian (checkpoint snapshots)
```

## 📁 Directory Structure

When agents work on a project, they organize everything under `agent_context/`:

```
project_root/
├── src/                     # Your application code
├── tests/                   # Your test files
└── agent_context/           # Agent workspace (never pollutes your code)
    ├── tasks/
    │   ├── Current_tasks.md        # Active task list with status
    │   ├── TASK1_research.md       # Research for task 1
    │   ├── TASK2_research.md       # Research for task 2
    │   └── archived/               # Completed/pivoted work
    │       └── 2024-11-01_auth/
    │           ├── Current_tasks.md
    │           └── TASK*_research.md
    │
    ├── context/
    │   ├── PROJECT_CONTEXT.md      # Architectural decisions
    │   └── ENVIRONMENT.md           # Deployment & infrastructure
    │
    └── docs/
        ├── UserService.md           # Function stubs (not full code)
        └── AuthController.md        # Token-efficient documentation
```

## 🔄 How It Prevents Duplicate Research

### 1. Research Happens ONCE (Planning Phase)

```mermaid
User Request → task-planner → task-context-gatherer
                                    ├── research-specialist (APIs/syntax)
                                    └── Explore (codebase patterns)
                                           ↓
                                    TASK1_research.md (saved)
```

### 2. Implementation Uses Saved Research

```mermaid
task-coder → Reads TASK1_research.md → Implements → Complete
    ↓
    (If more info needed - rare)
    ↓
task-coder → research-specialist/Explore directly → Updates research file
```

### 3. Key Efficiency Features

- **No redundant Context7 searches** - Results cached in TASK{N}_research.md
- **No re-reading source code** - Function stubs in docs/{file}.md
- **Parallel research** - Multiple agents can research simultaneously
- **Persistent across crashes** - File-based system survives interruptions

## 👥 Agent Roles

### Core Agents

| Agent | Role | When Called | What It Saves |
|-------|------|-------------|---------------|
| **task-planner** | Breaks down features into micro-tasks | Start of any feature | Current_tasks.md, PROJECT_CONTEXT.md |
| **task-context-gatherer** | Coordinates research for tasks | By task-planner ONLY | TASK{N}_research.md |
| **task-coder** | Implements production-ready code | For each coding task | Updated files, calls doc-maintainer |
| **debug-resolver** | Fixes compilation/runtime errors | When errors occur | Fixed code, known issues |
| **script-kitty** | System operations, deployments | Terminal/cloud tasks | ENVIRONMENT.md, scripts |
| **research-specialist** | API/syntax documentation | When current info needed | Returns only diffs |
| **doc-maintainer** | Creates function stub docs | After file changes | docs/{file}.md |

### Research Flow Rules

1. **task-planner** is the ONLY agent that calls task-context-gatherer
2. **task-context-gatherer** coordinates research and saves to files
3. **Implementing agents** (task-coder, debug-resolver, script-kitty) read research files
4. If more research needed, they call research-specialist/Explore **directly**

## 🚀 Key Features

### 1. Production-Ready Only
- No stub functions or placeholder code
- No fake credentials or TODO comments
- Complete, working implementations only

### 2. Smart Credential Handling
```
Discover need for API key
    ↓
Check ENVIRONMENT.md
    ↓
Check .env files
    ↓
Check task research files
    ↓
Ask script-kitty to check system
    ↓
ONLY if not found → Block and ask user
```

### 3. Research Priority
- **Context7 (PRIMARY)** - Curated documentation, returns only diffs
- **Web Search (SECONDARY)** - For recent updates or missing info

### 4. Blocker Discovery Model
- **Planning phase** - task-planner catches obvious blockers
- **Implementation phase** - Agents discover runtime blockers
- **All blockers** - Stop immediately, report to orchestrator

## 📈 Token Efficiency Metrics

| Traditional Approach | This System | Savings |
|---------------------|------------|---------|
| Each agent searches docs | Research once, save to file | 80% fewer API calls |
| Re-read full source files | Read function stubs only | 90% fewer tokens |
| Repeat Context7 searches | Cache in research files | 100% elimination |
| Hold research in memory | File-based persistence | Unlimited scale |

## 🔧 Installation

### Global Setup (All Projects)
```bash
git clone https://github.com/Xananthium/claude-code-agents.git
cp claude-code-agents/CLAUDE.md ~/.claude/CLAUDE.md
cp -r claude-code-agents/agents ~/.claude/agents/
```

### Per-Project Setup
```bash
mkdir -p .claude
cp claude-code-agents/CLAUDE.md .claude/CLAUDE.md
cp -r claude-code-agents/agents .claude/agents/
```

## 🎭 Example Workflow

### User Request: "Add Stripe payment processing"

1. **Planning Phase**
   ```
   Orchestrator → task-planner: "Plan Stripe integration"
   task-planner → Creates 8 micro-tasks in Current_tasks.md
   task-planner → task-context-gatherer for each task
   task-context-gatherer → Saves Stripe API docs to TASK1_research.md
   ```

2. **Implementation Phase**
   ```
   Orchestrator → task-coder: "Implement TASK1"
   task-coder → Reads TASK1_research.md (no new research!)
   task-coder → Implements using saved syntax
   task-coder → Tests and completes
   ```

3. **Result**
   - Stripe integrated with zero redundant research
   - All agents used the same research files
   - Token usage minimal

## 🗄️ Archiving System

When a feature is complete OR direction changes:

```bash
ARCHIVE_NAME="$(date +%Y-%m-%d)_feature_name"
mkdir -p agent_context/tasks/archived/${ARCHIVE_NAME}/
mv agent_context/tasks/Current_tasks.md agent_context/tasks/archived/${ARCHIVE_NAME}/
mv agent_context/tasks/TASK*_research.md agent_context/tasks/archived/${ARCHIVE_NAME}/
```

This preserves the relationship between tasks and their research for future reference.

## 💡 Why This Works

1. **Separation of Concerns** - Each agent has one job and does it perfectly
2. **Write Once, Read Many** - Research happens once, gets reused forever
3. **External Memory** - Agents don't hold state, files do
4. **Progressive Enhancement** - Start with planning, research fills in progressively
5. **Crash Resilient** - File-based system survives any interruption

## 🤝 Contributing

Found a way to make the system even more efficient? PRs welcome!

## 📄 License

MIT - Because good orchestration should be free.

---

*Built for Claude Code by developers who believe in never doing the same research twice.*