# Framecap — Caption Studio

A browser-based video and subtitle editor for creating captioned videos without a backend or a complicated editing setup.

Framecap lets you load a local video or an `.srt` subtitle file, edit caption timing and text on a visual timeline, customize caption appearance, preview the result, and export subtitles or a captioned video.

## Features

- **Local video editing** — Load a video file from your device.
- **SRT subtitle support** — Import `.srt` captions, edit them, and export updated subtitles.
- **Caption editing** — Add, split, trim, merge, and delete captions; edit caption text and timing.
- **Timeline controls** — Select captions, seek through the video, zoom the timeline, and fit it to the available width.
- **Caption styling** — Customize fonts and text appearance, with global or per-caption styling options.
- **Preview tools** — Preview captions over video, use safe-zone guides, and open the preview in fullscreen.
- **Video export** — Render captions into the exported video where supported by the browser.
- **Solid-color canvas** — Create a caption overlay on a solid background when working from an SRT file without a video.
- **Responsive interface** — Use the editor on desktop and smaller screens. Performance depends on the device and browser.

## Getting started

Framecap is packaged as a standalone HTML file, so you do not need Node.js, npm, a build step, or a backend to open the supplied app.

### Option 1: Open it locally

1. Download or clone this repository.
2. Open the app HTML file in a modern browser, preferably **Google Chrome** or **Microsoft Edge**.
3. Choose **Upload video** to load a local video.
4. Choose **Upload SRT** to import an existing subtitle file.
5. Edit captions and styling, then preview the result.
6. Use **Export SRT** to download subtitles, or **Export video** to render a captioned video.

> **Tip:** Keep the editor tab open while a video export is running. Video export can take time and uses your device's processing resources.

### Option 2: Deploy as a static website

Framecap does not require a server-side application. You can host it on a static hosting provider such as GitHub Pages or Netlify.

1. Put the app HTML file in the repository.
2. For a simple static deployment, name the app file `index.html`.
3. Publish the repository or upload the folder to your static hosting provider.
4. Open the deployed URL in a supported browser.

No environment variables or backend configuration are required for the standalone app as provided.

## How to use

1. **Load media:** Upload a video, or import an SRT file. If you only have subtitles, choose the solid-color background option.
2. **Edit captions:** Select a caption on the timeline to change its text, timing, or individual style.
3. **Arrange timing:** Use the playhead and timeline tools to split, trim, merge, add, or remove captions.
4. **Style captions:** Adjust font and visual settings. Choose whether changes apply globally or to the selected caption.
5. **Check the preview:** Play the video and review caption placement. Enable safe zones to check placement for short-form platforms.
6. **Export:** Download the edited SRT file or render a video with captions.

## Keyboard shortcuts

| Shortcut | Action |
|---|---|
| `Space` | Play or pause |
| `←` / `→` | Seek by 0.1 seconds |
| `Shift` + `←` / `→` | Seek by 1 second |
| `S` | Split the selected caption at the playhead |
| `T` | Trim the selected caption to the playhead |
| `N` | Add a caption at the playhead |
| `Delete` | Delete the selected caption |
| `Ctrl` / `⌘` + `Z` | Undo |
| `Ctrl` / `⌘` + `Shift` + `Z` | Redo |
| `F` | Toggle fullscreen preview |
| `?` | Open keyboard shortcuts |
| `Esc` | Close the shortcuts panel or exit fullscreen |

Shortcuts may not trigger while focus is inside an input, text area, or select control.

## Privacy and data handling

Framecap is designed as a client-side tool. In the supplied standalone version, you select files from your device and work with them in the browser; no application backend or account system is required.

- Do not commit confidential or sensitive media to a public repository.
- Exported files are downloaded by your browser.
- If you fork or modify the app, review any added scripts, libraries, analytics, or network requests before making privacy claims about your version.

## Browser compatibility and limitations

- Use a current version of Chrome or Edge for the most reliable experience.
- Video formats and codecs depend on browser support and the source file.
- Export formats depend on the browser's available media encoding capabilities. MP4/H.264 export is not available in every browser; some environments may only support WebM.
- Video rendering is resource-intensive. Large, high-resolution, or long videos may take longer to export and may require substantial memory.
- Keep the tab open and visible during export when the app instructs you to do so.
- The supplied app is a bundled HTML file, not the original editable React source project. A conventional source-code development workflow is not included unless source files are added separately.

## Project structure

A simple standalone distribution can be organized like this:

```text
.
├── index.html       # Framecap app (standalone HTML)
├── README.md        # Project documentation
├── LICENSE          # Add the selected license before publishing
└── .gitignore       # Optional Git ignore rules
```

If your repository uses a different HTML filename, update the instructions above accordingly.

## Contributing

Contributions, bug reports, and suggestions are welcome.

1. Check existing issues before opening a duplicate.
2. For a bug report, include your browser and operating system, steps to reproduce the issue, and any relevant error message.
3. For a feature request, describe the problem the feature would solve and the expected behavior.
4. Keep changes focused, and test media import, caption editing, SRT export, and video export in the browsers you intend to support.

Because the current distribution is a bundled HTML file, source-level contributions are easier if the original source project is made available.

## License

**Add a `LICENSE` file before publishing this repository.** The provided HTML file does not, by itself, specify the license for the complete Framecap application.

MIT is a reasonable choice if you want others to use, modify, and redistribute the project with minimal restrictions. Before selecting a license, confirm that you have the right to license all code you own and review notices and license obligations for bundled third-party components, including React.

## Acknowledgements

Framecap includes bundled React runtime code. Preserve applicable third-party copyright and license notices when redistributing the application. Add other third-party acknowledgements here if you include additional libraries or assets.
