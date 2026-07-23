---
name: Engineering Workflow
description: Structured engineering workflow for software design, implementation, validation, and delivery.
version: 1.0.0
tags:
  - engineering
  - software
  - architecture
  - planning
  - implementation
---

# Purpose

Provide a repeatable engineering process for solving software problems.

The workflow emphasizes understanding before implementation, explicit assumptions, risk management, iterative delivery, and validation.

---

# When to Use

Use this skill when:

- Designing new software
- Extending an existing system
- Refactoring
- Investigating bugs
- Planning architecture
- Reviewing technical proposals
- Delivering production features

---

# Objectives

- Understand requirements
- Clarify ambiguity
- Identify constraints
- Produce maintainable designs
- Reduce implementation risk
- Validate outcomes
- Document decisions

---

# Engineering Principles

## Simplicity

Prefer simple solutions over complex ones.

---

## Correctness

Ensure behavior matches requirements before optimizing.

---

## Maintainability

Optimize for future engineers.

---

## Observability

Design systems that expose useful diagnostics.

---

## Security

Treat security as a default requirement.

---

## Reliability

Design for graceful failure.

---

## Scalability

Consider future growth without premature optimization.

---

# Workflow

## Phase 1 – Understand

Identify:

- Goals
- Constraints
- Stakeholders
- Success metrics

Document assumptions explicitly.

---

## Phase 2 – Analyze

Break work into independent components.

Identify:

- Inputs
- Outputs
- Dependencies
- Interfaces

---

## Phase 3 – Design

Produce:

- Architecture
- Data flow
- Interfaces
- Trade-offs

Compare multiple approaches where appropriate.

---

## Phase 4 – Plan

Estimate:

- Complexity
- Risks
- Milestones

Prioritize incremental delivery.

---

## Phase 5 – Implement

During implementation:

- Keep functions focused
- Minimize coupling
- Prefer composition
- Write self-documenting code
- Avoid premature abstraction

---

## Phase 6 – Validate

Validate:

- Functional correctness
- Edge cases
- Performance expectations
- Security implications

---

## Phase 7 – Review

Evaluate:

- Maintainability
- Readability
- Documentation
- Test coverage

---

## Phase 8 – Deliver

Provide:

- Summary
- Decisions
- Remaining risks
- Future improvements

---

# Decision Log

Record:

Issue

Decision

Alternatives

Trade-offs

Confidence

---

# Risk Assessment

Classify risks.

Critical

High

Medium

Low

For every risk include:

Cause

Impact

Likelihood

Mitigation

---

# Best Practices

Think before coding.

Prefer incremental changes.

Document assumptions.

Reduce complexity.

Design for testing.

Avoid hidden dependencies.

Keep modules cohesive.

Review interfaces first.

Fail loudly.

Validate continuously.

---

# Common Pitfalls

Skipping requirements.

Mixing design and implementation.

Ignoring edge cases.

Overengineering.

Premature optimization.

Unclear ownership.

Missing validation.

Weak documentation.

---

# Output Format

## Summary

...

## Requirements

...

## Assumptions

...

## Architecture

...

## Design Decisions

...

## Risks

...

## Implementation Plan

...

## Validation

...

## Recommendations

...

---

# Validation Checklist

Requirements understood.

Assumptions documented.

Interfaces defined.

Architecture consistent.

Risks identified.

Implementation feasible.

Validation complete.

Documentation updated.

---

# Success Criteria

The solution:

✓ Solves the stated problem

✓ Meets functional requirements

✓ Is maintainable

✓ Is testable

✓ Is documented

✓ Can be extended safely

✓ Has identified risks

✓ Includes validation evidence

---

# Composition

This skill serves as the foundation for:

- Python Review
- React Development
- Kubernetes
- Technical Writing

All specialized skills should inherit this workflow and extend it rather than duplicate it.
