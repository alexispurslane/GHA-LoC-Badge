# LoC-Badge ![Generated Button](https://raw.githubusercontent.com/alexispurslane/GHA-LoC-Badge/image-data/badge.svg)

Based on shadowmoose's GHA-LoC-Badge!

Use [cloc](https://github.com/AlDanial/cloc?tab=readme-ov-file#overview-) to
count the source code lines of the specified source code files (not including
blank lines or comments), as opposed to shadowmoose's, which counts all lines.

## To use:
In a Github Action, download your project and run this action:

```yaml
      - name: Make Code Badge
        uses: alexispurslane/GHA-LoC-Badge@2.0.0
        id: badge
        with:
          debug: true
          directory: ./
          badge: ./output/badge.svg
          patterns: '*.js'  # Patterns in the format of a '.gitignore' file, separated by pipes.
          ignore: 'node_modules'
```

Once the badge has been generated, use whatever tool you prefer to upload it somewhere.
I personally prefer to push the badges to another branch of the project, where they can be linked easily.

You can [see a full example file that does this here.](./.github/workflows/main.yml)

The output badge can be customized. [Check out the input options here.](./action.yml)
