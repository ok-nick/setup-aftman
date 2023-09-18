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
- uses: ok-nick/setup-aftman@v0.4.0
```
For a list of default parameter values, [check here](https://github.com/ok-nick/setup-aftman/blob/main/action.yml#L5-L25).

### Advanced Usage
For more advanced cases, use the parameters below.
```yaml
steps:
- uses: ok-nick/setup-aftman@v0.4.0
  with:
    version: v1.0.0 # name of git tag in aftman (uses latest by default)
    path: some_dir/my_project # path to project dir containing `aftman.toml` (uses current dir by default)
    cache: true # whether to enable binary caching between runs (true by default)
    token: ${{ github.token }} # GitHub token to bypass rate limit (passed by default)
```

## Credits
[@nezuo](https://github.com/nezuo) - Installing `aftman` using `gh`
