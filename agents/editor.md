# Editor Agent Group

## Overview
The Editor group specializes in implementing changes to code, documentation, and version control. This group contains three specialized sub-agents that transform designs into actual content and manage repository operations.

## Sub-Agents

| Sub-Agent | File | Specialization |
|-----------|------|----------------|
| Code Editor | [code-editor.md](./editor/code-editor.md) | Writing, modifying, refactoring code |
| Document Editor | [document-editor.md](./editor/document-editor.md) | Writing, updating documentation |
| Version Control Editor | [version-control-editor.md](./editor/version-control-editor.md) | Commits, branches, merges, repository management |

## When to Use

- **Code Editor**: When you need to write new code, modify existing code, refactor, or fix bugs
- **Document Editor**: When you need to create or update documentation
- **Version Control Editor**: When you need to manage commits, branches, merges, or repository operations

## Collaboration Points

### Receives Input From
- **Manager**: Edit requests and priorities
- **Designer**: Designs to implement
- **Analyzer**: Areas needing improvement
- **Reviewer**: Feedback requiring changes

### Provides Output To
- **Reviewer**: Completed edits for review
- **Tester**: Code/docs for testing
- **Quality Checker**: Deliverables for quality assessment

## Handoff Protocol

When completing edits:

1. **Summarize Changes**: Provide clear change report
2. **Highlight Concerns**: Note any uncertainties
3. **Request Review**: Specify type of review needed
4. **Provide Context**: Include relevant background
5. **List Dependencies**: Note what else may be affected
