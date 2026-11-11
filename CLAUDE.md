@AGENTS.md

## This repo

- One Doc space, `cloud-console/` (Cloud Console, Cloud only), on `docs-v2`. There are no release branches.
- Until the cutover, `main` is the legacy Docusaurus site and writers merge there. Bring their fixes to `docs-v2` with `git merge main`, then check new pages' front matter (`type`, `description`) and links.
- The pages say "WSO2 Cloud", the product's name. "Cloud Console" is the Doc space's and the family's name on WSO2 Docs.
- Link to another Doc space with `docs:<doc-space>/<edition>/<page>` (for example `docs:agent-manager/cloud/`). A service not on WSO2 Docs yet keeps a plain link to its current site, since a `docs:` link to it fails the build.
- `redirects.yaml` maps the old `docs.wso2.com/docs/<page>` addresses: add an entry when you move or remove a page.
