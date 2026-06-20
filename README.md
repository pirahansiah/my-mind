# My Mind

![Screenshot](screenshot.png)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.txt)
[![GitHub stars](https://img.shields.io/github/stars/pirahansiah/my-mind.svg)](https://github.com/pirahansiah/my-mind/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/pirahansiah/my-mind.svg)](https://github.com/pirahansiah/my-mind/network)

A free, open-source web application for creating and managing mind maps. Distributed under the MIT license.

New to Mind maps? They are useful, aesthetic and cool! Read more about these special diagrams in [the Wikipedia article](http://en.wikipedia.org/wiki/Mind_map).

## Links

- [Official web page](http://my-mind.github.io/)
- [Sample mind map](http://my-mind.github.io/?map=examples/features.mymind) showcasing many features
- [News / Changelog](https://github.com/ondras/my-mind/wiki/News)
- [Documentation](https://github.com/ondras/my-mind/wiki)
- [YouTube tutorials](https://www.youtube.com/tiziran)

## Features

- Create, edit, and organize mind maps in a browser
- Multiple layout modes: graph, map, tree
- Multiple shape styles: box, ellipse, underline
- Multiple backends: Local storage, File, Firebase, Google Drive, WebDAV, Image export
- Import/Export: JSON, FreeMind (.mm), Markdown (.mma), plaintext
- Keyboard-driven workflow with customizable shortcuts
- Real-time collaborative editing via Firebase backend
- Export mind maps as images

## Installation

> There is also an online version at [my-mind.github.io](http://my-mind.github.io/)

1. Clone the repository:
   ```bash
   git clone https://github.com/pirahansiah/my-mind.git
   ```
2. Open `index.html` in your web browser
3. Done! See the [documentation](https://github.com/ondras/my-mind/wiki) for usage details.

### Local Development

The project uses a build system to combine source files:

```bash
make
```

Source files in `src/` are compiled into `my-mind.js`.

### Firefox Screenshot Tip

For personal use, you can take screenshots of individual mind map items using Firefox DevTools:
1. Press `F12` to open DevTools
2. Go to Console
3. Run: `:screenshot --selector .item`

## Architecture

```
my-mind/
├── src/                 # Source modules (compiled to my-mind.js)
│   ├── app.js           # Main application logic
│   ├── map.js           # Mind map data model
│   ├── item.js          # Individual node handling
│   ├── layout.*.js      # Layout engines (graph, map, tree)
│   ├── shape.*.js       # Node shape renderers
│   ├── backend.*.js     # Storage backends
│   ├── command.*.js     # User commands
│   └── ui.*.js          # UI components
├── css/                 # Stylesheets
├── vendor/              # Third-party libraries (pell editor)
├── bin/                 # Build tools
├── examples/            # Sample mind maps
└── my-mind.js           # Compiled application
```

## Technologies

- **Frontend:** Vanilla JavaScript (ES5 compatible), HTML5, CSS3
- **Storage:** LocalStorage, Firebase Realtime Database, Google Drive API, WebDAV
- **Build:** Custom Makefile-based compilation
- **Editor:** [Pell](https://github.com/jaredreich/pell) for rich text editing

## Contributing

Found a bug? [Open an issue.](https://github.com/pirahansiah/my-mind/issues)
Have an improvement? [Submit a pull request.](https://github.com/pirahansiah/my-mind/pulls)
Not sure how to do stuff? [Check the docs.](https://github.com/ondras/my-mind/wiki)

## License

[MIT](LICENSE.txt)
