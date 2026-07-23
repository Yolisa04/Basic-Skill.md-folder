---
name: Technical Writing
description: Production-ready guidance for creating clear, accurate, and maintainable technical documentation for software engineering projects.
version: 1.0.0
tags:
  - documentation
  - technical-writing
  - markdown
  - api
  - architecture
  - engineering
---

# Purpose

Provide a repeatable framework for planning, writing, reviewing, and maintaining technical documentation that serves engineers, operators, and end users.

This skill extends the Engineering Workflow and complements implementation-focused skills.

# Relationship to Engineering Workflow

Use after requirements and design have been established.

Documentation should reflect engineering decisions rather than replace them.

# When to Use

- Project documentation
- README files
- API documentation
- Architecture documentation
- Tutorials
- How-to guides
- Runbooks
- ADRs (Architecture Decision Records)
- Release notes
- Changelogs
- Internal engineering knowledge bases

# Objectives

- Improve clarity
- Reduce ambiguity
- Accelerate onboarding
- Capture engineering decisions
- Keep documentation maintainable
- Promote consistency

# Writing Principles

## Accuracy

Documentation must match system behavior.

## Clarity

Use plain language and short paragraphs.

## Completeness

Cover required information without unnecessary detail.

## Consistency

Use common terminology throughout.

## Audience First

Write for the intended reader.

# Audience Analysis

Identify:

- Experience level
- Technical background
- Goals
- Prerequisite knowledge
- Expected outcomes

Avoid assuming expert knowledge unless appropriate.

# Documentation Types

## README

Explain:

- Purpose
- Installation
- Usage
- Configuration
- Development
- License

## API Documentation

Include:

- Endpoints
- Parameters
- Authentication
- Request examples
- Response examples
- Error responses

## Tutorials

Teach through step-by-step examples.

Each step should build on the previous one.

## How-To Guides

Solve a specific task.

Avoid unrelated theory.

## Reference Documentation

Provide factual, complete, searchable information.

## Concept Guides

Explain why something works before explaining implementation details.

## Architecture Documentation

Describe:

- Components
- Data flow
- Interfaces
- Dependencies
- Constraints
- Trade-offs

# Document Structure

Recommended order:

1. Title
2. Summary
3. Audience
4. Prerequisites
5. Main Content
6. Examples
7. Troubleshooting
8. References
9. Revision History

# Markdown Best Practices

Use:

- Headings
- Lists
- Tables
- Code fences
- Relative links
- Meaningful file names

Avoid excessive nesting.

# Code Examples

Examples should be:

- Runnable
- Minimal
- Accurate
- Commented where necessary

Prefer complete examples over fragments.

# Diagrams

Use diagrams to explain:

- Architecture
- Data flow
- Deployment
- State transitions

Ensure diagrams remain synchronized with the implementation.

# Style Guide

Prefer:

- Active voice
- Concrete nouns
- Action verbs
- Consistent capitalization

Avoid:

- Marketing language
- Unexplained jargon
- Long paragraphs
- Ambiguous references

# Versioning

Document:

- Breaking changes
- Migration steps
- Deprecations
- Compatibility

# Changelogs

Record:

- Added
- Changed
- Deprecated
- Removed
- Fixed
- Security

# Review Workflow

1. Verify technical accuracy.
2. Check audience alignment.
3. Validate examples.
4. Verify links.
5. Review grammar and style.
6. Confirm consistency with implementation.

# Common Pitfalls

- Outdated screenshots
- Missing prerequisites
- Broken links
- Incomplete examples
- Hidden assumptions
- Inconsistent terminology
- Excessive detail
- Missing revision history

# Best Practices

- Keep documents close to the code.
- Update docs with every significant change.
- Prefer examples over lengthy explanations.
- Define acronyms on first use.
- Use reusable templates.

# Templates

## README

- Overview
- Installation
- Usage
- Development
- Testing
- Contributing
- License

## ADR

- Context
- Decision
- Alternatives
- Consequences

## Runbook

- Purpose
- Preconditions
- Procedure
- Validation
- Rollback

# Quality Checklist

- Audience identified
- Purpose clear
- Examples verified
- Commands tested
- Links valid
- Terminology consistent
- Formatting consistent
- Grammar reviewed

# Output Format

## Summary

Purpose and scope.

## Document Review

Strengths and improvement areas.

## Accuracy

Assessment.

## Clarity

Assessment.

## Completeness

Assessment.

## Recommendations

Prioritized improvements.

# Validation Checklist

- Accurate
- Current
- Searchable
- Consistent
- Actionable
- Well structured
- Free of broken references
- Examples validated

# Success Criteria

Documentation:

- Answers reader questions quickly
- Matches implementation
- Supports onboarding
- Enables maintenance
- Is easy to update
- Encourages reuse
- Uses consistent terminology

# Composition

Works with:

- Engineering Workflow
- Python Review
- React Development
- Kubernetes

Documentation should be treated as a production artifact and reviewed with the same discipline as source code.
