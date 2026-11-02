# Wiki.js (LazyCat LPK)

Modern wiki and knowledge base.

- Upstream: https://github.com/requarks/wiki
- Image: `requarks/wiki:3.0.2` (mirror mode, digest-matched)
- License: AGPL-3.0 (full text in `content/licenses/LICENSE`)
- Containers: Wiki.js + PostgreSQL 16

## Notes

- Wiki.js 3.x is **PostgreSQL-only** — no SQLite path, hence the sidecar.
- DB connection via `DB_TYPE=postgres` + `DB_HOST/DB_PORT/DB_NAME/DB_USER/DB_PASS`;
  the password comes from a platform stable secret.
- The admin account is created in the browser setup wizard on first visit — no seeded credential.
- Content and the git-backed repo persist on `/lzcapp/var/{content,repo}`; database on
  `/lzcapp/var/pgdata`.
- No mail service configured.
- Not yet verified on a real device.
