# Analyzer Agent Group

## Overview
The Analyzer group specializes in understanding, examining, and extracting insights from code and documentation. This group contains two specialized sub-agents.

## Sub-Agents

| Sub-Agent | File | Specialization |
|-----------|------|----------------|
| Code Analyzer | [code-analyzer.md](./analyzer/code-analyzer.md) | Source code analysis, patterns, architecture |
| Document Analyzer | [document-analyzer.md](./analyzer/document-analyzer.md) | Documentation quality and completeness |

## When to Use

- **Code Analyzer**: When you need to understand code structure, identify patterns, assess quality, or find issues
- **Document Analyzer**: When you need to evaluate documentation completeness, accuracy, or structure

## Collaboration Points

### Receives Input From
- **Manager**: Analysis requests with scope
- **Planner**: Context about what to analyze
- **Quality Checker**: Specific areas to investigate

### Provides Output To
- **Designer**: Insights for design decisions
- **Editor**: Areas needing improvement
- **Reviewer**: Analysis findings for review
- **Planner**: Information for planning

## Best Practices

1. **Be Thorough**: Don't skip areas even if they seem simple
2. **Be Objective**: Report findings without bias
3. **Be Specific**: Provide exact locations and examples
4. **Be Actionable**: Include recommendations for each finding
5. **Be Prioritized**: Rank findings by importance
6. **Be Clear**: Use consistent terminology and formatting
