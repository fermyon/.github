# Fermyon Rust Coding Guidelines

## Goals

* Improve code quality
* Reduce developer cognitive load

## Principles

* Guidelines aren't sacred, but deviations should be rare
  * If a deviation isn't rare, the guidelines should change
  * Deviations should generally be accompanied by a comment giving a rationale
* Guidelines aren't free; their advantages should be weighed against the cost of remembering and enforcing them
  * Prefer taking "no stance" on a choice where the benefit isn't clear
* Aim for code to be familiar to an "average" Rust developer (potential contributor)
  * Prefer formatter/linter defaults
  * Prefer existing community guidance, like the [Rust API Guidelines](https://rust-lang.github.io/api-guidelines/about.html)

## Code Review

Along with automated tooling, guidelines are primarily enforced in code review. "Improve code quality" is an obvious goal of code review, but it is also important to consider "reducing developer cognitive load", which applies to both authors _and_ reviewers:

* Authors should be clear if a PR is _not_ ready for close review against these guidelines. "Draft" PRs are a good signal for this.
* If a code review comment is _about_ the code itself and does not address the correctness, performance, or some other articulable aspect of "code quality", it should not block approval of a PR.
  * PR revisions are _cheap_, but not _free_; authors should exercise judgement in addressing non-blocking feedback.
  * Reviewers should be clear if feedback is based on aesthetics / personal preference: "I prefer...", "I like...", "non-blocking: ...". _Try to be equanimous about these comments being ignored._
* If you find yourself posting the same type of comment repeatedly, consider proposing a change to these guidelines _or_ reevaluating its importance.
  * Consider whether this type of feedback could be usefully automated.

## Guidelines

### Automated formatting / linting

By default, all Rust code should conform to `rustc`'s linting, `rustfmt` and `clippy`.

* Formatting exceptions via `#[rustfmt::skip]` should be avoided
* Linting exceptions via `#[allow(...)]` should be accompanied by a comment giving a rationale.

#### Exceptions

* Generated code (including 3rd party macros)
* "Vendored" external code

### Imports (`use`)

_TODO_

### Error Handling

_TODO_

### Generic arguments

_TODO_
> * When to (not) use `impl Into/AsRef`


