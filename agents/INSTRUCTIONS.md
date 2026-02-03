# GitHub Copilot Agent Instructions

## Quick Reference

Use these agent instructions by including them in your GitHub Copilot chat context. Each agent has specialized capabilities for different tasks.

## How to Use

1. Copy the contents of the relevant agent file(s) into your custom instructions
2. Reference agents in your prompts using `@agent-name` format
3. Follow the communication protocols defined in each agent

## Agent Invocation Examples

### Starting a New Project
```
@manager: I need to build a REST API for user management.
Please analyze the requirements and create a development plan.
```

### Analyzing Existing Code
```
@analyzer: Please analyze the authentication module in src/auth/
Focus on security patterns and potential vulnerabilities.
```

### Designing a New Feature
```
@designer: Design a caching layer for our API responses.
Requirements: Redis-based, TTL support, cache invalidation.
```

### Implementing Code
```
@editor: Implement the user registration endpoint based on the design.
Follow the existing code patterns in the project.
```

### Version Control Operations
```
@version-control-editor: Create a feature branch and commit the authentication changes.
Use conventional commit messages and squash WIP commits.
```

### Reviewing Work
```
@reviewer: Review the PR changes for the payment integration.
Focus on security and error handling.
```

### Planning Tests
```
@tester: Create a test plan for the new checkout flow.
Include unit, integration, and E2E test scenarios.
```

### Quality Check
```
@quality-checker: Assess the current sprint deliverables.
Provide quality gate status and recommendations.
```

## Workflow Templates

### Full Development Cycle
```
1. @planner: Create development plan
2. @analyzer: Analyze existing system
3. @designer: Create technical design
4. @reviewer: Review design
5. @editor: Implement changes
6. @reviewer: Review code
7. @tester: Execute tests
8. @quality-checker: Final quality assessment
```

### Quick Fix Cycle
```
1. @analyzer: Analyze the issue
2. @editor: Implement fix
3. @reviewer: Review fix
4. @tester: Verify fix
```

### Documentation Cycle
```
1. @planner: Plan documentation scope
2. @analyzer: Analyze content needs
3. @designer: Design document structure
4. @editor: Write documentation
5. @reviewer: Review documentation
```

## Inter-Agent Communication

Agents can reference each other's outputs:

```
@editor: Based on the design from @designer, implement the user service.
Use the analysis from @analyzer to ensure compatibility.
```

## Combining Agents

For complex tasks, combine multiple agents:

```
@manager: Coordinate @analyzer, @designer, and @editor to:
1. Analyze the current payment module
2. Design improvements for PCI compliance
3. Implement the changes incrementally
```

## File Locations

All agent instruction files are located in:
```
.github/copilot-agents/
├── README.md                 # Overview and documentation
├── INSTRUCTIONS.md           # This file - quick reference
├── manager.md                # Manager agent
├── planner.md                # Planner agent
├── quality-checker.md        # Quality Checker agent
│
├── analyzer.md               # Analyzer group overview
├── analyzer/
│   ├── code-analyzer.md      # Code Analyzer sub-agent
│   └── document-analyzer.md  # Document Analyzer sub-agent
│
├── designer.md               # Designer group overview
├── designer/
│   ├── system-designer.md    # System Designer sub-agent
│   ├── code-designer.md      # Code Designer sub-agent
│   └── document-designer.md  # Document Designer sub-agent
│
├── editor.md                 # Editor group overview
├── editor/
│   ├── code-editor.md            # Code Editor sub-agent
│   ├── document-editor.md        # Document Editor sub-agent
│   └── version-control-editor.md # Version Control Editor sub-agent
│
├── reviewer.md               # Reviewer group overview
├── reviewer/
│   ├── plan-reviewer.md      # Plan Reviewer sub-agent
│   ├── design-reviewer.md    # Design Reviewer sub-agent
│   ├── document-reviewer.md  # Document Reviewer sub-agent
│   └── code-reviewer.md      # Code Reviewer sub-agent
│
├── tester.md                 # Tester group overview
└── tester/
    ├── test-planner.md       # Test Planner sub-agent
    ├── test-designer.md      # Test Designer sub-agent
    ├── test-editor.md        # Test Editor sub-agent
    └── test-executor.md      # Test Executor sub-agent
```

## Best Practices

1. **Be Specific**: Provide clear context and requirements
2. **Use Templates**: Leverage the templates in each agent file
3. **Follow Workflows**: Use established workflow patterns
4. **Iterate**: Allow agents to refine outputs through iteration
5. **Quality First**: Always involve Quality Checker for important deliverables
6. **Document Decisions**: Keep records of agent recommendations

## Customization Tips

- Add project-specific context to agent prompts
- Extend templates with your team's standards
- Create project-specific workflow combinations
- Adjust quality thresholds for your needs
