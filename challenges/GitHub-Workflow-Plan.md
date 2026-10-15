# GitHub Pages deployment plan

## Scope

Implement GitHub Pages deployment for a static website.

The deployment must publish the repository root without adding a build system.

## Preconditions

1. Complete and locally check the website. GATE HERE. The User must confirm they can see it locally first.
2. Confirm that the repository's default deployment branch is `main`.
3. In the repository settings, set **Pages > Build and deployment > Source** to
   **GitHub Actions**.
4. Confirm that the repository permits GitHub Actions to deploy Pages.

## Files to add or update

- Add `.github/workflows/deploy-pages.yml`.
- Optional - Update `ARCHITECTURE.md` with the deployment workflow and release checks ONLY if this file already exists.

Do not add a package manager, static-site generator, server, or deployment
secret.

## Workflow design

Create one workflow with these properties:

- Run on pushes to `main`.
- Support manual runs with `workflow_dispatch`.
- Cancel an older in-progress Pages deployment when a newer run starts.
- Grant `contents: read`, `pages: write`, and `id-token: write` permissions.
- Check out the repository.
- Configure GitHub Pages with `actions/configure-pages@v5`.
- Upload the repository root with `actions/upload-pages-artifact@v4`.
- Deploy the artifact with `actions/deploy-pages@v4`.
- Use the `github-pages` environment.
- Expose the deployed URL through the deployment step's `page_url` output.

Use the current official GitHub Pages action versions when implementing the
workflow. Verify the action versions against the GitHub Pages documentation
before editing the workflow.

## Local release checks

Before merging the workflow:

1. Open `index.html` in a browser or a local static server.
2. Test the layout at a narrow mobile viewport and a desktop viewport.
3. Navigate with a keyboard.
4. Confirm that the visuals are approved by the user FIRST
5. Merge

## Deployment checks

After merging the workflow to `main`:

1. Confirm that the workflow starts from the push event.
2. Confirm that the upload and deployment jobs complete successfully.
3. Open the URL reported by the `github-pages` environment.
4. Repeat the responsive and keyboard checks against the deployed page.
5. Confirm that the deployed page matches the tested local page.

## Acceptance criteria

- A push to `main` deploys the repository root to GitHub Pages.
- A manual workflow run is available.
- The workflow reports the deployed URL.
- A failed deployment does not replace the last successful deployment.
- The deployed page contains the same HTML, CSS, and JavaScript behavior as the
  tested local page.

## References

- [Using custom workflows with GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)
- [Configuring a publishing source for GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
