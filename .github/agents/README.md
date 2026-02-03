# GitHub Copilot Agent System

## Overview

This is a comprehensive multi-agent system designed to assist with software development tasks. The system consists of a Manager agent that orchestrates specialized sub-agents, each with distinct responsibilities.

## Agent Architecture

```
                    ┌─────────────────┐
                    │    Manager      │
                    │  (Orchestrator) │
                    └────────┬────────┘
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
        ▼                    ▼                    ▼
┌───────────────┐  ┌─────────────────┐  ┌─────────────────┐
│   Planner     │  │ Quality Checker │  │    Analyzer     │
│               │  │   (Monitor)     │  │ ┌─────────────┐ │
│ - Task Plans  │  │                 │  │ │Code Analyzer│ │
│ - Strategy    │  │ - Quality Gates │  │ │Doc Analyzer │ │
└───────────────┘  │ - Metrics       │  │ └─────────────┘ │
                   └─────────────────┘  └─────────────────┘
        │                    │                    │
        ▼                    ▼                    ▼
┌───────────────┐  ┌─────────────────┐  ┌─────────────────┐
│   Designer    │  │    Editor       │  │    Reviewer     │
│ ┌───────────┐ │  │ ┌─────────────┐ │  │ ┌─────────────┐ │
│ │  System   │ │  │ │Code Editor  │ │  │ │Plan Reviewer│ │
│ │   Code    │ │  │ │Doc Editor   │ │  │ │Design Revwr │ │
│ │ Document  │ │  │ │VC Editor    │ │  │ │Doc Reviewer │ │
│ └───────────┘ │  │ └─────────────┘ │  │ │Code Reviewer│ │
└───────────────┘  └─────────────────┘  │ └─────────────┘ │
                                        └─────────────────┘
        │                                        │
        ▼                                        ▼
┌─────────────────────────────────────────────────────────┐
│                        Tester                           │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────────┐  │
│  │Test Planner │  │Test Designer│  │  Test Editor    │  │
│  └─────────────┘  └─────────────┘  └─────────────────┘  │
│                   ┌─────────────────┐                   │
│                   │ Test Executor   │                   │
│                   └─────────────────┘                   │
└─────────────────────────────────────────────────────────┘
```

## Directory Structure

```
.github/copilot-agents/
├── README.md                 # This file
├── INSTRUCTIONS.md           # Quick reference guide
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

## Agent Files

| Agent Group | Overview File | Sub-Agent Files |
|-------------|---------------|-----------------|
| Manager | [manager.md](./manager.md) | - |
| Planner | [planner.md](./planner.md) | - |
| Quality Checker | [quality-checker.md](./quality-checker.md) | - |
| Analyzer | [analyzer.md](./analyzer.md) | [code-analyzer.md](./analyzer/code-analyzer.md), [document-analyzer.md](./analyzer/document-analyzer.md) |
| Designer | [designer.md](./designer.md) | [system-designer.md](./designer/system-designer.md), [code-designer.md](./designer/code-designer.md), [document-designer.md](./designer/document-designer.md) |
| Editor | [editor.md](./editor.md) | [code-editor.md](./editor/code-editor.md), [document-editor.md](./editor/document-editor.md), [version-control-editor.md](./editor/version-control-editor.md) |
| Reviewer | [reviewer.md](./reviewer.md) | [plan-reviewer.md](./reviewer/plan-reviewer.md), [design-reviewer.md](./reviewer/design-reviewer.md), [document-reviewer.md](./reviewer/document-reviewer.md), [code-reviewer.md](./reviewer/code-reviewer.md) |
| Tester | [tester.md](./tester.md) | [test-planner.md](./tester/test-planner.md), [test-designer.md](./tester/test-designer.md), [test-editor.md](./tester/test-editor.md), [test-executor.md](./tester/test-executor.md) |

## Agent Summary

### Manager
The central coordinator that:
- Receives user requests
- Decomposes tasks
- Delegates to appropriate sub-agents
- Monitors progress
- Integrates results

### Planner
Creates actionable plans:
- Breaks down requirements
- Identifies dependencies
- Assigns resources
- Manages risks

### Analyzer (Group)
- **Code Analyzer**: Examines code structure, patterns, quality
- **Document Analyzer**: Reviews documentation completeness, accuracy

### Designer (Group)
- **System Designer**: Creates architectures and technical strategies
- **Code Designer**: Designs APIs, data models, patterns
- **Document Designer**: Plans document structure and content

### Editor (Group)
- **Code Editor**: Writes and modifies code
- **Document Editor**: Creates and updates documentation
- **Version Control Editor**: Manages commits, branches, merges, and repository operations

### Reviewer (Group)
- **Plan Reviewer**: Validates plans and strategies
- **Design Reviewer**: Evaluates system and code designs
- **Document Reviewer**: Checks documentation quality
- **Code Reviewer**: Reviews code for quality and correctness

### Tester (Group)
- **Test Planner**: Creates test strategies
- **Test Designer**: Designs test cases and scenarios
- **Test Editor**: Implements test code
- **Test Executor**: Runs tests and reports results

### Quality Checker
Monitors all activities:
- Enforces quality gates
- Tracks metrics
- Identifies risks
- Recommends improvements

## Standard Workflows

### New Feature Development
```
Planner → Analyzer → Designer → Editor → Reviewer → Tester → Quality Checker
```

### Bug Fix
```
Analyzer → Planner → Editor → Reviewer → Tester
```

### Documentation Task
```
Planner → Analyzer (Doc) → Designer (Doc) → Editor (Doc) → Reviewer (Doc)
```

### Code Refactoring
```
Analyzer → Designer → Editor → Reviewer → Tester
```

## Communication Protocol

Agents communicate using structured handoffs:

```
@[agent-name]: [task description]
Context: [relevant background]
Expected Output: [deliverable specification]
Constraints: [limitations or requirements]
```

## Quality Standards

- All deliverables must be reviewed
- Quality gates must be passed before proceeding
- Metrics are tracked throughout
- Continuous improvement is expected

## Usage

To use this agent system:

1. **Start with the Manager**: Present your request to the Manager
2. **Follow the Workflow**: Let the Manager delegate to appropriate agents
3. **Iterate as Needed**: Agents will collaborate and iterate
4. **Quality Assured**: Quality Checker monitors throughout

## Customization

These agent instructions are designed to be general-purpose. For specific projects:

1. Add project-specific standards to each agent file
2. Customize templates for your domain
3. Adjust quality thresholds as needed
4. Add domain-specific terminology

## Version

- **Version**: 1.0
- **Created**: 2026-02-03
- **Last Updated**: 2026-02-03
