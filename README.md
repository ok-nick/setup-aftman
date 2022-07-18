<div align="center">
  <h1><code>setup-aftman</code></h1>
  <p>
    <a href="https://github.com/ok-nick/setup-aftman/actions?query=workflow%3ACI"><img src="https://github.com/ok-nick/setup-aftman/workflows/CI/badge.svg" alt="CI" /></a>
    <a href="https://discord.gg/w9Bc6xH7uC"><img src="https://img.shields.io/discord/834969350061424660?label=discord" alt="discord" /></a>
  </p>
</div>

Github action to install and run [aftman](https://github.com/LPGhatguy/aftman), a toolchain manager.

## Usage
```yaml
steps:
- uses: actions/setup-aftman@v1
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
```

### Parameters
|name|description|default|
|---|---|---|
|`version`|`aftman` version in the form `vx.x.x`|-|
|`no-trust-check`|Whether to check trusts|`false`|
|`trusts`|List of trusted tools separated by spaces|-|
|`path`|Path to the `aftman.toml` directory|-|
|`token`|Github token from `secrets.GITHUB_TOKEN`||

## Credits
[@nezuo](https://github.com/nezuo) - Installing `aftman` using `gh`
