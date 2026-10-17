# SSO cleanup: intended end state (draft note, not live)

Prepared with the October 2026 redesign draft. Nothing in this note has been applied live.

## Finding

The redesign draft contains no /sso route or page, no links to /sso, and no references to sso.nivelatolabs.com anywhere in the site files (checked by full-text search of the draft worktree). The only "sso" matches in the draft are the word "crossorigin" in font preconnect tags, which is unrelated.

## Intended end state (live change, needs its own go-ahead)

- The /sso route (a pre-September UI trace) is removed, and requests to it redirect to the sign-in destination.
- The sso.nivelatolabs.com subdomain (also a pre-September UI trace) is removed, and requests to it redirect to the same sign-in destination.
- The sign-in destination is the site's existing sign-in: https://login.nivelatolabs.com
- Sign-in itself is not removed or changed. It is the redirect target, not a target of the cleanup.

## Not done in this draft

- No DNS records were changed.
- No Cloudflare routes, redirects, or worker rules were changed.
- No sign-in links or pages were touched. The draft's existing links to https://login.nivelatolabs.com remain exactly as they were.
