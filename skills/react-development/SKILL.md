---
name: React Development
description: Production-ready guidance for building, reviewing, and maintaining modern React applications.
version: 1.0.0
tags:
  - react
  - frontend
  - javascript
  - typescript
  - ui
  - web
---

# Purpose

Provide a consistent engineering workflow for designing, implementing, reviewing,
and maintaining modern React applications.

This skill extends the Engineering Workflow foundation.

# When to Use

- Building new React applications
- Reviewing pull requests
- Refactoring components
- Improving performance
- Designing component libraries
- Implementing accessibility
- Preparing production releases

# Objectives

- Build maintainable applications
- Promote reusable components
- Improve rendering performance
- Ensure accessibility
- Encourage testability
- Reduce technical debt

# Workflow

## 1. Understand Requirements

- Identify user goals
- Define functional requirements
- Capture constraints
- Clarify assumptions

## 2. Design

Prefer:

- Composition over inheritance
- Small focused components
- Feature-based organization
- Explicit interfaces
- Predictable data flow

## 3. Component Architecture

Every component should have:

- Single responsibility
- Clear props
- Stable API
- Minimal internal state

Prefer:

- Functional components
- Custom hooks
- Controlled components
- Pure rendering

Avoid:

- Massive components
- Prop drilling across many levels
- Duplicate state
- Hidden side effects

## 4. State Management

Use the simplest solution that satisfies requirements.

Typical progression:

- Local state (`useState`)
- Reducers (`useReducer`)
- Context for shared state
- External state libraries only when justified

Avoid storing derived state.

## 5. Hooks

Follow the Rules of Hooks.

Custom hooks should:

- Encapsulate behavior
- Avoid UI concerns
- Be reusable
- Have descriptive names

## 6. Rendering

Prefer declarative rendering.

Keep render logic simple.

Avoid unnecessary re-renders by:

- Stable props
- Stable callbacks when beneficial
- Memoization only after measurement

## 7. React Patterns

Encourage:

- Composition
- Render props (when appropriate)
- Custom hooks
- Context boundaries
- Suspense-compatible patterns

## 8. Accessibility

Every UI should support:

- Keyboard navigation
- Semantic HTML
- Visible focus
- Screen readers
- Sufficient color contrast
- Proper labels

Never rely solely on color.

## 9. Styling

Maintain consistency.

Prefer:

- Design systems
- CSS Modules
- Tailwind
- CSS-in-JS only when justified

Avoid inline styles for complex layouts.

## 10. Performance

Review:

- Rendering frequency
- Bundle size
- Code splitting
- Lazy loading
- Virtualization for long lists

Measure before optimizing.

## 11. Error Handling

Provide:

- Error boundaries
- User-friendly fallback UI
- Retry mechanisms where appropriate

## 12. Testing

Test:

- User behavior
- Accessibility
- Component interactions
- Edge cases

Prefer testing behavior over implementation details.

## 13. Folder Organization

Example:

src/
  app/
  features/
  components/
  hooks/
  services/
  utils/
  assets/
  tests/

Group by feature when applications grow.

# Best Practices

- Prefer TypeScript where possible
- Keep components focused
- Reuse logic through hooks
- Validate props and inputs
- Keep side effects isolated
- Remove dead code
- Document public APIs

# Common Pitfalls

- Overusing Context
- Premature memoization
- Deep prop drilling
- Duplicate state
- Business logic inside UI
- Missing cleanup in effects
- Ignoring accessibility
- Oversized components

# Review Checklist

- Requirements implemented
- Components reusable
- Naming consistent
- Hooks follow rules
- Effects minimal
- State normalized
- Accessibility verified
- Performance acceptable
- Tests included
- Documentation updated

# Output Format

## Summary

Overall assessment.

## Strengths

Positive observations.

## Findings

For each issue include:

- Severity
- Location
- Explanation
- Recommendation

## Performance

Assessment and opportunities.

## Accessibility

Compliance observations.

## Testing

Coverage summary and gaps.

## Final Recommendation

- Approve
- Approve with Changes
- Request Changes

# Validation Checklist

- Functional requirements met
- No React warnings
- No unnecessary re-renders identified
- Accessible interactions
- Responsive layouts
- Error states handled
- Loading states handled
- Tests passing
- Build succeeds

# Success Criteria

A successful React implementation:

- Is maintainable
- Is accessible
- Performs well
- Uses predictable state
- Encourages reuse
- Is easy to test
- Supports future extension

# Composition

Use with:

- Engineering Workflow
- Python Review (for backend integration)
- Kubernetes (deployment)
- Technical Writing (documentation)
