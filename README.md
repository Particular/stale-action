# stale-action

Manages Particular's usage of https://github.com/actions/stale

Because we distribute `stale.yml` workflows to all repos via [RepoStandards](https://github.com/Particular/RepoStandards), we need to reference an action with an unchanging version `@main`. Otherwise Dependabot would raise PRs in each repo that GitHubSync would try to reverse.

## Usage

```yaml
      - name: Set stale PRs
        uses: Particular/stale-action@main
        with:
          repo-token: ${{ secrets.GITHUB_TOKEN }}
```

## License

The scripts and documentation in this project are released under the [MIT License](/LICENSE.md).