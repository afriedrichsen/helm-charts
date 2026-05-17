# Release Workflow

1. Commit changes to charts in branch/PR to `main`
2. Run command to package new version of charts that were added/modified

```
helm package charts/<CHART NAME> -d library --version <NEXT_CHART_VERSION_REQUIRED> --app-version <NEXT_APP_VERSION_OPTIONAL>
```

3. Confirm uncommitted `library` directory exists and that it is populated with ` *.tgz` packages for each packaged chart
4. Check out branch `gh-pages`
5. Run command `helm repo index . --url https://afriedrichsen.github.io/helm-charts/` and confirm `index.yaml` is now modified.
6. Submit the changes to the `library` directory and `index.yaml` in a PR to branch `gh-pages`. Use conventional commit syntax in any commits (Examples exist on `main` but feel free to improve upon it).
