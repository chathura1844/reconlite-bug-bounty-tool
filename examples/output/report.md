# ReconLite v2 Report

## Summary

- Tool version: **2.0.0**
- Author: **Chathura Chamantha**
- Total URLs loaded: **27**
- Domain filter: **lifeout.com**
- Categories with matches: **6**

## Findings by Category

| Category | Severity | Count | Review Hint |
|---|---|---:|---|
| `all_parameterized_urls` | **INFO** | 17 | General parameterized URLs for broad manual review. |
| `auth_pages` | **HIGH** | 12 | Check login errors, reset flow, token handling, CSRF, and rate limiting. |
| `xss_candidates` | **HIGH** | 11 | Check reflection and context: HTML text, attribute, script, or URL context. |
| `redirect_candidates` | **HIGH** | 10 | Check if external domains are accepted; test safely and avoid harmful redirects. |
| `sensitive_files` | **LOW** | 2 | Confirm exposure of public files only; do not access private data. |
| `idor_candidates` | **HIGH** | 1 | Check access control using your own authorized test accounts only. |

## Top Priority URLs

| Score | Category | URL |
|---:|---|---|
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=blog.php` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=chat.php` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=polls.php` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=online.php` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=big1gil2` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=videos.php` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=whatare.php` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=search.php` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=ClydeworldComics` |
| 94 | `auth_pages` | `https://www.lifeout.com/login.php?referer=uc4ucjax` |
| 90 | `auth_pages` | `https://www.lifeout.com/getaccountcreds.php` |
| 90 | `auth_pages` | `https://www.lifeout.com/login.php` |
| 89 | `redirect_candidates` | `https://www.lifeout.com/login.php?referer=blog.php` |
| 89 | `redirect_candidates` | `https://www.lifeout.com/login.php?referer=chat.php` |
| 89 | `redirect_candidates` | `https://www.lifeout.com/login.php?referer=polls.php` |
| 89 | `redirect_candidates` | `https://www.lifeout.com/login.php?referer=online.php` |
| 89 | `redirect_candidates` | `https://www.lifeout.com/login.php?referer=big1gil2` |
| 89 | `redirect_candidates` | `https://www.lifeout.com/login.php?referer=videos.php` |
| 89 | `redirect_candidates` | `https://www.lifeout.com/login.php?referer=whatare.php` |
| 89 | `redirect_candidates` | `https://www.lifeout.com/login.php?referer=search.php` |

## Suggested Manual Workflow

1. Start with `top_priority.txt`.
2. Review `auth_pages.txt` for login, reset, and username enumeration issues.
3. Review `redirect_candidates.txt` for open redirect and redirect-based XSS.
4. Review `xss_candidates.txt` for reflected parameters and context.
5. Review `idor_candidates.txt` only with authorized test accounts.
6. Review `api_endpoints.txt` for auth, CORS, verbose errors, and schema exposure.

## Safety Note

ReconLite does not exploit targets. It only organizes URLs for ethical manual review within authorized scope.
