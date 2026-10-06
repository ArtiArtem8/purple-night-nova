# Manual check — Firefox 157+

Use `npm run dev` with your current Firefox binary. Note Firefox version, OS and anything that looks off. These boxes are for your own check.

Checked in Firefox 157 on Windows: horizontal/vertical tabs, sidebar open/close, and URL field focus at 1440×900 and 880×720. Native popup capture was unavailable; popup colors were checked from computed styles. The remaining states below still need a manual pass.

- [ ] Horizontal tabs: selected, inactive, hovered and loading. Selection stays clear without a shadow; stars twinkle without hiding labels/icons.
- [ ] URL bar: normal, focused, selected text and autocomplete. Check normal and keyboard-selected suggestion text.
- [ ] Popups: Extensions, bookmarks, downloads and hamburger menu. Check mouse hover and keyboard navigation.
- [ ] Toolbar and tab-strip buttons: hover, pressed/open, and attention icons (saved bookmark or completed download).
- [ ] Sidebar: closed, open, expanded on hover, and Customize sidebar. Check stars behind the rail and vertical tabs, its page separator and icons. Separate bookmarks/history panels stay solid; Firefox does not keep alpha in `sidebar` colors.
- [ ] Private window and inactive browser window.
- [ ] New tab and settings/about pages: check chrome, cards, text and the search box where Firefox allows theme colors.
- [ ] Maximized and non-maximized windows, including a narrow window. Check star tiling and toolbar/sidebar edges.
- [ ] Light/dark OS settings and another OS accent. Try compact density if you use it.

Across these checks: no old acid-magenta `#6C0072`, no red-looking popup, readable main/secondary text, obvious focus/selection, and the same cool purple hue across the header, sidebar and popups. Check that stars stay behind text and icons. Report default blue where it seems controllable; some rings, links and OS-accent controls still belong to Firefox. Nova also ignores sidebar highlight colors. Firefox 157's expand-on-hover background bug is listed as fixed in 158.
