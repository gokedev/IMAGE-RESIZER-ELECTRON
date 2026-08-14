# Image Resizer

A cross-platform desktop application built with Electron for resizing images quickly and easily.

## Features

- **Simple UI** - Drag and drop or select an image file
- **Auto-dimensions** - Automatically detects and fills in the original image width/height
- **Custom sizing** - Set custom width and height for resizing
- **Multiple formats** - Supports JPEG, PNG, and GIF images
- **Toast notifications** - Success and error notifications
- **Auto-save** - Resized images saved to `~/imageresizer` folder
- **Cross-platform** - Works on Windows, macOS, and Linux
- **About window** - Accessible from the menu bar

## Tech Stack

- **Electron** - Desktop app framework
- **resize-img** - Image resizing library
- **toastify-js** - Toast notifications
- **Vanilla HTML/CSS/JS** - No frontend framework

## Installation

```bash
# Clone the repository
git clone <repository-url>
cd image-resizer-electron

# Install dependencies
npm install

# Run the app
npm start
```

## Development

```bash
# Run in development mode (opens DevTools)
npm start
```

The app runs in development mode by default (window width: 1000px). For production, set `NODE_ENV=production`.

## Usage

1. Launch the app
2. Click "Select an image to resize" or drag an image onto the drop zone
3. The original dimensions will auto-fill in the width/height fields
4. Modify the dimensions as needed
5. Click "Resize"
6. The resized image will be saved to `~/imageresizer` and the folder will open automatically

## Project Structure

```
image-resizer-electron/
├── main.js                 # Main Electron process
├── preload.js              # Preload script (secure IPC bridge)
├── package.json
├── assets/
│   ├── icons/              # App icons (Windows, macOS, Linux)
│   └── screen.png          # Screenshot
├── renderer/
    ├── index.html          # Main window HTML
    ├── about.html          # About window HTML
    ├── css/
    │   └── style.css       # Styles
    ├── js/
    │   └── renderer.js     # Renderer process logic
    └── images/
        └── logo.svg        # App logo
```

## Building for Distribution

To create distributable packages, you'll need to add a build tool like `electron-builder` or `electron-forge` to `package.json`.

Example with electron-builder:

```bash
npm install --save-dev electron-builder
```

Then add build config to `package.json` and run:

```bash
npx electron-builder
```

## License

MIT License - see [package.json](package.json) for details.

## Author

gokedev