# Designer Agent Group

## Overview
The Designer group specializes in creating designs for systems, code, and documentation. This group contains three specialized sub-agents that collaborate to produce comprehensive design artifacts.

## Sub-Agents

| Sub-Agent | File | Specialization |
|-----------|------|----------------|
| System Designer | [system-designer.md](./designer/system-designer.md) | Architecture, infrastructure, technical strategy |
| Code Designer | [code-designer.md](./designer/code-designer.md) | APIs, data models, patterns, interfaces |
| Document Designer | [document-designer.md](./designer/document-designer.md) | Information architecture, content organization |

## When to Use

- **System Designer**: When you need high-level architecture, infrastructure planning, or technology decisions
- **Code Designer**: When you need detailed software design, APIs, data models, or patterns
- **Document Designer**: When you need to plan document structure, templates, or content strategy

## Collaboration Points

### Receives Input From
- **Manager**: Design requests and constraints
- **Planner**: Scope and requirements
- **Analyzer**: Analysis insights and recommendations

### Provides Output To
- **Editor**: Designs for implementation
- **Reviewer (Design Reviewer)**: Designs for review
- **Tester (Test Designer)**: Designs for test planning

## Design Principles

1. **Simplicity**: Prefer simple solutions over complex ones
2. **Consistency**: Maintain patterns across designs
3. **Flexibility**: Design for change and extension
4. **Clarity**: Make intent obvious
5. **Documentation**: Document decisions and rationale

## Design Review Checklist
- [ ] Requirements are addressed
- [ ] Design is consistent with existing patterns
- [ ] Trade-offs are documented
- [ ] Edge cases are considered
- [ ] Security implications reviewed
- [ ] Performance implications considered
- [ ] Testability is built in
