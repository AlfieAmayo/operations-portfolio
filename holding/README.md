# Temporary holding page

This folder is what GitHub Pages publishes while the portfolio is being updated.
The Hugo source (content, layouts, themes, static) is untouched.

Restore the full site:

    cp .github/disabled/deploy-hugo.original.yml .github/workflows/.github/workflows/deploy.yml
    git rm -r holding .github/disabled   # optional clean-up

Then commit and push to main. (`git revert` of the holding-page commit does the same.)
