<p align="center">
  <img src="assets/moodboardy.png" alt="Moodboardy — a colorful scrapbook of ideas" width="180" height="180">
</p>

<h1 align="center">Moodboardy</h1>

<p align="center">
  <strong>A little space for big ideas.</strong><br>
  A whole canvas of possibilities.<br>
  Collect images, stray thoughts and things worth keeping — and make them yours.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Free-to_use-F8DF94?style=flat-square&amp;labelColor=254E3B" alt="Free to use">
  <img src="https://img.shields.io/badge/Source-available-C9D9BB?style=flat-square&amp;labelColor=254E3B" alt="Source available">
  <img src="https://img.shields.io/badge/No-sign_up-FFD2B9?style=flat-square&amp;labelColor=254E3B" alt="No sign-up">
  <img src="https://img.shields.io/badge/Saved-in_your_browser-C5D8F4?style=flat-square&amp;labelColor=254E3B" alt="Saved in your browser">
  <img src="https://img.shields.io/badge/GitHub_Pages-ready-F2C9C8?style=flat-square&amp;labelColor=254E3B" alt="GitHub Pages ready">
</p>

<p align="center">
  <a href="https://cioni03.github.io/Moodboardy/">
    <img src="https://img.shields.io/badge/Open_Moodboardy_%E2%86%92-254E3B?style=for-the-badge" alt="Open Moodboardy online">
  </a>
</p>

<p align="center"><sub>No sign-up. No noise. Just your ideas.</sub></p>

---

## ✨ Your ideas, all in one happy place

Build a moodboard for your next room makeover, brand identity, dream trip or very specific new obsession. Think cream paper, peach sticky notes, forest-green ink and little pops of coral, butter yellow and blue.

No feed to scroll. No account to create. Just an open space to play.

## 📌 The good stuff

| Feature | Make it yours |
| --- | --- |
| 🖼️ **Collect your inspiration** | Upload, drop or paste images onto your canvas. Add captions and keep your references together. |
| 📝 **Catch every thought** | Add colorful sticky notes and free text, from tiny reminders to big ideas. |
| 🌼 **Add a little personality** | Sprinkle in emoji and shapes. Give your board its own mood. |
| 🔗 **Keep your links close** | Paste URLs as simple link cards, ready to revisit. |
| ↗️ **Connect the dots** | Use lines and attached arrows to show how your ideas fit together. |
| 🪄 **Arrange it your way** | Move, resize, multi-select and group items. Undo and redo while you experiment. |
| 🌍 **Room to wander** | Explore an infinite canvas with pan and zoom. No page edges, no fixed layout. |
| 🗂️ **One tab per obsession** | Create multiple canvases, rename them and drag their tabs into your favorite order. Each remembers its own view. |
| 💾 **Pick up where you left off** | Your canvases save automatically in the same browser, on the same site. |
| 🎒 **Take your boards with you** | Export a canvas as JSON and import it elsewhere, without replacing your other canvases. |

## 🌱 From blank canvas to new favorite thing

1. **Drop something you love.** An image, a link, a few words. Start anywhere.
2. **Build the vibe.** Add notes, colors, emoji and connections. Move things until it feels right.
3. **Make room for more.** Open another canvas for your next idea. Export your favorites as backups.

**Little shortcuts, big flow:** paste with **⌘/Ctrl + V**, drag the background to explore, and use **Ctrl + scroll** to zoom. Press **?** for the full shortcut guide.

### A few handy canvas tricks

- Click **+** to start a new canvas, and click a tab to switch.
- Double-click a tab name, or use **✎**, to rename it.
- Drag tabs to reorder them. Press **Escape** to cancel, or use **Alt + ← / →** with a tab name focused.
- Open **⋯ → Export JSON** to download the current canvas, including uploaded images and its saved view.
- Choose **⋯ → Import JSON**, or drop a JSON file onto the page, to open it in a new tab. Older Moodboard exports work too.
- Use **×** to remove a canvas after confirmation. Closing the last one gives you a fresh start.

## 🏡 Your browser is home

Your boards are stored in your browser's IndexedDB, not on a server. There are no accounts, cloud sync, sharing links or server-side backups.

- **Back up the boards you love.** Clearing site data or using private browsing can remove them. Export JSON regularly.
- **New browser, new space.** Boards do not automatically follow you to another browser, device or website address. Use export and import to move them.
- **Storage is larger, not unlimited.** IndexedDB can hold substantially more than localStorage, but its quota depends on the browser and available disk space. If a save warning appears, export your work and reduce large images. Wait for the saved indicator before closing the page; asynchronous writes cannot be guaranteed during shutdown. Avoid editing the same site in multiple windows at once.
- **Local uploads travel better.** Images added by URL stay remote and may disappear. Upload files to include the images in your JSON backup.
- **No runtime CDN dependencies.** Fonts, compiled Tailwind CSS and Alpine.js are included locally. Remote images still need a connection and contact their hosts. Link cards do not fetch metadata or previews. Reopening the hosted site offline is not guaranteed: there is no service worker.
- **Unreadable storage is protected.** If local data cannot be read, automatic saving is paused. Use **⋯ → Export recovery data** to download the untouched raw data, and **Export JSON** to back up the current canvas. Restore a valid backup only after keeping a copy of the recovery file; resetting site storage must be done explicitly in your browser.
- **Stale tabs pause saving.** Each save atomically checks the previous workspace inside an IndexedDB transaction. If another window has changed it, saving pauses rather than overwriting it. Export any canvases you changed, then reload to get the latest saved workspace. Avoid simultaneous editing: this is not a collaborative editor.

The interface follows your system's light/dark preference by default. Use the moon/sun button in the top-right pill to choose a theme; your manual choice is remembered in this browser. Dark mode uses neutral grays without recoloring your board's images or chosen colors.

## Development

The checked-in assets are ready for static hosting, including GitHub Pages. Node.js is only needed when developing:

```sh
npm ci
npm test
npm run build
```

Rebuild after changing utility classes or the Tailwind theme. `npm run build` compiles `assets/app.css` and copies the pinned Alpine.js distribution into `assets/vendor/`. Font files and their licenses are in `assets/fonts/`; third-party notices are in `assets/THIRD-PARTY.md`.
