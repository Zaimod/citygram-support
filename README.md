# Citygram Support

Static pages for **Citygram**, a nonogram puzzle game for iOS. Hosted on GitHub
Pages and served publicly — these pages are linked from the App Store listing,
from inside the app, and from the Google AdMob console.

## Live pages

| Page | URL |
| --- | --- |
| Support | https://zaimod.github.io/citygram-support/ |
| Privacy Policy | https://zaimod.github.io/citygram-support/privacy |

## Files

```
index.html      Support page — contact, FAQ
privacy.html    Privacy Policy — GDPR, international transfers, US privacy
.nojekyll       Disables Jekyll processing; files are served as-is
```

## Where these URLs are referenced

Changing a URL means updating it in **four** places. Keep them in sync:

1. App Store Connect → App Information → Privacy Policy URL
2. App Store Connect → App Privacy
3. Google AdMob → Privacy & messaging → GDPR message → app privacy policy URL
4. The app itself — `PRIVACY_POLICY_URL` in `app/settings.tsx` (requires a new
   build to take effect)

## Updating a page

Edit the HTML directly on GitHub or push a commit to `main`. GitHub Pages
redeploys automatically within a few minutes. Check the **Actions** tab for the
`pages-build-deployment` job.

Verify the result rather than trusting the browser, which caches aggressively:

```bash
curl -sI https://zaimod.github.io/citygram-support/privacy | head -1
```

When changing the Privacy Policy, bump the "Last updated" date at the top of
the page — App Review and the policy's own Section 7 both rely on it.

## Notes

- Do not make this repository private. GitHub Pages stops serving the site, and
  re-enabling it afterwards requires reconfiguring the publishing source.
- Only commit files intended to be public. Everything here is served to anyone
  who knows the URL.
- Application source code lives in a separate private repository.

## Contact

ivashchukvladyslav@gmail.com
