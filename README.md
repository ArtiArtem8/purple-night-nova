# Purple Night Nova

An independent fork of [Purple Night](https://github.com/Br3uxi/Purple-Night-Theme) for Firefox 157+ / Nova. Not an official update from the original authors.

## Install / Development

Node 22+ and Firefox are needed for development.

```sh
npm install
npm run dev
npm run lint
npm run build
```

`npm run dev` loads the theme into a temporary Firefox profile. To choose a Firefox binary, use `npm run dev -- --firefox "path/to/firefox"`. Builds go into `web-ext-artifacts/`. The ZIP is unsigned; permanent installation in release Firefox needs [Mozilla signing](https://extensionworkshop.com/documentation/publish/signing-and-distribution-overview/).

## Why this fork

Kept the stars. Reworked the popup, sidebar, tabs and URL field around quieter purple surfaces. Purple marks focus and selection; pink marks loading and attention.

Upstream has two commits, both from August 2020. Its `images/0.png` was actually a four-frame GIF. It's now an APNG with the same pixels, 150 ms per frame and infinite looping, since Firefox themes support APNG animation rather than animated GIF. The opaque image already has its own purple background, so a gradient underneath would be hidden.

Stars stay in the top toolbars. The toolbar has a dark translucent surface; the sidebar stays plain. Manifest v2 still fits a static theme. Firefox 156 is the minimum because that's when `backgrounds_area` arrived; visual testing targets 157+.

[Mozilla's Nova notes](https://blog.mozilla.org/addons/2026/09/29/nova-is-here-what-changes-for-your-firefox-theme/) take precedence where the [MDN theme reference](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/theme) still describes older UI:

- The overall accent follows the OS; some focus rings and links remain blue/cyan. There is no separate popup icon color yet.
- `popup_text` no longer colors URL suggestions; `ntp_text` no longer colors the new-tab search box.
- Sidebar highlight colors currently have no visible effect in Nova. They're set for UI that still uses them. Sidebar icons follow its text color.
- `sidebar_border` and `toolbar_bottom_separator` now separate the page from browser surfaces. Firefox 157 also has a sidebar expand-on-hover background bug; Mozilla lists a fix for 158.

Static checks don't establish how Firefox renders the theme. Run the short [manual checklist](MANUAL-TEST.md) before release.

## Credits

Purple Night by [Br3uxi / Breuxi](https://github.com/Br3uxi/Purple-Night-Theme), also on [Firefox Add-ons](https://addons.mozilla.org/de/firefox/addon/purple-night-theme/).
Based on [Purple Twinkle](https://addons.mozilla.org/de/firefox/addon/purple-twinkle/) by [Chu](https://addons.mozilla.org/de/firefox/user/12464975/).
Upstream also thanks Mytra, Nitrogen and YukaChanx3 for help choosing colors.

This derivative keeps the original star artwork and changes the image encoding, theme colors, compatibility metadata and tooling. Licensed under [CC BY-NC-SA 3.0 Unported](https://creativecommons.org/licenses/by-nc-sa/3.0/); the original [LICENSE.md](LICENSE.md) is unchanged.
