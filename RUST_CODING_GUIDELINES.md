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


# Code Review

* If a code review comment is _about_ the code itself and does not address the correctness, performance, or some other articulable aspect of "code quality" it should not block a PR.
  * PR revisions are cheap, but not free.
  * Be clear if a review comment is aesthetic / personal preference: "I prefer...", "I like...", "non-blocking: ...". _Try to be equanimous about these comments being ignored._
* If you find yourself posting the same type of comment repeatedly, consider proposing a change to these guidelines _or_ reevaluating its importance.
  * "Reduce developer cognitive load" applies to authors _and_ reviewers.
  * Consider whether your feedback could be usefully automated.
