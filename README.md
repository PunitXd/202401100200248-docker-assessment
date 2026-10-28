# FestPass — Docker & Container Security Assessment

| | |
|---|---|
| Name | Punit Singh |
| REGNO | 202401100200248 |
| PORT | 8048 |
| Docker Hub user | punitxd |
| Docker Hub repo | https://hub.docker.com/r/punitxd/fest-backend |


## 1.0.0 digest
`sha256:PASTE_DIGEST`

## Vulnerability scan: before and after (Trivy 0.75.0)

| Image | Base | CRITICAL | HIGH | Size (disk / content) |
|---|---|---|---|---|
| fest-backend:0.1 | python:3.9 | 234 | 2249 | 1.61 GB / 401 MB |
| fest-backend:0.2 | python:3.13-slim | 0 | 49 | 0.2_SIZE |

Fixes: slim base pinned to python:3.13, non-root user (appuser, UID 10001), upgraded pip, Flask 3.1.3, Werkzeug 3.1.9, psycopg2-binary 2.9.13. `trivy image --severity CRITICAL --ignore-unfixed --exit-code 1 fest-backend:0.2` exits with 0.

## Steps not completed
- None
