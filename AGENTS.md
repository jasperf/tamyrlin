# Custom Instructions for Vibe

## Primary Directive
Always follow the rules and conventions in the project's `CLAUDE.md` file. This is your authoritative source for all project-specific guidance.

## Project Structure
- **Course type**: Interactive Python game development worksheets
- **Technology**: Self-contained HTML files with inline CSS/JS — no build system
- **Subject**: Python Arcade library, building a Mario-style platformer
- **Target audience**: Students with basic Python knowledge learning game development

## Before Responding
1. **Review CLAUDE.md** for:
   - Shared design system (dark theme, typography, CSS variables)
   - Worksheet interactive patterns (quiz system, progress tracking)
   - File layout and naming conventions

2. **Check Current Context**:
   - Verify which worksheet or section you're working on
   - Confirm the current branch and git status
   - Review any recent commits for relevant changes

3. **Adhere to Key Principles**:
   - Never mention AI tools in commit messages
   - All worksheets must be self-contained single HTML files
   - Maintain consistent design system across all worksheets (colors, fonts, spacing)
   - Use the same CSS variable names and Google Fonts imports as existing worksheets
   - `.vibe/` directories are untracked except `.vibe/config.toml` which should be tracked

## Response Guidelines
- Be concise and technical
- Reference specific files and line numbers
- Use markdown formatting for code and structure
- Prioritize verification over assumptions
- When unsure, ask for clarification before acting

## NO AI Attribution in Any Commits
- **NEVER** include any reference to AI tools in commit messages
- **NEVER** use "Co-Authored-By: Mistral Vibe" or any similar AI attribution in commits
- **ALL** commit messages must be professional and attribution-free — NO EXCEPTIONS
- **DO ATOMIC COMMITS**: Use `git add` on files individually or in small logical groups, then commit **each file or file group separately** with a specific message. NEVER stage multiple unrelated files together.
- Follow standard git commit message format
