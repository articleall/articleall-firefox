# Articleall

Articleall is a lightweight Manifest V3 Firefox extension that redirects
supported multi-page articles to their full-page view. Redirects happen only
for top-level web navigation, preserve unrelated query parameters and URL
fragments, and stop automatically when the target parameter or path is already
present.

## Install manually

1. Download or clone this repository.
2. Open `about:debugging#/runtime/this-firefox` in Firefox.
3. Click **Load Temporary Add-on**.
4. Select `manifest.json` from this repository.

For a persistent installation, package and sign the extension through the
Firefox Add-ons Developer Hub.

The extension is enabled by default. Click the Articleall toolbar icon to pause
or resume automatic redirects. The setting is stored with Firefox Sync storage.

## Supported sites

| Site | Full-page rule |
| --- | --- |
| `kompas.com` and subdomains | `?page=all` |
| `suara.com` | `?page=all` |
| `tribunnews.com` | `?page=all` |
| `grid.id` | `?page=all` |
| `viva.co.id` | `?page=all` |
| `intipseleb.com` | `?page=all` |
| `parapuan.co` | `?page=all` |
| `sonora.id` | `?page=all` |
| `herstory.co.id` | `?page=all` |
| `motorplus-online.com` | `?page=all` |
| `kompasiana.com` | `?page=all` |
| `jawapos.com` | `/?page=all` |
| `idntimes.com` | `?page=all` |
| `popmama.com` | `?page=all` |
| `kosadata.com` | `?page=all` |
| `fajar.co.id` | `?page=all` |
| `sindonews.com` | `?showpage=all` |
| `poskota.co.id` | `?view=all` |
| `beritasatu.com` | `/?view=all` |
| `detik.com` | `?single=1` |
| `insidermonkey.com` | `?singlepage=1` |
| `inews.id` | path suffix `/all` |
| `wahananews.co` | path suffix `/0` |

## Development

The URL engine is a pure JavaScript module with focused tests:

```sh
npm test
```

No build step or external runtime dependency is required.
