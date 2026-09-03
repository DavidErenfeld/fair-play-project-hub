# Fair Play Project Hub — Phase 0

This repository is currently in **Phase 0 only**.

Phase 0 is an **External Context Reading POC**. It exists to test whether an external ChatGPT conversation can open Markdown files from a public Netlify URL, read exact values, and see updated values after a later Git push and deployment.

The deployment contains **synthetic public information only**.

## Public vs private

The GitHub repository may be private while the Netlify site is intentionally public.

Anything deployed to Netlify must be considered public.

No real Fair Play documentation belongs in this POC.

## Out of scope

No full Project Hub implementation is authorized yet.

Do not add documentation-site tooling, application source, authentication, or real project context.

Phase 1 must not begin until explicit user approval:

`Phase 0 approved — proceed to full Project Hub`

## Local verification

From the repository root:

```sh
find . -not -path './.git/*' | sort
cat site/context/chats/test.md
grep -n 'Disallow: /' site/robots.txt || true
cat site/_headers
cat netlify.toml
```

Serve the `site` directory with any static file server if you want to inspect pages locally. There is no build step and no package manager.
