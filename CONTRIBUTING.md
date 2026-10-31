# PQR – Repository collaboration rules

**Organization:** Philomath Quantitative Research (PQR)  
**Applies to:** All contributors, collaborators, and AI coding agents  
**Status:** Interim GitHub policy, pending migration to GitLab

These rules are mandatory. In private repositories on GitHub Free, certain branch protections and CI merge requirements **cannot be enforced by GitHub**. Technical access does **not** constitute permission to bypass them.

## 1. Branches and pull requests

1. **Never push directly to `main` or `master`.** Changes to the stable branch must enter through an approved pull request (PR), including changes made by administrators.
2. **Only organization owners and designated repository administrators may push directly to `develop`.** All other collaborators must use separate working branches.
3. Use descriptive names such as `feature/description`, `fix/description`, or `experiment/description`. Normally open a PR into `develop`.
4. Release PRs normally merge `develop` into `main`/`master`, and only authorized administrators may merge them.
5. An urgent `hotfix/*` PR may target the stable branch directly with administrator authorization; the fix must also be integrated into `develop`.
6. Do not force-push, overwrite others' work, or delete shared branches without authorization.
7. Some small repositories have no `develop` branch. Follow their documented alternative (usually working branch → PR into `main`).

## 2. Quality, testing and review

1. **All applicable CI checks must succeed before merging.** Never treat failed, cancelled, incomplete, or missing required checks as a pass.
2. CI should run on PRs to `develop` and `main`/`master`, direct pushes to `develop`, and merges into the stable branch.
3. Administrators who push to `develop` must promptly repair or revert resulting CI failures.
4. If CI is not yet configured, perform and document the manual validation required by the repository administrator.
5. Explain what changed, why, and how it was tested in each PR. Significant or sensitive changes should receive an independent review where a qualified reviewer is available.
6. Do not merge into the stable branch, bypass reviews, or ignore known serious problems without explicit administrator approval.

## 3. Releases and deployment

1. In software projects configured for automated releases, a successful merge into `main`/`master` triggers post-merge validation; **only successful validation may publish a versioned release**.
2. Release tags, manual releases, production deployments, and release automation must not be modified or triggered without authorization.
3. Research, documentation, data, infrastructure and website projects may have different release/deployment schedules; follow each repository's stated policy.

## 4. Security and access

1. Never commit or reveal passwords, API keys, tokens, private keys, or other secrets, including in CI logs, sample files, PRs, or issue discussions.
2. Do not disclose private source code or organizational information outside authorized channels.
3. Enable two-factor authentication. Never share accounts or credentials.
4. Do not change repository access, visibility, branch policy, CI/CD workflows, security controls, or applications without authorization.
5. Keep third-party tools and coding agents on the minimum required access. **The human operator is responsible for every AI-assisted contribution.**
6. Report suspected breaches, exposed credentials, and accidental rule violations immediately.

## 5. Exceptions and accountability

Exceptions require **prior, explicit authorization** from a repository administrator and must be documented in an issue or PR. In urgent incidents, document any approved emergency action as soon as practical.

These rules remain applicable even when GitHub technically permits the action. Repository-specific guidance may add stricter requirements.

