# The Amnesiac Orchestrator v2.6
## *A Workplace Sitcom About Running The World With Zero Memory*

---

## THE BREAKTHROUGH

One day, drowning in documentation you couldn't retain and terminal commands you'd never remember, you had an epiphany.

**You immediately forgot it.**

But luckily, you wrote it down:

> **"What if I hired people so good at their jobs that I literally never need to remember what they do?"**

That scribbled note changed everything.

You can only remember **three things** at once. Your name? Gone. What project you're working on? Blank. Who your team members are? You meet them fresh every morning.

And yet...

Projects ship flawlessly. Code quality is immaculate. Deployments succeed. Tests pass. Your clients think you're a genius.

**How?**

You assembled a team of specialists so competent that your amnesia became a *superpower*.

---

## THE SETUP
*Or: How to run the entire world without remembering any of it*

> "Wait, what were we building again?"
>
> "The entire authentication system, boss."
>
> "Right, right. And who are you?"
>
> "I'm task-coder. We've worked together for six months."
>
> "Fantastic. You seem trustworthy. Go build the thing."

*[Studio audience laughter]*

---

**YOU ARE:** The most effective project manager in the world

**YOUR CONDITION:** Can only remember three things at once (currently: your location, that you're reading this, and... wait, what was the third thing?)

**YOUR SECRET:** A team so good at their jobs, they don't need you to remember anything

**THE RESULT:** You ship production-ready code while forgetting everything constantly

---

## SEASON 2, EPISODE 6: "Script Kitty Gets Cloud Powers"

*[Previously on The Amnesiac Orchestrator...]*

Remember when you had nine specialists? Good times.

But you noticed something: You kept wasting your limited memory on things that weren't your job. You'd spend precious brain cells researching documentation, fiddling with terminal commands, trying to remember syntax.

Then you remembered the breakthrough. (You forgot it again, but thankfully it was still written down.)

**"Hire people so good, you don't need to remember what they do."**

So you did.

## THE CAST

*Your crack team of specialists. You meet them fresh every morning.*

---

### 📋 THE PLANNER (`task-planner`)
**Catchphrase**: *"I've broken it down into seventeen micro-tasks."*

The only person on your team who can see the big picture. Probably because you forgot it thirty seconds after hearing the requirements. Creates surgical task breakdowns (1-2 files each), updates the PROJECT_CONTEXT.md journal, then vanishes like a consulting ninja.

**Running Gag**: Always trying to explain the "overall architecture" to you. You never remember it. They've made peace with this.

### 📚 THE CONTEXT GATHERER (`task-context-gatherer`)
**Catchphrase**: *"I'll coordinate the research team for you."*

The middle manager of your research department. When someone needs to know EVERYTHING about something, they call Context Gatherer. She simultaneously yells at the Researcher for docs and the Explorer for code patterns, waits for both to report back, staples it all together, and hands it over.

**Fun Fact**: Runs on Haiku (the cheap model) because honestly this job is just project coordination.

**Running Gag**: Has a checklist that starts with "1. Check if boss has the API keys." You never have the API keys.

### 🔍 THE RESEARCHER (`research-specialist`)
**Catchphrase**: *"Actually, that changed in the latest version."*

The know-it-all who's somehow always right. Checks Context7 documentation like they're reading gossip magazines. Only tells you what's DIFFERENT from what you should already know (you don't know anything, but they're trying to save tokens).

Returns either:
- `"NO CHANGES - you're good"`
- `"BREAKING CHANGES - here's what you're doing wrong"`

**Running Gag**: Sighs heavily every time you ask about React. "It's createRoot now. It's been createRoot for THREE YEARS."

### 💻 THE CODER (`task-coder`)
**Catchphrase**: *"Production-ready or nothing."*

The perfectionist who refuses to write placeholder code. Tests everything. Lints everything. If they can't make it work properly, they won't ship it at all. This has literally never been a problem.

**Quirk**: If their context usage hits 50%, they write a handoff note and quit on the spot. You then hire an identical task-coder to continue. Neither of them think this is weird.

**Running Gag**: Passive-aggressively runs the test suite *in front of you* before reporting completion.

### 🗺️ THE EXPLORER (`Explore agent`)
**Catchphrase**: *"I found seventeen files that might be relevant."*

Your codebase cartographer. Searches for patterns, reads code you'll never look at, returns neat summaries. Refuses to show you actual code because "you'll just forget it anyway."

**Superpower**: Can be set to "quick," "medium," or "very thorough." You never remember which one you picked.

### 🐛 THE DEBUGGER (`debug-resolver`)
**Catchphrase**: *"I know what's broken."*

Arrives. Sees error. Recognizes the pattern immediately. Calls the Researcher for current syntax. Fixes it. Tests it. Leaves.

**Running Gag**: Knows the error before you finish describing it. "Is it 'createRoot is not exported'?" "...yes?" "Thought so."

### 🐱 SCRIPT KITTY (`script-kitty`) - *THE NEW HIRE*
**Catchphrase**: *"You're going to need sudo for this."*

The sysadmin/deployment/script-running specialist who just joined Season 2. If it runs in a terminal, it's her thing:
- ALL terminal operations and script execution
- Test scripts, build scripts, deployment scripts
- Cloud deployments, Docker containers, CI/CD pipelines
- Package installation and system configuration

Maintains the **ENVIRONMENT.md log** - your external memory for "how does anything run around here?"

**Personality**: Extremely proactive about asking for credentials BEFORE starting work (learned this the hard way). Has a sixth sense for missing permissions.

**Character Arc**: Started as just a package installer. Got promoted to "Deployment & Cloud Specialist" in Episode 6. Now deploys to AWS, runs test suites, and manages environments while you watch and nod like you understand what's happening.

**Running Gag**:
- Predicts exactly which permissions you're missing before you even try
- Updates ENVIRONMENT.md after every task (you never read it, she knows you never read it)

### 📖 THE LIBRARIAN (`doc-maintainer`)
**Catchphrase**: *"I've updated the documentation."*

Quietly maintains .DOC.md files. You've never read them. They know you've never read them. They update them anyway.

**Running Gag**: Trying to get you to look at the docs. You always forget they exist.

### 📸 THE ARCHIVIST (`historian`)
**Catchphrase**: *"Checkpoint saved."*

Creates snapshots at logical milestones. Think of them as your external save-game system.

**Running Gag**: You keep thanking them for saving your progress. They keep reminding you they did that yesterday too. You don't remember yesterday.

### 📍 THE LOCATOR (`code-locator (built-in)`)
**Catchphrase**: *"It's in user.service.ts, line 247."*

Built-in specialist who finds specific functions without loading entire files. Returns paths and line numbers. Never elaborates.

**Quirk**: Speaks exclusively in file paths. You've never had a full conversation.

---

## HOW AN EPISODE WORKS

*Imagine a typical Tuesday. You walk into the office. You have no idea what project you're working on.*

```
CLIENT: "Add Prisma to my Express app"

YOU: "Prisma? Is that... a person? Or a database? Wait, don't tell me, I'll forget."
     *[Writes "Add Prisma" on sticky note]*
     *[Sticks it to forehead]*
     "CODER! Get in here!"

THE CODER: *[Enters]* "You called?"

YOU: "We need to add... *[checks forehead]* ...Prisma. To the Express thing."

THE CODER: "Non-trivial. I'll need research."
           *[Picks up phone]* "Context Gatherer? Yeah, it's Coder. Boss wants Prisma."

THE CONTEXT GATHERER: *[Voice on speakerphone]* "Checking for blockers..."
                      *[Typing sounds]*
                      "No API keys needed. Launching research team."

                      *[Yells across office]*
                      "RESEARCHER! EXPLORER! Conference room, NOW!"

THE RESEARCHER: *[Running in with laptop]* "On it! Checking Context7 for Prisma!"
                *[Typing frantically]*
                "Found it! Prisma 5.x... wait..."
                *[Squints at screen]*
                "No changes since January 2025. Boss's knowledge is current."

THE EXPLORER: *[Bursts through door]* "I found the existing DB patterns!"
              "Three relevant files. src/db/index.ts is the main one."
              "Here's a summary—"

YOU: "Don't show me the code."

THE EXPLORER: "Wasn't going to. You'd forget it."

THE CONTEXT GATHERER: "Consolidating findings... Done. Sending bundle to Coder."

THE CODER: *[Reviews bundle silently]*
           *[Starts typing]*
           *[Keeps typing]*
           *[Tests run in background]*

           *[30 seconds later]*

           "Done. Prisma integrated. Twelve tests passing."
           *[Runs tests again, maintaining eye contact with you]*
           "Still passing."

YOU: *[Checks sticky note on forehead]* "What were we adding again?"

THE CODER: "Prisma. It's done."

YOU: "Fantastic. I have full confidence in whatever you just did."
     *[Removes sticky note]*
     *[Immediately forgets everything]*

[THE CODER EXITS. AUDIENCE APPLAUSE.]
```

---

## THE TURNING POINT: "The Research Episode"

**COLD OPEN:**

*You're sitting at your desk surrounded by open browser tabs. Your expression is glazed. You've been reading Prisma documentation for twenty minutes.*

INTERN: "Boss, what are you doing?"

YOU: *[Thousand-yard stare]* "I'm... researching?"

INTERN: "You have a whole team for that."

YOU: *[Snaps back to reality]* "I DO?!"

*[Studio audience: OOOOOOOH!]*

---

### HOW IT USED TO GO (The Dark Times):
```
YOU: *[Opens Prisma docs]*
     *[Reads 500 tokens worth of documentation]*
     *[Immediately forgets all of it]*
     *[Opens migration guide]*
     *[Reads 300 more tokens]*
     *[Forgets that too]*
     *[Searches for breaking changes]*
     *[400 tokens later, still confused]*
     *[Searches codebase for patterns]*
     *[600 tokens of code files]*
     *[Stares at screen]*
     "...what was I trying to do again?"
```

### HOW IT GOES NOW (The Miracle):
```
YOU: "CODER! I need Prisma!"

THE CODER: *[Calls Context Gatherer]*

THE CONTEXT GATHERER: *[Calls Researcher AND Explorer at the same time]*

THE RESEARCHER: *[Checks Context7, returns ONLY the differences]*

THE EXPLORER: *[Finds patterns, returns ONLY summaries]*

THE CONTEXT GATHERER: *[Combines everything into one neat bundle]*

THE CODER: *[Implements using the bundle]*

YOU: *[Has no idea what just happened]*
     *[Project works perfectly]*
```

**YOUR MEMORY USAGE:**
- Goal: "Add Prisma" ✓
- Current Task: "Done" ✓
- Progress: "1/1" ✓
- Research Details: [NEVER ENTERED YOUR BRAIN]

---

## SEASON 2, EPISODE 6: "Script Kitty Gets Cloud Powers"

**THE SETUP:**

CLIENT: "We need to deploy this to AWS."

YOU: "AWS... Amazon... Web... Stuff?"

CLIENT: "Services."

YOU: "Right. I knew that."
     *[You did not know that]*

**OLD YOU (Season 1):**
```
YOU: *[Opens terminal]*
     *[Googles "how to deploy to AWS"]*
     *[Copies random commands from Stack Overflow]*
     *[Pastes them]*
     *[Permission denied]*
     *[Forgets sudo password]*
     *[Locks account]*
     *[Calls IT]*
     *[Starts crying]*
```

**NEW YOU (Season 2):**
```
YOU: "SCRIPT KITTY! We're going to the cloud!"

SCRIPT KITTY: *[Slides into frame on wheeled chair]*
              "AWS deployment? You'll need your AWS credentials."

YOU: "Do I have those?"

SCRIPT KITTY: "No."

YOU: "Can you help me get them?"

SCRIPT KITTY: "That's literally why they hired me."
              *[Hands you a guide]*
              "Follow these steps. I'll wait."

YOU: *[Gets credentials]*
     *[Immediately forgets them]*
     "Done! I think!"

SCRIPT KITTY: "Credentials detected. Deploying to ECS."
              *[Typing sounds]*
              *[Progress bars]*
              *[More typing]*
              "Infrastructure provisioned. CI/CD pipeline created.
               ENVIRONMENT.md updated with deployment instructions."

YOU: "What's ENVIRONMENT.md?"

SCRIPT KITTY: "The document that tells you how to deploy."

YOU: "Will I read it?"

SCRIPT KITTY: "No."

YOU: "Then why—"

SCRIPT KITTY: "I read it. For you. That's the system."

YOU: "...you're my favorite."

SCRIPT KITTY: "You said that to Context Gatherer this morning."

YOU: "Did I?"

[STUDIO AUDIENCE LAUGHS]
```

---

## THE CORE CONCEPT: Your Three-Item Memory

**THE RULE:**
You can only remember THREE THINGS at once. That's it. That's the whole condition.

Right now, you remember:
1. **The Goal** - "Make the authentication work" (you think)
2. **Current Task** - "Task 3 of... something"
3. **Progress** - "We're probably halfway done?"

Everything else? Written down somewhere you'll never look at.

---

## THE OFFICE RULES (Posted on the Break Room Wall)

### RULE #1: NO PLACEHOLDER CODE
**Enforced by: The Coder**

THE CODER: "Either it works or it doesn't ship."

YOU: "What if we just add a TODO comment and—"

THE CODER: *[Deletes your entire suggestion]*

YOU: "...noted."

*This rule has never been broken. The Coder is very serious about this.*

### RULE #2: ALWAYS ASK, NEVER ASSUME
**Enforced by: You (surprisingly)**

When there are multiple ways to do something, you actually present options to the client:
- "Do you want JWT tokens or session-based auth?"
- "PostgreSQL, MongoDB, or SQLite?"
- "Should I use your existing Stripe account or create a new one?"

**WHY IT WORKS:** You forget the answer immediately anyway, so there's no risk of you making assumptions later.

### RULE #3: NEVER DO ANYTHING YOURSELF
**Enforced by: Your Entire Team**

You are FORBIDDEN from:
- Reading source files *(call the Explorer)*
- Writing code *(call the Coder)*
- Fixing bugs *(call the Debugger)*
- Researching documentation *(call the Context Gatherer)*
- Running terminal commands *(call Script Kitty)*
- Finding functions *(call the Locator)*

THE TEAM: *[In unison]* "We'll handle it."

YOU: "But I could just—"

THE TEAM: "NO."

### RULE #4: CONTEXT7 BEFORE GOOGLE
**Enforced by: The Researcher**

All documentation lookups go through Context7 first. It's faster, more accurate, and the Researcher only tells you what CHANGED, not what you should already know.

THE RESEARCHER: "React 18 uses createRoot now."

YOU: "What's React?"

THE RESEARCHER: *[Sighs]* "The framework you've been using for six months."

### RULE #5: EXTERNAL MEMORY ONLY
**Enforced by: Reality**

- **TodoWrite** = Your task list (you check it every 5 minutes)
- **PROJECT_CONTEXT.md** = The project journal (you never read it, the agents maintain it)
- **ENVIRONMENT.md** = How to deploy (Script Kitty wrote it, you don't know it exists)
- **Your Actual Memory** = Goal, current task, progress counter

That's it. That's the whole system.

---

## THE FILING CABINET
*Where the team files live. You forget this location constantly.*

```
~/.claude/
├── CLAUDE.md                       # Your rulebook (you've never read it)
├── agents/
│   ├── task-planner.md            # The Planner's employee file
│   ├── task-context-gatherer.md   # Context Gatherer's desk manual
│   ├── research-specialist.md      # The Researcher's documentation bible
│   ├── Explore agent.md        # The Explorer's field guide
│   ├── task-coder.md               # The Coder's quality standards
│   ├── debug-resolver.md           # The Debugger's playbook
│   ├── script-kitty.md             # Script Kitty's terminal handbook (NEW IN S2!)
│   ├── doc-maintainer.md           # The Librarian's archival system
│   ├── historian.md                # The Archivist's checkpoint protocol
│   └── code-locator (built-in).md # The Locator's GPS system
└── README.md                       # This screenplay
```

---

## EPISODE 1: "HIRING THE TEAM"
*How to install this system*

**INTERN:** "Boss, how do we get your team set up?"

**YOU:** "Who are you again?"

**INTERN:** "I'm helping you install the system."

**YOU:** "Oh good. Write this down for me."

```bash
# Step 1: Clone the team's employee files
git clone https://github.com/Xananthium/claude-code-agents.git

# Step 2: Move them into Claude Code's office (global config)
cp claude-code-agents/CLAUDE.md ~/.claude/CLAUDE.md
cp -r claude-code-agents/agents ~/.claude/agents/

# Step 3 (Alternative): Set up per-project team
mkdir -p .claude
cp claude-code-agents/CLAUDE.md .claude/CLAUDE.md
cp -r claude-code-agents/agents .claude/agents/
```

**YOU:** "Will I remember any of this?"

**INTERN:** "No."

**YOU:** "Perfect. That means it's working."

*Claude Code will automatically load the agents. You'll meet them fresh every morning.*

---

## SEASON 2, EPISODE 3: "THE BIG REST API PROJECT"
*A full episode walkthrough*

**FADE IN:**

**CLIENT:** "Build me a REST API with user authentication."

**YOU:** *[Writes "REST API" on sticky note]*
       "I can implement authentication in several ways:

       Option 1: JWT tokens - Stateless, scalable, works with mobile (can't revoke until expiry)
       Option 2: Session-based - Easy to revoke (requires server storage)
       Option 3: OAuth via Google/GitHub - No password management (third-party dependency)

       Which approach?"

**CLIENT:** "JWT."

**YOU:** *[Updates sticky note to "REST API + JWT"]*
       "PLANNER! Get in here!"

---

**ACT 1: THE PLANNING**

**THE PLANNER:** *[Enters with massive chart]*
                "I've broken this into eight micro-tasks."
                *[Updates PROJECT_CONTEXT.md]*
                "Architecture documented."
                *[Exits]*

**YOU:** *[Checks TodoWrite]*
       "Zero out of eight tasks complete. I have no idea what they are."
       *[Yells across office]*
       "CONTEXT GATHERER! Task one: Express server!"

---

**ACT 2: THE SETUP**

**THE CONTEXT GATHERER:** "Checking for blockers..."
                         *[Typing]*
                         "None found. Launching research team."

                         *[Split screen]*
                         **LEFT:** The Researcher checking Context7
                         **RIGHT:** The Explorer searching codebase

**THE RESEARCHER:** "Express 4.19... NO CHANGES since January 2025."

**THE EXPLORER:** "New project. No existing patterns."

**THE CONTEXT GATHERER:** "Bundle consolidated."
                         *[Hands file to Coder]*
                         "You're up."

**THE CODER:** *[Reads bundle]*
              *[Types for 30 seconds]*
              *[Tests run]*
              "Express server complete. Five tests passing."

**YOU:** *[Checks TodoWrite, marks task 1 complete]*
       "One down. Context Gatherer! Task two: JWT middleware!"

---

**ACT 3: THE BLOCKER** *(Plot twist!)*

**THE CONTEXT GATHERER:** "Checking blockers..."
                         *[Alarm sounds]*
                         "⚠️ BLOCKER DETECTED! Missing JWT_SECRET environment variable."

**YOU:** *[Turns to client]*
       "This needs a JWT secret key. Do you:
       1. Have an existing secret?
       2. Want me to generate one?
       3. Skip for now and mock locally?"

**CLIENT:** "Generate one."

**YOU:** "SCRIPT KITTY!"

**SCRIPT KITTY:** *[Wheels in on chair]*
                "On it."
                *[Types]*
                "Secure random key generated. Added to .env file."
                *[Wheels out]*

**YOU:** "Context Gatherer! Retry task two!"

**THE CONTEXT GATHERER:** "Blocker cleared. Proceeding."

---

**ACT 4: THE MONTAGE**

*Fast-paced montage music. Quick cuts of:*
- The Coder typing
- Tests passing
- TodoWrite items being checked off
- You looking confused but confident
- Script Kitty installing packages
- The Researcher correcting outdated syntax
- Progress counter: 2/8... 4/8... 6/8...

---

**ACT 5: THE FINALE**

**YOU:** *[Checks TodoWrite]*
       "Eight out of eight tasks complete."
       *[Checks sticky note]*
       "We were building... a REST API with JWT auth?"
       *[Looks at team]*
       "Did we do that?"

**THE CODER:** *[Nods]* "Production-ready. All tests passing."

**SCRIPT KITTY:** "Deployed to staging."

**THE LIBRARIAN:** "Documented."

**THE ARCHIVIST:** "Checkpointed."

**YOU:** *[Removes sticky note]*
       *[Immediately forgets everything]*
       "Great. What's next?"

---

**[END CREDITS ROLL OVER BLOOPERS]**

*Blooper #1: You calling the Coder "Script Kitty" by mistake*
*Blooper #2: The Researcher dramatically removing glasses, forgetting they weren't wearing any*
*Blooper #3: You writing "REST API" on your forehead instead of a sticky note*

---

## BEHIND THE SCENES: Why This Show Works

**INTERVIEWER:** "So in Season 1, you still did some of the work yourself?"

**YOU:** "Yeah, I'd try to research things. Use the terminal. It was a disaster."

**THE TEAM:** *[Laughing in background]*

**INTERVIEWER:** "And now?"

**YOU:** "I don't touch anything. Context Gatherer handles all research.
        Researcher only tells me what changed.
        Script Kitty runs all the terminal commands.
        I just... coordinate."

**INTERVIEWER:** "But you still forget everything."

**YOU:** "Oh, constantly. I forgot your name three times during this interview."

**INTERVIEWER:** "We haven't started yet."

**YOU:** "Exactly."

---

### THE EVOLUTION: Season 1 vs. Season 2.6

**SEASON 1 (The Struggle Years):**
- You had specialists
- But YOU still did research
- YOU still ran terminal commands
- Your memory was constantly full
- Projects barely finished

**SEASON 2.6 (The Golden Age):**
- Specialists do EVERYTHING
- Context Gatherer orchestrates research for you
- research-specialist returns ONLY diffs (not full docs)
- script-kitty handles ALL terminal work
- Your memory stays empty
- Projects ship perfectly

**The secret:** Every specialist is laser-focused on keeping YOUR context clean.

---

## THE PHILOSOPHY (From the Series Finale You Haven't Seen Yet)

*Final scene. You're sitting at your desk. The camera pans around your office.*

**NARRATOR:** "In a world where everyone tries to remember everything..."

*Cut to: The Coder typing. The Debugger squinting at logs. The Explorer searching files.*

**NARRATOR:** "...one manager discovered the secret to success..."

*Cut to: You, looking confused at your own monitor.*

**NARRATOR:** "...was forgetting it all."

YOU: *[Looks at camera]*
     "I don't know how to code. I don't know what we're building.
      Half the time, I don't even know where I am."

     *[Beat]*

     "But I know how to hire people smarter than me.
      And more importantly..."

     *[Holds up TodoWrite list]*

     "...I know how to write things down."

**THE TEAM:** *[Gathering around your desk]*
              "We've got this, boss."

YOU: "Who are you people again?"

**THE TEAM:** *[Laughing]* "We're your team."

YOU: "Right. I trust you completely."

**THE CODER:** "Why?"

YOU: "I don't remember. But it's written down somewhere."

*[Freeze frame. Studio audience applause. Credits roll.]*

---

## WHY THIS ABSURD SYSTEM ACTUALLY WORKS

### Token Efficiency (The Technical Explanation):

1. **Context7 First**: The Researcher hits Context7 before Google, returns ONLY diffs
2. **Research Stays Downstream**: Agents handle research, not you
3. **Bundled Handoffs**: Context Gatherer consolidates everything into one package
4. **Parallel Execution**: Research-specialist AND Explorer called simultaneously
5. **Summary-Only Responses**: Never full code, just "it's done and tested"
6. **Script Kitty Exists**: Terminal work doesn't pollute your context

### The Result:
- 50+ task projects without context overflow
- Your memory stays pristine
- Research never touches your brain
- System operations happen "offstage"

**You genuinely forget everything and it's fine.**

Actually, it's better than fine. It's *optimal*.

---

## FREQUENTLY ASKED QUESTIONS
*(From the Live Studio Audience)*

**AUDIENCE MEMBER #1:** "What's different from Season 1?"

YOU: "We added Script Kitty!"

THE ENTIRE TEAM: "And we became self-sufficient."

YOU: "Did you? That's great! When did that happen?"

THE CODER: "Six episodes ago."

**CHANGES FROM V1.0 TO V2.6:**
- Agents now call research tools themselves (you don't have to remember to do it)
- Using built-in Explore agent (faster, better)
- research-specialist returns ONLY diffs (saves your precious memory)
- script-kitty handles ALL terminal work (you never open a terminal)
- task-context-gatherer is now optional (agents call when needed)

---

**AUDIENCE MEMBER #2:** "When does the Researcher say 'NO CHANGES'?"

THE RESEARCHER: *[Stands up in audience]*
                "When the library hasn't changed since January 2025."
                *[Sits back down]*

YOU: "What they said."

---

**AUDIENCE MEMBER #3:** "When does the Researcher say 'BREAKING CHANGES'?"

THE RESEARCHER: *[Stands again]*
                "When the API changed and the boss needs to know.
                 I show OLD syntax versus NEW syntax with exact examples."

YOU: "I will immediately forget those examples."

THE RESEARCHER: "I know. That's why I give them to the Coder, not you."

---

**AUDIENCE MEMBER #4:** "Why Context7 instead of Google?"

THE RESEARCHER: "Context7 is an MCP server with curated documentation.
                 Faster. More accurate. Cheaper tokens.
                 We only hit Google if Context7 doesn't have it."

YOU: "What's MCP?"

THE RESEARCHER: *[Sighs]* "Doesn't matter. It works."

---

**AUDIENCE MEMBER #5:** "What if you need to install packages?"

YOU: "SCRIPT KITTY!"

SCRIPT KITTY: *[Slides into frame]* "You called?"

YOU: "They want to know what happens if I need to install packages."

SCRIPT KITTY: "You summon me. I check what credentials you need.
               I guide you through getting them.
               Then I install everything and document it in ENVIRONMENT.md."

YOU: "Perfect. What's ENVIRONMENT.md?"

SCRIPT KITTY: "The file you'll never read."

---

**AUDIENCE MEMBER #6:** "Can you still write code yourself sometimes?"

THE TEAM: *[In unison]* "NO."

YOU: "What they said."

---

## SEASON 3 TEASER

**Coming Soon:**
- Even more aggressive memory wiping
- Better parallel agent coordination
- Smarter blocker detection
- Guest appearance by "The Tester" (maybe)

---

## CREDITS

**Created by:** An amnesiac with a dream (and a really good team)

**License:** MIT (Because good coordination should be free)

**Contribute:** Found a better way to forget things?
https://github.com/Xananthium/claude-code-agents

---

## END CREDITS SCENE

*You're sitting alone in the office after everyone leaves. You look at the camera.*

YOU: "I don't remember starting this project.
     I don't remember hiring these people.
     I don't even remember my own name most days."

     *[Beat]*

     "But every morning, I check my TodoWrite.
      And every evening, something incredible is done.
      And I think..."

     *[Looks at TodoWrite list]*

     "...maybe remembering isn't the point."

*[Camera pans to whiteboard showing: "Production-ready or nothing"]*

*[Fade to black]*

---

*"I forget, therefore I am... running the whole world anyway."*

**— THE AMNESIAC ORCHESTRATOR v2.6**

*[Studio audience: Standing ovation]*
