# Publishing Toplane Guide

## One-time Netlify setup

1. Open the Netlify dashboard for the existing site `lolgameguide.netlify.app`.
2. Under **Identity**, enable Netlify Identity.
3. Under **Identity → Services → Git Gateway**, enable Git Gateway.
4. Under **Identity → Registration**, choose **Invite only** and invite the email address you will use to administer the CMS.
5. Accept the invite and set a password from the email Netlify sends. Do not share the invite or password.
6. Confirm the site deploys from the GitHub repository `Unskilledfrog/Toplaneguide` and the `main` branch. The included `netlify.toml` publishes the repository root as a static site.

## Publish these code changes

1. Open the pull request: https://github.com/Unskilledfrog/Toplaneguide/pull/3
2. Review and merge it into `main` when GitHub says it can be merged.
3. Wait for Netlify's production deploy to finish successfully.
4. Open https://lolgameguide.netlify.app/admin/ and sign in with the invited Identity account.
5. Edit a champion or a matchup and save. Git Gateway commits CMS changes to `main`; Netlify should deploy those commits automatically.

## Editing content

- **Champions and champion guides**: roster, class, traits, early/mid/late game advice, runes, starting item, core items and summoner spells.
- **Champion matchups**: manual rating overrides and matchup-specific explanations, plans, runes and items. If a matchup has no override, the site continues to use its automatic/default rating.
- **Site settings**: homepage title, description, navigation links and images.

If the CMS says it cannot authenticate, the Netlify Identity and Git Gateway setup above is not complete. If saving succeeds but the live site does not change, check the latest production deploy in Netlify.
