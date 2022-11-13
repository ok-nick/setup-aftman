<div align="center">
  <h1><code>setup-aftman</code></h1>
  <p>
    <a href="https://github.com/ok-nick/setup-aftman/actions?query=workflow%3ACI"><img src="https://github.com/ok-nick/setup-aftman/workflows/CI/badge.svg" alt="CI" /></a>
    <a href="https://discord.gg/w9Bc6xH7uC"><img src="https://img.shields.io/discord/834969350061424660?label=discord" alt="discord" /></a>
  </p>
</div>

GitHub action to install and run [aftman](https://github.com/LPGhatguy/aftman); a toolchain manager.

## Usage
```yaml
steps:
- uses: ok-nick/setup-aftman@v0.3.0
```

### Parameters
|name|description|default|
|---|---|---|
|`version`|`aftman` version in the form `vx.x.x`|-|
|`path`|Path to the `aftman.toml` directory|`.`|
|`token`|Github token from `github.token`|`github.token`|

## Credits
[@nezuo](https://github.com/nezuo) - Installing `aftman` using `gh`
