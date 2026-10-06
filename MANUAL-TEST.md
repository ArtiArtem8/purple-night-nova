# Manual check — Firefox 157+

Use `npm run dev` with your current Firefox binary. Note Firefox version, OS and anything that looks off. These boxes are intentionally unchecked; the UI has not been verified yet.

- [ ] Horizontal tabs: selected, inactive, hovered and loading. Selection stays clear without a shadow; stars twinkle without hiding labels/icons.
- [ ] URL bar: normal, focused, selected text and autocomplete. Check normal and keyboard-selected suggestion text.
- [ ] Popups: Extensions, bookmarks, downloads and hamburger menu. Check mouse hover and keyboard navigation.
- [ ] Toolbar and tab-strip buttons: hover, pressed/open, and attention icons (saved bookmark or completed download).
- [ ] Sidebar: closed, open, expanded on hover, and Customize sidebar. Check its page separator and icons. Try vertical tabs too.
- [ ] Private window and inactive browser window.
- [ ] New tab and settings/about pages: check chrome, cards, text and the search box where Firefox allows theme colors.
- [ ] Maximized and non-maximized windows, including a narrow window. Check star tiling and toolbar/sidebar edges.
- [ ] Light/dark OS settings and another OS accent. Try compact density if you use it.

Across these checks: no old acid-magenta `#6C0072`, no red-looking popup, readable main/secondary text, obvious focus/selection, and a quiet sidebar that fits the header. Report default blue where it seems controllable; some rings, links and OS-accent controls still belong to Firefox. Nova also ignores sidebar highlight colors. Firefox 157's expand-on-hover background bug is listed as fixed in 158.
