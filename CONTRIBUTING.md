# Contributing to UNICEF Venture Fund Projects

> **First time here? Start by [opening an issue](#3-opening-a-github-issue) — don't send a pull request without a conversation first.**

---

## 1. About This Organization

The UNICEF Venture Fund GitHub organization hosts open source software built by portfolio companies, UNICEF staff, and collaborators across the Digital Public Goods ecosystem. These repositories are working tools — many are prototypes, pilots, or products built for specific contexts and problems in low-resource or humanitarian settings.

Because of this, repositories in this org often move fast, carry context that isn't fully documented, and may be optimized for a particular use case rather than general adoption. This is intentional, not a deficiency.

These guidelines exist to help you contribute effectively within that reality — and to protect maintainers' time and contributors' effort.

---

## 2. Start With a Conversation

**The most important thing to understand about contributing to this org:**

> **Talk before you code.** Open a GitHub Issue before writing any code or making any change. This applies to bug fixes, new features, refactors, documentation updates, and dependency upgrades alike.

Many repositories in this org were built to solve a specific problem for a specific partner or context. A change that seems obviously good in general may not fit the direction of the project.

Opening an issue first:

- Lets maintainers confirm the change is in scope
- Saves you from investing time in work that won't be merged
- Surfaces context you might not have — about the roadmap, the deployment environment, or the partner relationship
- Gives you a space to ask questions before you're deep in implementation

If you are unsure whether something is worth raising, raise it anyway. A quick conversation is always preferable to a large PR that has to be declined.

---

## 3. Opening a GitHub Issue

A good issue gives maintainers enough information to understand what you're seeing and why it matters — without requiring back-and-forth to fill in the basics. Use the templates provided in each repository where available. When there is no template, use the structures below.

### 3.1 Reporting a Bug

**Title format:** `[Bug] Short description of what is broken`

Include the following:

#### What happened?
Describe what you observed. Be specific. "It doesn't work" is not actionable; "the form submission returns a 500 error when the phone number field is left blank" is.

#### What did you expect to happen?
Describe what the correct behavior should be.

#### Steps to reproduce
List the exact steps needed to trigger the bug. Number them.

```
1. Navigate to /dashboard
2. Click 'New Beneficiary'
3. Leave the phone number field empty
4. Click Submit
5. Observe: 500 Internal Server Error returned
```

#### Environment
- OS and version (e.g. Ubuntu 22.04, macOS 14.3)
- Browser and version if applicable
- App version or commit hash
- Deployment context if relevant (local dev / staging / production)

#### Logs and screenshots
Attach relevant error output, console logs, or screenshots. Paste log output as text in a code block rather than as an image where possible.

---

### 3.2 Proposing a Feature or Change

**Title format:** `[Feature] Short description of what you want to add or change`

#### What problem does this solve?
Describe the problem or gap you are trying to address. Be concrete — ground it in a real scenario or user need. Proposals that start with "it would be nice to have" without a specific problem are harder to evaluate.

#### Who is affected, and how?
Describe who experiences this problem — which users, roles, or deployment contexts. If this comes from a specific partner or field deployment, say so.

#### What change are you proposing?
Describe your proposed solution at a high level. You do not need to have a fully worked-out implementation — the goal here is to open a conversation, not to present a final design.

#### What alternatives have you considered?
Have you considered other approaches? Why is the one you're proposing the right fit?

#### Any additional context
Links to related issues, prior discussions, relevant documentation, or comparable implementations in other projects.

---

### 3.3 Asking a Question or Starting a Discussion

**Title format:** `[Question]` or `[Discussion]` followed by a short, specific title.

Use this type when you want to understand something about the project before proposing a change, or when you want to explore a direction with maintainers before writing it up as a formal proposal. These conversations are valuable — don't skip them to save time.

> **Tip:** Some repositories in this org have GitHub Discussions enabled for open-ended questions and community topics. Check the repository tabs before opening an issue for something that isn't a specific bug or proposal.

---

## 4. After Your Issue Is Acknowledged

Wait for a response from the maintainers before starting work. Maintainers will either:

- Confirm the issue is in scope and invite you to submit a PR
- Ask clarifying questions
- Let you know the change does not fit the project's current direction
- Suggest a different approach to the same problem

If you have not received a response within two weeks, a polite follow-up comment on the issue is welcome.

> ⚠️ **Do not open a pull request without a linked, acknowledged issue.**
> PRs submitted without a prior conversation will likely be closed, regardless of their technical quality. This is not a reflection on the contribution — it is a recognition that maintainer review time is finite and should be spent on changes that have been confirmed as welcome.

---

## 5. Submitting a Pull Request

Once a maintainer has confirmed your issue is in scope, you are ready to contribute.

### 5.1 Before You Open the PR

- Fork the repository and create a branch from `main` (or the branch specified by the maintainers)
- Name your branch descriptively — e.g. `fix/beneficiary-form-500` or `feat/offline-sync-queue`
- Keep your change focused. One issue, one PR. Avoid bundling unrelated fixes.
- Run the project's existing tests and add tests for new behavior where the project has a test suite
- Check that your changes do not introduce new linting errors

### 5.2 Writing a Good PR Description

Your PR description should answer:

- **What does this PR do?** (one sentence summary)
- **Which issue does it close?** (use `Closes #<issue number>` so it links automatically)
- **How has it been tested?**
- **Are there any known limitations or follow-up items?**

Keep the description short and factual. Link to the issue for full context — don't repeat it all in the PR.

### 5.3 During Review

- Be responsive. If a reviewer asks a question, reply within a reasonable time.
- Treat feedback as collaborative, not evaluative. Reviewers are trying to understand and improve the change, not to reject it.
- If you disagree with a requested change, explain your reasoning calmly in the thread.
- Avoid force-pushing to a branch once a PR is under review, as it makes it harder to track what changed.

---

## 6. What Maintainers Will Look For

Maintainers will review your contribution for the following, in rough order of priority:

1. **Fit** — confirmed in the issue conversation before work started
2. **Correctness** — does it do what it says, without breaking existing behavior?
3. **Simplicity** — is this the smallest change that solves the problem?
4. **Deployment compatibility** — many projects target low-bandwidth, offline-first, or resource-constrained contexts
5. **License compatibility** — all dependencies must be compatible with the repository's license
6. **Code style** — consistency with the existing codebase

Maintainers may also consider whether a proposed change creates maintenance burden that the project team cannot sustain.

---

## 7. What to Expect

Repositories in this org are maintained by small teams with significant competing responsibilities. Response times will vary. Please be patient.

- **Issues:** maintainers aim to respond within two weeks, though this may take longer during active sprints or field deployments
- **PRs:** reviews are typically completed within two to four weeks of the PR being submitted
- **If a repository appears unmaintained** (no activity in over six months), please note this in your issue

Contributions may be declined even if they are technically sound. This is not a judgment on the quality of your work — it reflects the specific constraints of the project.

---

## 8. Licensing

By submitting a contribution to any repository in this organization, you agree that your contribution is made under the same license as the repository you are contributing to.

If you are contributing on behalf of an organization, ensure you have the appropriate permissions to do so under your employer's intellectual property policies.

Do not introduce dependencies with licenses incompatible with the repository's existing license. When in doubt, raise the question in your issue before writing code.

---

## 9. Code of Conduct

All contributors are expected to follow the [UNICEF Venture Fund Code of Conduct](./CODE_OF_CONDUCT.md). Please read it before participating in any repository in this organization.

---

## 10. Thank You

Every contribution to this organization — whether a bug report, a question, a documentation fix, or a new feature — directly supports technology built to serve children and communities around the world. We appreciate you taking the time to engage with us thoughtfully.

---
