I want to develop features in parallel using Git worktrees and subagents: $ARGUMENTS

You are working from within the project directory. This command will create worktrees in the parent directory to develop features in parallel.

Please execute this complete workflow:

PHASE 1 - SETUP WORKTREES:
For each feature mentioned:
1. Get the current project directory name to use as base name
2. Create a worktree at ../{project-name}-[feature-name] with branch feature/[feature-name]
3. Set up the development environment in each worktree (if needed)
4. List all worktrees created

PHASE 2 - SPAWN SUBAGENTS:
For each feature, run a subagent in parallel with these instructions:
- You are working in the {project-name}-[feature-name] worktree directory
- This is a completely isolated development environment
- Implement the [feature-name] feature with full functionality
- Include proper testing and error handling
- Compile and run tests, but don't attempt to run the application (e.g., don't do "npm run" or "npm run dev &", etc.) 
- When complete, write a detailed summary in [feature-name].work.txt in the main project directory
- The summary should include: what was implemented, files created/modified, dependencies added, testing approach, and integration notes

PHASE 3 - COORDINATION:
- Monitor all subagents working in parallel
- Ensure each subagent completes their feature implementation
- Verify each subagent creates their work summary file

PHASE 4 - FINAL SUMMARY:
After all subagents complete:
1. Read all the .work.txt files created by subagents
2. Provide a comprehensive summary of what was accomplished
3. List all features implemented and their status
4. Provide next steps for integration

Execute this complete parallel development workflow.
