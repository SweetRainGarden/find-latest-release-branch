# find-latest-release-branch

Outputs the latest `release/x.y.z` branch and a bumped `devCode` (minor +1).

## Inputs

| Name          | Required | Default | Description                                                                                  |
| ------------- | -------- | ------- | -------------------------------------------------------------------------------------------- |
| `path`        | No       | `.`     | Path to the git repo directory.                                                              |
| `showSummary` | No       | `false` | Show diagnostics in the GitHub job summary log. Set to `'true'` to show; defaults to hidden. |

## Outputs

| Name                  | Description                                    |
| --------------------- | ---------------------------------------------- |
| `latestReleaseBranch` | The latest `release/x.y.z` branch.             |
| `devCode`             | The next dev version with bumped minor (`x.(y+1).0`). |

## Usage

```yaml
- name: Find latest release and dev version
  id: find_latest_release_branch
  uses: SweetRainGarden/find-latest-release-branch@develop
  with:
    showSummary: "true" # optional; defaults to hidden
```