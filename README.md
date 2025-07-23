# vibes - Vibe coding framework for Claude Code

## Installation

### For New Projects

1. Run `vibes-deploy <repo root>` to install `vibes` in your repository.
2. Run `claude` from your repository root and get to vibing.

### For Existing Projects

1. **Deploy the framework:**
   ```bash
   /path/to/vibes/vibes-deploy /path/to/your/existing/project
   ```

2. **Initialize project documentation:**
   ```bash
   cd /path/to/your/existing/project
   claude
   /vibes:init-existing
   ```

3. **Start your first session:**
   ```bash
   /vibes:startsession <your goal>
   ```

The deployment adds:
- `vibes/` directory with project templates and documentation
- `.claude/commands/vibes/` with framework commands  
- `vibes/CLAUDE.md` with framework instructions for Claude

The `/vibes:init-existing` command guides you through populating your `vibes/project/CODEBASE.md` with information about your existing project structure and conventions.

