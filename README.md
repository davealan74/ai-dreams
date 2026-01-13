# AI Dreams - Pollinations Live Feed Visualizer

A real-time visualization of AI image generation happening on the [Pollinations.ai](https://pollinations.ai) platform. Watch as creative prompts from around the world transform into stunning visuals, streaming live.

**Live Demo:** [aidreams.cru2.net](https://aidreams.cru2.net)

## Features

- **Real-time streaming** - Connects to Pollinations' SSE feed to display images as they're generated
- **Three viewing modes:**
  - **Strips** - Flowing horizontal ribbons of images (configurable 3-12 rows)
  - **Rainbow** - Images automatically sorted by their dominant color using adaptive hue boundaries
  - **Collage** - Organic, layered display with floating animations
- **Smart caching** - Images are cached locally to prevent re-fetching when switching modes
- **Responsive** - Works on desktop and mobile devices
- **No API keys required** - 100% client-side JavaScript using Pollinations' public feed

## How It Works

The application connects to `https://image.pollinations.ai/feed` via Server-Sent Events (SSE) to receive real-time notifications of newly generated images. Each image is analyzed for its dominant color (in Rainbow mode) and displayed according to the selected visualization mode.

### Rainbow Mode Color Analysis

Rainbow mode uses a sophisticated color analysis algorithm:
- Samples image pixels and converts to HSL color space
- Uses circular averaging for hue values to handle the 0°/360° wraparound
- Weights colors by saturation (more vivid colors have more influence)
- Adaptively adjusts hue boundaries based on incoming image distribution to ensure equal distribution across all 7 color strips

## Technology

- Pure HTML/CSS/JavaScript (no frameworks or build tools)
- Server-Sent Events for real-time data
- Canvas API for color analysis
- CSS animations for smooth transitions

## License

MIT License

## Author

**Dave Alan Caruana** / [Techmagic](https://techmagic.info)

Available for AI integration projects and creative tech solutions.

---

Powered by [Pollinations.ai](https://pollinations.ai) - Your Friendly Open-Source Gen-AI Platform
