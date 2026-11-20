# docs-wso2cloud

A Content repo of WSO2 Docs (docs.wso2.com). It holds this Doc space:

| Directory | Doc space | Editions and branches |
|---|---|---|
| `cloud-console/` | Cloud Console: the WSO2 Cloud console's docs, the family Cloud of the Cloud Console family | Cloud on `docs-v2/main` |

It has no Self-hosted version, so there are no release branches. Docs releases are tagged `cloud-<YYYY.MM.DD>.<n>`.

Until the cutover, `main` is still the legacy Docusaurus site and its deploy pipeline, and writers still merge there. `docs-v2/main` is the WSO2 Docs main line, generated from `main` until the cutover: don't commit to it by hand. At the cutover it becomes the repo's main line.

The Doc space directory holds `docspace.yaml` (the Doc space manifest), `editions.yaml` (per-Edition variables), `redirects.yaml` (page moves, and the map from the old `docs.wso2.com/docs/…` addresses), `docs/` (pages; folders are the menu) and `assets/` (images).

The repo root holds only shared files: this README, `CODEOWNERS`, the release workflow (`.github/workflows/docs-bundle-release.yml` releases a Docs bundle on every merge to the main line, `docs-v2/main` until the cutover), the branch ruleset (`.github/branch-ruleset.json`), the editor settings, and `AGENTS.md` and `CLAUDE.md` for agents (they point to `npx @wso2-enterprise/docs help`). The Platform-managed files come from `templates/content-repo/` in `wso2-enterprise/choreolabs-docs`.

The tools are on GitHub Packages. Once per machine, make a classic personal access token with `read:packages` (authorised for the `wso2-enterprise` organisation's SSO if it asks), then run `npm login --scope=@wso2-enterprise --auth-type=legacy --registry=https://npm.pkg.github.com` with your GitHub user name and the token as the password. This repo's `.npmrc` names the registry for `@wso2-enterprise`; it holds no token.

Get started, from setting up your computer to a Docs release going live: the WSO2 Docs Platform's README, https://github.com/wso2-enterprise/choreolabs-docs#readme.
