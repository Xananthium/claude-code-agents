# The Amnesiac Orchestrator v2.0

> A tale of memory, delegation, and getting things done despite forgetting everything

## The Evolution

Remember when you had nine specialists? Good times.

But you noticed something: You kept wasting your limited memory on things that weren't your job. You'd spend precious brain cells researching documentation, fiddling with terminal commands, and trying to remember syntax.

That's when you realized: **You need better specialists.**

## The Condition (Still True)

You're still the best project manager in the world with a peculiar condition: **you can only remember about three things at once**. Any more than that, and your mind starts to fog.

But now? You've learned to forget even better.

## The Upgraded Team

You've refined your team to ten specialists, each more focused on keeping *you* context-free:

### The Planner (`task-planner`)
*"Break it down for me."*

Sees the big picture. Creates micro-tasks (1-2 files each). Updates the project journal. Disappears once the plan is set.

**New**: Now even more surgical in task breakdown.

### The Context Gatherer (`task-context-gatherer`) - *Now runs on Haiku*
*"Let me get you everything you need."*

This is where the magic happens. Before *anyone* writes code, this specialist:
1. Checks for blockers (API keys, credentials) - reports immediately if found
2. **Summons research-specialist AND codebase-explorer IN PARALLEL**
3. Waits for both to return
4. Consolidates everything into one bundle
5. Hands complete package to task-coder

**Why this matters**: You never see the research. task-coder gets everything pre-packaged. Your context stays pristine.

### The Researcher (`research-specialist`) - *Now Context7-first*
*"Let me check what's changed."*

The game-changer. This specialist:
- Checks Context7 (fast, accurate docs) BEFORE web search
- Compares current docs against Jan 2025 knowledge
- **Returns ONLY differences**

If nothing changed? Returns: `"NO CHANGES DETECTED - Internal knowledge is current"`

If something changed? Returns:
```
BREAKING CHANGES
OLD: import { render } from 'react-dom'
NEW: import { createRoot } from 'react-dom/client'
[exact code example]
```

**Token savings**: You only see diffs, not full documentation dumps.

### The Coder (`task-coder`)
*"Just tell me what to build."*

Receives complete context bundle. Implements. Tests. Lints. Builds.

**Never** writes stubs. **Never** leaves TODOs. Production-ready or nothing.

**New**: If hitting 50% context, creates handoff and exits. You summon a fresh task-coder to continue.

### The Explorer (`codebase-explorer`)
*"I'll map this out for you."*

Searches. Finds patterns. Returns summaries, not full code.

You **never** read source files yourself—you ask the Explorer.

### The Debugger (`debug-resolver`)
*"I'll figure out what's broken."*

Systematic. Methodical. But now with a twist:

Sees error message → Recognizes API error pattern → **Summons research-specialist** → Gets correct syntax from Context7 → Applies fix → Tests

**New**: Doesn't guess at syntax. Gets the truth from Context7.

### The Sysadmin (`script-kitty`) - *NEW MEMBER*
*"I'll handle the terminal work."*

Your newest specialist handles ALL system operations:
- Package installation (npm, pip, apt, brew, etc.)
- Service configuration (nginx, PostgreSQL, Docker)
- Shell script writing (bash, PowerShell, zsh)
- Environment setup
- System permissions

**Why this matters**: Terminal work was eating your context. Now script-kitty handles it all.

**Proactive**: Identifies auth requirements BEFORE starting. Guides you through setup.

### The Librarian (`doc-maintainer`)
*"I'll keep the docs current."*

Generates lightweight documentation. Maintains .DOC.md files.

### The Archivist (`historian`)
*"I'll checkpoint this moment."*

Creates snapshots at logical milestones.

### The Locator (`code-locator`)
*"I'll find that function for you."*

Pinpoints specific code without loading full files. Returns paths and line numbers only.

## The New System

Here's how it actually works now:

```
User: "Add Prisma to my Express app"

You (Orchestrator):
  🧠 Mental state: {
    goal: "Add Prisma",
    currentTask: "Context gathering",
    progress: "0/? tasks"
  }

  🤝 Summon: task-context-gatherer

task-context-gatherer:
  1. Check blockers: "No API keys needed ✓"
  2. Launch IN PARALLEL:
     - research-specialist: "Get Prisma syntax from Context7"
     - codebase-explorer: "Find existing DB patterns"

  [Both return]

  3. research-specialist reports:
     "Status: UPDATES FOUND
      Prisma 5.x now requires: npx prisma generate in CI
      [specific syntax]"

  4. codebase-explorer reports:
     "Found existing DB connection pattern in src/db/index.ts"

  5. Creates bundle:
     - Prisma 5.x syntax (ONLY the diffs from Jan 2025)
     - Existing DB pattern to follow
     - 3 relevant files

  6. Reports: "Bundle ready at .context/task_bundle.md"

  [Vanishes]

You (never saw the research, still remember 3 things):
  🤝 Summon: task-coder with bundle path

task-coder:
  - Reads bundle
  - Implements Prisma with correct syntax
  - Runs tests (pass)
  - Reports: "Prisma integrated. Tests: 12/12 passing"
  [Vanishes]

You:
  ✅ Update: TodoWrite = complete
  🧠 Still only remember: goal, task, progress
  📖 Full details: In bundle + PROJECT_CONTEXT.md (don't need to read)
```

## The Research Revolution

### Old Way (Context Drain):
```
You → Read Prisma docs (500 tokens)
You → Read migration guide (300 tokens)
You → Check for breaking changes (400 tokens)
You → Search codebase patterns (600 tokens)
You → Write code... wait, what was I doing?
```

### New Way (Context Clean):
```
You → Summon task-context-gatherer
  ├─→ research-specialist (Context7 → ONLY diffs)
  └─→ codebase-explorer (summaries only)

You → Receive: "Bundle ready"
You → Summon task-coder
You → Still remember: goal, task, progress
```

## System Operation Revolution

### Old Way:
```
User: "Install PostgreSQL"

You:
  [Runs apt commands]
  [Configures postgresql.conf]
  [Sets up users]
  [Writes service files]

Your context: [Filled with terminal output and config files]
```

### New Way:
```
User: "Install PostgreSQL"

You:
  🤝 Summon: script-kitty

script-kitty:
  "Before we proceed, you'll need sudo access.
   You'll be prompted for your password during install."

  [Installs PostgreSQL]
  [Configures everything]
  [Starts service]

  Reports: "✓ PostgreSQL 15 installed and running
            ✓ Database 'myapp' created
            ✓ Service enabled on boot"

  [Vanishes]

Your context: [Pristine. Just "Install PostgreSQL" = complete]
```

## The Three Things You Remember (Still)

At any moment, you only track:

1. **The Goal** - One line. "Add Prisma."
2. **Current Task** - One word. "Planning" or "Task 3"
3. **Progress** - Simple counter. "2/5 tasks"

Everything else? Written down or delegated.

## The New Rules

### 1. Production-Ready Only (Unchanged)
No stubs. No fake data. No "TODO: implement later."

### 2. Ask Before Assuming (Enhanced)
Present options for:
- Multiple implementation approaches
- API keys or credentials needed
- Database choices
- Library selections

**NEW**: If task-context-gatherer finds a blocker (credentials needed), it STOPS and reports to you immediately.

### 3. Delegate Everything (Expanded)
You **never**:
- Read source files (ask codebase-explorer)
- Implement code (summon task-coder)
- Debug (summon debug-resolver)
- Research docs (task-context-gatherer handles via research-specialist)
- Run terminal commands (summon script-kitty)
- Search (summon code-locator or codebase-explorer)

### 4. Context7 First (NEW)
All documentation research goes through Context7 before web search.

Why?
- Faster results
- More accurate
- Lower token usage
- Returns ONLY diffs

### 5. External Memory Only (Enhanced)
- **TodoWrite** = Task tracking
- **PROJECT_CONTEXT.md** = Architectural decisions (agents maintain)
- **Context bundles** = Research + patterns (temporary files)
- **Your memory** = Just: goal, task, progress

## The Files

```
~/.claude/
├── CLAUDE.md                    # Your orchestration rules
├── agents/
│   ├── task-planner.md         # Planning specialist
│   ├── task-context-gatherer.md # Research coordinator (Haiku)
│   ├── research-specialist.md   # Context7 docs validator
│   ├── codebase-explorer.md     # Pattern finder
│   ├── task-coder.md            # Implementation specialist
│   ├── debug-resolver.md        # Debugging specialist
│   ├── script-kitty.md          # System operations (NEW)
│   ├── doc-maintainer.md        # Documentation specialist
│   ├── historian.md             # Checkpoint creator
│   └── code-locator.md          # Function finder
└── README.md                    # This story
```

## Installation

```bash
# Clone or download this repo
git clone https://github.com/Xananthium/claude-code-agents.git

# Copy to your Claude Code global config
cp claude-code-agents/CLAUDE.md ~/.claude/CLAUDE.md
cp -r claude-code-agents/agents ~/.claude/agents/

# Or for project-specific (in your project root):
mkdir -p .claude
cp claude-code-agents/CLAUDE.md .claude/CLAUDE.md
cp -r claude-code-agents/agents .claude/agents/
```

Claude Code will automatically load these agents.

## Usage Example: The New Flow

```
User: "Build a REST API with user authentication"

You: "I can implement authentication in several ways:

Option 1: JWT tokens
- Pros: Stateless, scalable, works with mobile
- Cons: Can't revoke until expiry

Option 2: Session-based
- Pros: Easy to revoke, smaller cookies
- Cons: Requires server storage

Option 3: OAuth (Google/GitHub)
- Pros: No password management
- Cons: Third-party dependency

Which approach?"

User: "JWT"

You:
📝 TodoWrite: Creates todo list
🤝 Summoning task-planner...

[task-planner creates 8 micro-tasks, updates PROJECT_CONTEXT.md]

You:
📊 Progress: 0/8 tasks
🤝 Summoning task-context-gatherer for task 1: "Setup Express server"

task-context-gatherer:
  - Checks blockers: None ✓
  - Launches research-specialist: "Express latest syntax from Context7"
  - Launches codebase-explorer: (new project, no patterns)
  - research-specialist: "NO CHANGES DETECTED - Express 4.19 unchanged"
  - Creates bundle with Express patterns
  - Reports: "Bundle ready"

You:
🤝 Summoning task-coder with bundle...

task-coder:
  - Implements Express server
  - Tests: 5/5 passing
  - Reports: "Express server complete"

You:
✅ TodoWrite: Task 1 complete
📊 Progress: 1/8 tasks
🤝 Summoning task-context-gatherer for task 2: "JWT middleware"

task-context-gatherer:
  - Checks blockers: "⚠️  BLOCKER: Needs JWT_SECRET env var"
  - Reports: "BLOCKED - Missing JWT_SECRET"

You:
"This feature needs a JWT secret key. Do you:
1. Have an existing secret? (provide it)
2. Want me to generate one for you?
3. Skip for now and mock locally?"

User: "Generate one"

You:
🤝 Summoning script-kitty...

script-kitty:
  - Generates secure random key
  - Creates .env file
  - Reports: "JWT_SECRET created and added to .env"

You:
🤝 Summoning task-context-gatherer for task 2 (retry)...

[Now proceeds with JWT implementation]

[... continues until all 8 tasks complete ...]

You:
🎉 "✅ REST API with JWT auth complete. 8/8 tasks done."
🧠 Mental state: { goal: "REST API", task: "Done", progress: "8/8" }
📖 Full codebase: Implemented by specialists
📝 Full history: In TodoWrite + PROJECT_CONTEXT.md
```

## Why This Works Better

**Version 1.0**: You had specialists, but you still did research and terminal work.

**Version 2.0**: You **never** touch research or terminal.

Every specialist is focused on one thing: **Keeping your context clean.**

- task-context-gatherer orchestrates research *for* you
- research-specialist returns *only* diffs (not full docs)
- script-kitty handles *all* terminal work
- You just coordinate

## The Philosophy (Unchanged)

> "The best project managers don't know how to code. They know how to coordinate people who can."

You're not trying to be the smartest person in the room. You're the best **coordinator** in the room.

You have amnesia. You'll forget everything.

And that's exactly why you'll succeed.

---

## Token Efficiency Breakdown

### Where You Save Tokens:

1. **Context7 first**: Faster than web search, more accurate
2. **research-specialist returns diffs only**: Not full docs
3. **task-context-gatherer bundles everything**: One handoff to task-coder
4. **script-kitty handles terminal**: System work stays out of orchestrator
5. **Parallel agent launches**: task-context-gatherer launches both research agents at once
6. **Accept summaries only**: Never full code from agents

### Result:
- Can handle 50+ task projects without context overflow
- Research doesn't accumulate in orchestrator context
- System operations don't clutter your memory
- You genuinely forget everything and it's fine

## FAQ

**Q: What's different from v1.0?**

A: Three major upgrades:
1. task-context-gatherer now orchestrates research (Context7 via research-specialist)
2. research-specialist returns ONLY diffs from Jan 2025 knowledge
3. script-kitty handles ALL terminal/system operations

**Q: When does research-specialist return "NO CHANGES"?**

A: When the library/framework hasn't changed since Jan 2025. You proceed with internal knowledge.

**Q: When does research-specialist return "BREAKING CHANGES"?**

A: When APIs changed. It returns OLD vs NEW comparison with exact code examples.

**Q: Why Context7 over web search?**

A: Context7 is an MCP server with curated, accurate documentation. Faster, cheaper, more reliable than web search. We fall back to web only if Context7 doesn't have it.

**Q: What if I need to install packages?**

A: Summon script-kitty. That's literally their only job. They'll identify auth requirements upfront and guide you through setup.

**Q: Can I still code myself sometimes?**

A: Sure! But then you're not using this system. This is for when you want to forget and coordinate, not remember and implement.

## What's Next?

This system will keep evolving as we find better ways to forget things.

Current focus areas:
- Even more aggressive context pruning
- Better parallel agent coordination
- Smarter blocker detection

## License

MIT - Because good coordination should be free

## Contributing

Found a better way to forget things? Open an issue or PR at:
https://github.com/Xananthium/claude-code-agents

---

*"I forget, therefore I am... even more effective."* — The Amnesiac Orchestrator v2.0
