<div align="center">
  <h1><code>setup-aftman</code></h1>
  <p>
    <a href="https://github.com/ok-nick/setup-aftman/actions?query=workflow%3ACI"><img src="https://github.com/ok-nick/setup-aftman/workflows/CI/badge.svg" alt="CI" /></a>
    <a href="https://discord.gg/w9Bc6xH7uC"><img src="https://img.shields.io/discord/834969350061424660?label=discord" alt="discord" /></a>
  </p>
</div>

GitHub action to install and run [aftman](https://github.com/LPGhatguy/aftman); a toolchain manager.

## Usage
Use the latest released version of `aftman` with default parameters:
```yaml
steps:
- uses: ok-nick/setup-aftman@v0.4.2
```
For a list of default parameter values, [check here](https://github.com/ok-nick/setup-aftman/blob/main/action.yml#L5-L20).

### Advanced
For more advanced cases, use the parameters below.
```yaml
steps:
- uses: ok-nick/setup-aftman@v0.4.2
  with:
    version: v1.0.0 # name of git tag in aftman (uses latest tag by default)
    path: some_dir/my_project # path to project dir containing `aftman.toml` ("." (current dir) by default)
    cache: false # whether to enable binary caching between runs (false by default)
    token: ${{ github.token }} # GitHub token to bypass rate limit (${{ github.token }} set by default)
```

## Inputs
### `version`
The git tag of `aftman` to install from releases and use. By default this input will be assigned to the latest version of `aftman`.

### `path`
The path to the directory containing the `aftman.toml` to install tools from. The default is the current directory (`.`).

### `cache`
Enable to cache tools installed by `aftman`, the default value of this input is `false`. Note, in many cases enabling this feature will slow down the `setup-aftman` action.

There are a few reasons you may choose to enable caching:
* Action runs often, causing the GitHub rate-limit to be reached
* A large amount of tools to install
* Server downloading from is slow

In any case, it is recommended to benchmark before enabling this feature.

### `token`
Set to a GitHub token to be used by `aftman` to increase the GitHub rate-limit. Note, these two options, `${{ github.token }}` and `${{ secrets.GITHUB_TOKEN }}`, are equivalent and passed by default. **Thus, you do not need to specify this parameter unless you are using a token different from the owner of the repository.**

## Credits
[@nezuo](https://github.com/nezuo) - Installing `aftman` using `gh`

