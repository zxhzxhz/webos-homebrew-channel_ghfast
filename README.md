# webos-homebrew-channel_ghfast

Accelerated mirror of the [webOS Homebrew Channel](https://github.com/webosbrew/webos-homebrew-channel) app catalog, proxied through [ghfast.top](https://ghfast.top) for faster downloads in regions with slow GitHub connectivity.

## Usage

Replace the default Homebrew Channel repository URL with one of the following:

- **Direct**: `https://raw.githubusercontent.com/zxhzxhz/webos-homebrew-channel_ghfast/master/apps.json`
- **Accelerated**: `https://ghfast.top/https://raw.githubusercontent.com/zxhzxhz/webos-homebrew-channel_ghfast/master/apps.json`

## How it works

- Fetches `https://repo.webosbrew.org/api/apps.json` every hour via GitHub Actions
- Rewrites all `github.com` and `raw.githubusercontent.com` URLs with `https://ghfast.top/` prefix
- Non-GitHub URLs (e.g. `repo.webosbrew.org`, `mirrors.kodi.tv`) are left untouched
- Commits and pushes the transformed `apps.json` automatically

## Manual trigger

Trigger the sync workflow manually from the [Actions tab](https://github.com/zxhzxhz/webos-homebrew-channel_ghfast/actions/workflows/sync.yml).
