# generate-registry-deep

Run `aqua gr --deep` by GitHub Actions

`--deep` option may cause GitHub API rate limiting, so we created this repository only for running `aqua gr --deep`.

https://docs.github.com/en/rest/overview/resources-in-the-rest-api?apiVersion=2022-11-28

> When using `GITHUB_TOKEN`, the rate limit is 1,000 requests per hour per repository.

`GITHUB_TOKEN`'s rate limit is set per repository, so even if the rate limit occurs in this repository, it doesn't affect other repositories and users.

## How to use

[Run the GitHub Actions Workflow](https://github.com/aquaproj/generate-registry-deep/actions/workflows/generate.yaml).

e.g.

```console
$ gh workflow run generate.yaml -f package=suzuki-shunsuke/tfcmt [-r <branch>]
```

Then the result would be outputted to GITHUB_STEP_SUMMARY.
Please see the summary.

e.g.

https://github.com/aquaproj/generate-registry-deep/actions/runs/4260470293

![image](https://user-images.githubusercontent.com/13323303/221124854-3e9f25cb-34fa-4f9b-acee-8386d1a6334a.png)

### :rocket: Fork this repository

If you want to run the workflow, please [fork this repository](https://github.com/aquaproj/generate-registry-deep/fork) and run the workflow!
No GitHub Secrets or something are needed. You only have to fork this repository.

## Reference

- [aquaproj/aqua#1662](https://github.com/aquaproj/aqua/pull/1662)

## LICENSE

[MIT](LICENSE)
