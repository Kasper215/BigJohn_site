# Большой Джон — сайт пиццерии

Static website files copied from the deployed server at `/var/www/bolshoyjohn.ru` on 2026-11-11.

## Files

`index.html` and the image assets are the live files from the site directory. Server-side `.bak.*` snapshots are excluded from version control.

## Security review

- The page is static and has no local form handler, API endpoint, or inline JavaScript.
- No embedded credentials or obvious dangerous DOM sinks were found in the deployed HTML.
- The page loads `https://bigjohn.mypwa.ru/widget-chat.js`; this third-party script runs with the page's privileges and should be trusted/monitored as an external dependency.
- The matching Nginx virtual host does not currently define Content-Security-Policy, HSTS, X-Content-Type-Options, Referrer-Policy, or frame protection headers. These are server configuration findings and are not changed by this static-file repository.
