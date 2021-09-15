# action-dotnet-publish
This action runs the `dotnet publish` command that creates publish assets inside the specified directory.

## Usage
By default, this action requires the build to be up to date for the given build-configuration. To that purpose, you can use EasyDesk/action-dotnet-build. Otherwise, you can force a new build with skip-build: false.

### Usage example
```yaml
    steps:
      - uses: EasyDesk/action-dotnet-publish@v1
        with:
          # (Optional) The path to the project that should be published.
          # If not specified, defaults to '.'.
          path: '<path>'

          # (Optional) Additional command line arguments to be passed to 'dotnet test'.
          # If not specified, defaults to 'packages'.
          output-dir: '<path-to-output-dir>'

          # (Optional) The build configuration.
          # If not specified, defaults to 'Release'.
          build-configuration: Release

          # (Optional) Whether to skip the build using the '--no-build' flag.
          # If not specified, defaults to true.
          skip-build: true
```
