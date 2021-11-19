# docstr-cov-workflow

Measure docstring coverage of Python packages with GitHub Actions


### Usage

1. Copy `.github/workflows/docstr-cov.yml` and  `.docstr.yaml` to your repository.
2. Tweak the configuration file following the [package documentation](https://github.com/HunterMcGushion/docstr_coverage#config-file).
3. Login to https://jsonbin.org and store the API key as a repository secret named `JSONBIN_APIKEY`.
4. The workflow will fail if the coverage is lower than the score of the base branch (on `pull_request`) or the previous commit (on `push`), and files that made the job fail will be blamed.
5. Pushing to `main` branch updates the current coverage of the project by updating a nice badge.
6. You can change the color range of the badge by tweaking the `RANGE` variable at the top of the workflow. For example, `50..75` means that coverage below `50` will display a red badge, and above `75` a green one.
7. Remember to add the badge to your README.md


### Example

![docstr-cov](https://img.shields.io/endpoint?url=https://jsonbin.org/epassaro/docstr-cov-workflow/badges/docstr-cov)

Make changes to `example/base.py` and see the workflow in action.


### Acknowledgements

- [Hunter McGushion](https://github.com/HunterMcGushion), and the contributors of the package [`docstr-coverage`](https://github.com/HunterMcGushion/docstr_coverage).
- [Remy Sharp](https://github.com/remy), creator of [jsonbin.org](https://jsonbin.org).
- [TARDIS-SN](https://github.com/tardis-sn) collaboration, for letting me have fun with these tools.
