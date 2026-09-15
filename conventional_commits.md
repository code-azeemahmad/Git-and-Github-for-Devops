# Conventional Commits

It was originally heavily inspired by the Angular framework's internal commit guidelines, but it has since been adopted as the gold standard across the DevOps and software engineering industry.

## The Anatomy of a Conventional Commit

The standard dictates that a commit message should be structured like this:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

Notice the use of `auth:` in the example below. Under the Conventional Commits standard, `auth` is typically a **scope** (the part of the code you touched), while `feat` or `fix` is the **type** (the kind of work you did).

For example:

```
feat(auth): add google sign-in button
```

## The Standard Commit Types

While you can technically invent your own types, the industry universally uses this specific set:

| Type | When to use it | Example |
|------|-----------------|---------|
| `feat` | Adding a brand new feature or functionality. | `feat(checkout): add PayPal payment option` |
| `fix` | Fixing a bug in the code. | `fix(ui): resolve button alignment issue on mobile` |
| `docs` | Changes specifically to documentation (README, wikis). | `docs: update API setup instructions` |
| `chore` | Routine tasks, dependency updates, or tool configurations that don't change production code. | `chore: update Node.js to version 20` |
| `refactor` | Code changes that neither fix a bug nor add a feature (e.g., cleaning up messy code). | `refactor(auth): simplify login validation logic` |
| `style` | Changes to formatting (spaces, commas, missing semicolons) that do not affect logic. | `style: fix indentation in config.yml` |
| `test` | Adding missing tests or correcting existing ones. | `test(api): add unit tests for user endpoint` |
| `ci` | Changes to CI/CD configuration files and scripts (e.g., GitHub Actions). | `ci: add automated security scanning` |



BREAKING CHANGE: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type.