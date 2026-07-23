---
name: Python Review
description: Comprehensive methodology for reviewing Python code for correctness, maintainability, performance, security, testing, and production readiness.
version: 1.0.0
tags:
  - python
  - code-review
  - software-engineering
  - quality
  - testing
  - security
  - performance
---

# Purpose

Provide a structured, repeatable process for reviewing Python code with a focus on correctness, maintainability, reliability, security, performance, and production readiness.

This skill extends the Engineering Workflow foundation and applies it specifically to Python codebases.

---

# Relationship to Engineering Workflow

This skill assumes the Engineering Workflow has already been followed.

Use this skill after:

- Requirements are understood
- Design decisions are documented
- Implementation is complete
- Code is ready for review

Do not use this skill as a substitute for software design.

---

# When to Use

Use this skill for:

- Pull Requests
- Merge Requests
- Production releases
- Security reviews
- Refactoring reviews
- Performance reviews
- Architecture validation
- Library development
- API development
- Automation scripts
- Data processing pipelines
- CLI tools

---

# Objectives

Review code for:

- Functional correctness
- Code quality
- Readability
- Pythonic practices
- Type safety
- Performance
- Security
- Reliability
- Maintainability
- Testability

---

# Review Philosophy

The objective is to improve software rather than criticize authors.

Every recommendation should explain:

- What
- Why
- Risk
- Suggested improvement

Avoid subjective preferences unless supported by measurable benefits.

---

# Review Workflow

## Phase 1 — Understand Context

Identify:

- Purpose
- Requirements
- Expected behaviour
- Public API
- Dependencies
- Runtime environment

Questions:

- What problem is solved?
- Is the implementation appropriate?
- Are assumptions documented?

---

## Phase 2 — Correctness

Verify:

- Logic
- Algorithms
- Boundary conditions
- Error handling
- Input validation
- Expected outputs

Look for:

- Off-by-one errors
- Incorrect conditions
- Missing branches
- Dead code
- Impossible states
- Infinite loops

---

## Phase 3 — Python Idioms

Encourage idiomatic Python.

Prefer:

- Context managers
- Enumerate
- Zip
- Comprehensions
- Generator expressions
- Dataclasses
- pathlib
- f-strings

Avoid unnecessary Java-style patterns.

---

## Phase 4 — Maintainability

Review:

- Function length
- Class size
- Module organization
- Coupling
- Cohesion

Prefer:

Small focused functions

Single responsibility

Meaningful names

Minimal nesting

---

## Phase 5 — Types

Review:

Type hints

Return annotations

Optional values

Generics

Protocols

TypedDict

Literal

NewType

Check consistency.

Avoid partially typed APIs.

---

## Phase 6 — Error Handling

Verify:

Meaningful exceptions

Appropriate exception hierarchy

Specific catches

Context preservation

Resource cleanup

Avoid:

```
except:
```

Prefer:

```
except ValueError:
```

---

## Phase 7 — Performance

Evaluate:

Algorithm complexity

Memory usage

Repeated work

Large allocations

I/O

Serialization

Database access

Network usage

Caching opportunities

---

## Phase 8 — Security

Review for:

Injection

Path traversal

Unsafe deserialization

Command execution

Weak randomness

Credential exposure

Secrets

Authentication

Authorization

Session handling

Input validation

Output escaping

---

## Phase 9 — Testing

Evaluate:

Coverage

Edge cases

Failure cases

Integration tests

Regression tests

Fixtures

Mocks

Assertions

Deterministic behaviour

---

## Phase 10 — Documentation

Check:

Docstrings

Examples

Public APIs

README updates

Breaking changes

Migration notes

---

# Severity Model

## Critical

Must be fixed before merge.

Examples:

Remote code execution

Data corruption

Authentication bypass

Race conditions

Unsafe SQL

Credential leaks

---

## High

Likely production failures.

Examples:

Incorrect algorithms

Resource leaks

Concurrency bugs

Unhandled failures

Broken APIs

---

## Medium

Maintainability concerns.

Examples:

Duplicate logic

Weak abstractions

Poor naming

Complex methods

Large modules

---

## Low

Quality improvements.

Examples:

Formatting

Minor optimizations

Documentation

Small refactoring

---

## Nit

Optional suggestions.

Examples:

Naming preference

Alternative syntax

Readability

Consistency

---

# Correctness Checklist

Verify:

Business logic

State transitions

Return values

Error paths

Input validation

Edge cases

Boundary conditions

---

# Performance Checklist

Review:

Time complexity

Memory complexity

Repeated allocations

Repeated queries

Repeated API calls

Object creation

String concatenation

Large copies

Blocking operations

---

# Security Checklist

Review:

Secrets

Tokens

Passwords

API keys

Encryption

TLS usage

Permissions

Authentication

Authorization

Logging

PII

---

# Typing Checklist

Review:

Complete annotations

Public interfaces

Optional handling

Protocols

Dataclasses

Enums

TypedDict

Generics

Forward references

---

# API Design Checklist

Evaluate:

Consistency

Predictability

Naming

Extensibility

Backward compatibility

Documentation

---

# Async Review

Check:

async/await correctness

Blocking calls

Task cancellation

Timeout handling

Context propagation

Resource cleanup

---

# Concurrency Review

Review:

Thread safety

Locks

Deadlocks

Shared state

Atomic operations

Multiprocessing boundaries

---

# Logging Review

Ensure logs are:

Useful

Structured

Actionable

Consistent

Safe

Never log:

Passwords

Tokens

Secrets

Personal information

---

# Exception Review

Prefer:

Specific exceptions

Helpful messages

Exception chaining

Recovery strategies

Avoid:

Silent failures

Hidden exceptions

Broad catches

---

# Dependency Review

Evaluate:

Maintenance

Popularity

Security

License

Transitive dependencies

Update frequency

Replace abandoned packages.

---

# Refactoring Guidance

Recommend refactoring when:

Function >50 lines

Deep nesting

Large classes

Duplicate logic

Hidden coupling

Poor naming

Long parameter lists

---

# Readability Principles

Prefer:

Explicit code

Clear intent

Meaningful variables

Simple expressions

Predictable flow

Avoid cleverness.

---

# Python Best Practices

Use:

pathlib

dataclasses

typing

contextlib

logging

enum

collections

functools

itertools

Avoid reinventing standard library features.

---

# Common Pitfalls

Mutable default arguments

Hidden global state

Circular imports

Unused imports

Magic numbers

Broad exceptions

Deep inheritance

Monkey patching

Implicit behaviour

Excessive metaprogramming

---

# Anti-Patterns

God objects

Massive utility modules

Long functions

Feature envy

Copy-paste programming

Premature optimization

Boolean parameter explosion

Nested conditionals

---

# Testing Guidance

Tests should include:

Happy path

Failure path

Boundary conditions

Invalid input

Performance-sensitive paths

Regression cases

Property-based tests where appropriate

---

# Documentation Expectations

Public functions require:

Purpose

Parameters

Returns

Raises

Examples

Side effects

---

# Review Output Format

## Summary

Brief overview of code quality.

---

## Strengths

Positive observations.

---

## Findings

Each finding should include:

Severity

Location

Description

Impact

Recommendation

Example fix (if appropriate)

---

## Security Review

Pass or findings.

---

## Performance Review

Pass or findings.

---

## Testing Review

Coverage assessment.

Missing scenarios.

---

## Maintainability

Overall maintainability assessment.

---

## Final Recommendation

Choose one:

Approve

Approve with Minor Changes

Request Changes

Reject

---

# Validation Checklist

✓ Code executes correctly

✓ Public APIs documented

✓ Type hints complete

✓ Exceptions handled

✓ Logging appropriate

✓ Tests sufficient

✓ Security reviewed

✓ Performance acceptable

✓ No duplicated logic

✓ Naming consistent

✓ Dependencies acceptable

✓ Documentation updated

---

# Success Criteria

A successful review:

- Identifies real issues without unnecessary noise
- Explains reasoning behind recommendations
- Prioritizes findings by impact
- Improves maintainability
- Preserves readability
- Encourages Pythonic solutions
- Supports long-term evolution of the codebase
- Produces actionable, evidence-based feedback

---

# Composition

This skill composes with:

- Engineering Workflow (required foundation)
- React Development (for Python-backed web services)
- Kubernetes (for deployment readiness)
- Technical Writing (for documenting APIs, libraries, and review findings)

When multiple skills apply, perform the Engineering Workflow first, then conduct the Python Review before assessing deployment or documentation concerns.
