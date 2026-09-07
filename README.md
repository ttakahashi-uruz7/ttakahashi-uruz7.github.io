# Novel Studio public information site

This repository contains the public, static GitHub Pages site used for Novel Studio's
application information, privacy policy, and terms of service.

The site has no JavaScript, external libraries, CDN assets, cookies, analytics, advertising, or
tracking. It must contain public information only. Do not add OAuth client secrets, refresh or
access tokens, service-account files, Drive file IDs, API keys, `.env` files, credential files,
local absolute paths, or private contact details.

## Pages

- Home: <https://ttakahashi-uruz7.github.io/>
- Privacy policy: <https://ttakahashi-uruz7.github.io/privacy.html>
- Terms of service: <https://ttakahashi-uruz7.github.io/terms.html>

## Search Console verification

Search Console ownership verification is intentionally not pre-populated with a made-up token.
After adding the site as a URL-prefix property, prefer the HTML file method when Google provides
one:

1. Add the URL-prefix property `https://ttakahashi-uruz7.github.io/` in Google Search Console.
2. Choose HTML file verification and download the exact file supplied by Google.
3. Add that exact `googleXXXXXXXXXXXX.html` file to this repository root without changing its
   filename or contents.
4. Commit and push the file, then confirm that the public URL
   `https://ttakahashi-uruz7.github.io/googleXXXXXXXXXXXX.html` is reachable.
5. Return to Search Console and complete verification.

The alternative is the HTML tag method: add Google's exact
`<meta name="google-site-verification" content="...">` tag to `index.html`, push it, and then
complete verification in Search Console. The token must come from Google; it must never be
invented here.

## Google Auth Platform notes

Search Console URL-prefix ownership and Google Auth Platform's Authorized domain requirement are
separate checks. The candidate authorized domain is `ttakahashi-uruz7.github.io`, not the public
suffix `github.io`, and it should only be entered if Google Auth Platform accepts it after the
account owner has completed the relevant Search Console ownership verification. This repository
does not claim that GitHub Pages automatically satisfies Google's verified-domain requirement.

Google's current guidance also says that personal-use apps with fewer than 100 users can be
exempt from OAuth verification, while Testing status still imposes its own test-user and
seven-day authorization limits. Moving a project to In production and removing the seven-day
limit is a separate Google Auth Platform action and is not performed by this repository.

## Local validation

From the repository root, check that the three HTML pages exist and contain no credentials before
committing. A simple static-server check is sufficient; no build step or deployment pipeline is
required.
