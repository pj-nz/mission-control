Anyone can use this orchestration setup:

### Option 1: Fork the Repo
1. Fork `https://github.com/pj-nz/mission-control`
2. Customize `memory/user.md` with their own context
3. Add their own skills to `skills/`
4. In Claude chat: "mission control" → Claude pulls from their fork

### Option 2: Download and Upload
1. Download zip from `https://github.com/pj-nz/mission-control`
2. Extract, customize `memory/user.md`
3. Re-zip or tar: `tar -czvf shared-context.tar.gz shared-context/`
4. Upload to Claude chat → say "mission control"

### Required Claude Settings
For GitHub pull to work, add these to Claude network allowlist:
- `github.com`
- `codeload.github.com`
- `raw.githubusercontent.com`

### What to Customize
| File | Purpose | Personalize? |
|------|---------|--------------|
| `memory/user.md` | Who you are, preferences | **Yes** |
| `memory/entities.json` | Your tools, companies, keys | **Yes** |
| `skills/*` | Skill definitions | Add your own |
| `projects/*` | Active workstreams | **Yes** |
| `ORCHESTRATION.md` | Architecture reference | Optional |

### Minimal Setup
At minimum, edit `memory/user.md`:
```markdown
# User: [Your Name]

## Role
[Your job/context]

## Communication Style
[How you like responses]

## Current Focus
[What you're working on]
```

Then say "mission control" in any new Claude chat.
