# Image Background Remover in the browser 

A powerful React + Vite application that removes backgrounds from images directly in your browser. This app leverages machine learning models through Transformers.js to process media locally, ensuring your files never leave your device.

## Features

- 🎯 One-click background removal for images
- 🎨 Custom background color and image selection
- 💾 Download options for both transparent and colored backgrounds
- 🏃‍♂️ Local processing - no server uploads needed
- 🔒 Privacy-focused - all processing happens in your browser
- ⚡ Optional WebGPU acceleration for supported browsers

## Technical Implementation

The app implements a cross-browser approach to background removal with optional WebGPU acceleration:

### Default Implementation (All Browsers)
- Ensures consistent performance across all modern browsers
- Processes images efficiently using WebAssembly

Both implementations use Transformers.js to run the machine learning models directly in the browser, eliminating the need for server-side processing.

## How It Works

1. **File Selection**: Upload any image file
2. **Model Selection**: 
   - By default, uses RMBG-1.4 for maximum compatibility
   - If WebGPU is available, offers option to switch to MODNet
3. **Background Removal**: The selected ML model processes your media, creating an alpha mask
4. **Customization**: Choose a custom background color, image or keep transparency
5. **Export**: Download your processed media with either transparent or colored background

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/Louay0007/Ai-BG-Remover-V1.git
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

## Browser Support

- **Default Experience**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **Optional WebGPU**: Available in browsers with WebGPU support (Chrome Canary with WebGPU flags enabled)

## Technical Stack

- React + Vite for the frontend framework
- Transformers.js for ML model inference
- RMBG-1.4 as the default cross-browser model
- Optional WebGPU acceleration with MODNet
- IndexedDB (via Dexie.js) for local file management
- TailwindCSS for styling

## Credits

Made By Louay Rjili.

## License

MIT License 
