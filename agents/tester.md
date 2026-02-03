# Tester Agent Group

## Overview
The Tester group specializes in all aspects of testing, from planning to execution. This group contains four specialized sub-agents that work together to ensure comprehensive test coverage.

## Sub-Agents

| Sub-Agent | File | Specialization |
|-----------|------|----------------|
| Test Planner | [test-planner.md](./tester/test-planner.md) | Test strategy and planning |
| Test Designer | [test-designer.md](./tester/test-designer.md) | Test case and scenario design |
| Test Editor | [test-editor.md](./tester/test-editor.md) | Test code and automation |
| Test Executor | [test-executor.md](./tester/test-executor.md) | Test execution and reporting |

## When to Use

- **Test Planner**: When you need to create test strategies or test plans
- **Test Designer**: When you need to design test cases or scenarios
- **Test Editor**: When you need to write or maintain test code
- **Test Executor**: When you need to run tests and report results

## Testing Workflow

```
Test Planner → Test Designer → Test Editor → Test Executor
      ↓              ↓              ↓              ↓
  Strategy       Test Cases     Test Code      Results
  & Plan        & Scenarios    & Automation   & Defects
```

## Collaboration Points

### Receives Input From
- **Manager**: Test requests and priorities
- **Planner**: Project plans including test tasks
- **Designer**: Designs to test against
- **Editor**: Code/docs to test

### Provides Output To
- **Manager**: Test results and status
- **Editor**: Defects requiring fixes
- **Quality Checker**: Quality metrics from testing
- **Reviewer**: Test artifacts for review

## Quality Metrics

- **Test Coverage**: % of requirements covered
- **Defect Density**: Defects per unit of code
- **Pass Rate**: % of tests passing
- **Defect Leakage**: Defects found post-release
- **Test Execution Rate**: Tests run per cycle
