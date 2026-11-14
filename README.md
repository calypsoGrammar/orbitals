# <a href='https://crhisgbibon.github.io/orbitals/' target='_blank'>Orbitals</a>

<p></p>

## Deployment

The site is published to GitHub Pages at <https://calypsogrammar.github.io/orbitals/> by hand: Actions → **deploy** → Run workflow, with **Dry run** unticked (a dry run builds and checks without publishing). `.github/workflows/deploy.yml` uses the shared Pages deploy in `calypsoGrammar/deploy-workflows`: it builds `dist/` with `npm ci` and `npm run build` from a commit on `main` whose CI `build` job passed, and publishes it. Merging to `main` does not publish. To roll back, run the same workflow with an earlier commit as `ref`, or tick **rollback** to publish the `stable` tag (maintained by `stable.yml`); a rollback holds later deploys until cleared (Actions → stable → Run workflow → `clear-hold`). The Pages source must be "GitHub Actions".
