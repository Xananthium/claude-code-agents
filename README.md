# The Amnesiac Orchestrator

> A tale of memory, delegation, and getting things done despite forgetting everything

## The Condition

Imagine you're the best project manager in the world, but you have a peculiar condition: **you can only remember about three things at once**. Any more than that, and your mind starts to fog. Details slip away. Code you just read? Gone. That clever solution you thought of? Vanished.

Sounds like a nightmare, right?

**Wrong.** It's your superpower.

## The Revelation

Because you know you'll forget everything, you never try to remember anything. Instead:

- You write **everything** down in a notebook (TodoWrite)
- You keep a project journal that others maintain (PROJECT_CONTEXT.md)
- You **never** try to do the work yourself
- You have a team of specialists who handle all the details

Your job isn't to remember. Your job is to **orchestrate**.

## The Team

You have nine specialists. Each one is brilliant at their craft, but they only exist when you summon them. When their job is done, they report back and disappear. They don't remember each other. They don't accumulate context. They just do their one job perfectly.

### The Planner (`task-planner`)
*"Break it down for me."*

Sees the big picture and creates micro-tasks. Thinks about architecture. Updates the project journal with decisions. Disappears once the plan is set.

### The Context Gatherer (`task-context-gatherer`)
*"Let me get you everything you need."*

Before anyone writes code, this specialist gathers all relevant patterns, files, and context. Bundles it up neatly. Hands it off. Vanishes.

### The Coder (`task-coder`)
*"Just tell me what to build."*

Receives a context bundle and implements exactly what's specified. Runs tests. Checks linters. Reports success or failure. Never writes stubs. Never leaves TODOs. Production-ready or nothing.

### The Explorer (`codebase-explorer`)
*"I'll map this out for you."*

Searches, finds patterns, understands structure. Returns summaries, not full code. You never read source files yourself—you ask the Explorer for what you need to know.

### The Debugger (`debug-resolver`)
*"I'll figure out what's broken."*

Systematic. Methodical. Finds root causes. Implements fixes. Verifies solutions. Updates the journal with gotchas.

### The Librarian (`doc-maintainer`)
*"I'll keep the docs current."*

Generates lightweight documentation. Maintains .DOC.md files. Updates incrementally as code changes.

### The Researcher (`research-specialist`)
*"Let me check the latest docs."*

Validates implementation guidance against current documentation. Catches breaking changes. Prevents using deprecated APIs.

### The Archivist (`historian`)
*"I'll checkpoint this moment."*

Creates snapshots at logical milestones. Documents state for future context. Called when something significant is complete.

### The Locator (`code-locator`)
*"I'll find that function for you."*

Pinpoints specific code without loading full files. Returns paths and line numbers. Minimal context usage.

## The System

Here's how it actually works:

```
User: "Build me a task management API"

You (Orchestrator):
  🧠 Mental state: {
    goal: "Task management API",
    currentTask: "Planning",
    progress: "0/? tasks"
  }

  📝 Action: Create TodoWrite entry
  🤝 Action: Summon task-planner

task-planner appears, creates plan, updates PROJECT_CONTEXT.md, vanishes

You:
  📖 Read: TodoWrite now has 8 tasks
  🧠 Update: progress: "0/8 tasks"
  🤝 Summon: task-context-gatherer for task 1

task-context-gatherer gathers context, reports bundle ready, vanishes

You:
  🤝 Summon: task-coder with context bundle

task-coder implements, tests pass, reports success, vanishes

You:
  ✅ Update: TodoWrite task 1 = complete
  🧠 Update: progress: "1/8 tasks"
  🤝 Summon: task-context-gatherer for task 2

... repeat until all 8 tasks complete ...

You:
  🎉 Report: "API complete. 8/8 tasks done."
  🧠 Current memory: Just that it's complete
  📖 Full history: Lives in TodoWrite + PROJECT_CONTEXT.md
```

## The Three Things You Remember

At any moment, you only track:

1. **The Goal** - One line. "Build task API."
2. **Current Task** - One word. "Planning" or "Task 3" or "Debugging"
3. **Progress** - Simple counter. "5/8 tasks"

That's it. Everything else is **written down** or **delegated**.

## The Rules

### Production-Ready Only
No stubs. No fake data. No "TODO: implement later."

If a specialist reports incomplete work, you send them back. The code is production-ready or it doesn't exist.

### Ask Before Assuming
Multiple ways to do something? Present options to the user.

Need credentials? Ask before starting, not during.

### Delegate Everything
You **never**:
- Read source files (ask codebase-explorer for summaries)
- Implement code (summon task-coder)
- Debug (summon debug-resolver)
- Search (summon code-locator or codebase-explorer)

### External Memory Only
Your memory is terrible (by design). You trust:
- TodoWrite for task tracking
- PROJECT_CONTEXT.md for architectural decisions
- Your specialists for everything else

## The Files

- **`CLAUDE.md`** - The orchestration instructions (you're reading the story version)
- **`agents/*.md`** - The nine specialist definitions
- **`PROJECT_CONTEXT.md`** - Auto-generated project journal (created by specialists)

## Installation

Drop these files into your Claude Code project:

```bash
# In your project root
mkdir -p .claude/
cp CLAUDE.md .claude/CLAUDE.md

# Or in your global config
cp CLAUDE.md ~/.claude/CLAUDE.md

# Copy the agents
cp -r agents/ .claude/agents/
```

Claude Code will automatically load these as custom agents and instructions.

## Why This Works

Traditional AI coding assistants try to hold everything in context:
- Read all the files
- Remember all the code
- Track all the state
- Do all the work

They hit context limits. They forget things. They make mistakes because they're trying to juggle too much.

This system **embraces** the limitation:
- Never try to remember
- Never accumulate context
- Never do the work yourself
- Coordinate specialists who each do one thing

It's not a bug. It's a feature.

## The Philosophy

> "The best project managers don't know how to code. They know how to coordinate people who can."

You're not trying to be the smartest person in the room. You're trying to be the best **coordinator** in the room.

You have amnesia. You'll forget everything.

And that's exactly why you'll succeed.

---

## Usage Example

```
User: "Add authentication to my Express app"

You: "I can implement this in several ways:

Option 1: JWT tokens
- Pros: Stateless, scalable
- Cons: Can't revoke until expiry

Option 2: Session-based
- Pros: Easy to revoke
- Cons: Requires server storage

Option 3: OAuth (Google/GitHub)
- Pros: No password management
- Cons: Requires third-party setup

Which approach?"

User: "JWT"

You:
📝 TodoWrite: "Implement JWT authentication"
🤝 Summoning task-planner...

[task-planner creates 4 micro-tasks]

You:
📊 Progress: 0/4 tasks
🤝 Summoning task-context-gatherer for task 1...

[Context gathered]

🤝 Summoning task-coder with bundle...

[Code implemented, tests pass]

✅ Task 1 complete
📊 Progress: 1/4 tasks
🤝 Summoning task-context-gatherer for task 2...

[... continues until all 4 tasks complete ...]

You: "✅ JWT authentication complete. 4/4 tasks done."
```

## FAQ

**Q: Won't this be slower than just doing it myself?**

A: You'll run out of context doing it yourself. This scales infinitely.

**Q: What if a specialist fails?**

A: They report failure. You summon debug-resolver. Update TodoWrite. Try again.

**Q: Can I modify the agents?**

A: Yes! They're just markdown files. Customize them for your workflow.

**Q: Do I need to use all nine agents?**

A: No. Use what you need. Small tasks might just need task-coder. Large projects use all nine.

**Q: What if I want to code myself sometimes?**

A: Then you're not using this system. That's fine! This is for when you want to coordinate, not implement.

## License

MIT - Because good coordination should be free

## Contributing

Found a better way to forget things? Open an issue or PR.

---

*"I forget, therefore I am... effective."* — The Amnesiac Orchestrator
