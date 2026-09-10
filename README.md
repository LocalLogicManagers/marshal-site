# Marshal

Product/marketing page for Marshal, the MCP (Model Context Protocol) server
built by Local Logic Management that lets any AI assistant push code, run
tests, and deploy across a client's git host and deploy platform of choice.

Static site, no build step — same pattern as threshold-site: `index.html`
for markup/content, `styles.css` for shared design tokens and chrome (nav,
footer, buttons, deploy-log mock). Served via GitHub Pages at
`marshal.locallogicmanagement.com`.

The hero's "deploy log" panel and the sample `marshal.config.yml` are both
illustrative — Marshal is in private beta, and the config shape may still
change before general release. The signup form has no backend wired yet;
it opens a `mailto:` draft to hello@locallogicmanagement.com. Swap in a
real endpoint (Formspree, ConvertKit, Mailchimp, etc.) before launch.

## Deploy it (same pattern as Kronos / Threshold / Warden)

1. Create a new GitHub repo in the `LocalLogicManagers` org — e.g. `marshal-site`.
2. Push `index.html`, `styles.css`, and `CNAME` (already set to
   `marshal.locallogicmanagement.com`) to the repo's default branch.
3. In the repo's Settings → Pages, set the source to that branch (root).
4. In Wix DNS (where the domain's DNS is managed), add a CNAME record for
   `marshal` pointing at `<your-github-username>.github.io`, matching the
   setup already used for kronos/threshold/warden/beacon.
5. Once DNS + Pages propagate, the page is live at
   `marshal.locallogicmanagement.com`, and the existing "Marshal →" link on
   the main site (which currently 404s/SSL-errors because nothing is hosted
   there yet) will resolve correctly.

## Files here

- `index.html` — the marketing page.
- `styles.css` — shared tokens, nav, footer, buttons, deploy-log component.
- `CNAME` — GitHub Pages custom-domain file for `marshal.locallogicmanagement.com`.
