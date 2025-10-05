# 📹 Video Downloader Frontend

A modern, beautiful web application for downloading videos from YouTube and Facebook with high-quality streaming, progress tracking, and multi-server fallback support.

## ✨ Features

- **Multi-Platform Support**: Download videos from YouTube and Facebook
- **Quality Selection**: Choose from 144p to 1080p or best available quality
- **Real-time Progress**: Live download progress with file size tracking
- **Multi-Server Fallback**: Automatic failover between multiple backend servers
- **Modern UI**: Beautiful gradient design with responsive layout
- **Fast Downloads**: Streaming download with progress indicators
- **Smart Naming**: Downloads use actual video titles as filenames

## 🚀 Live Demo

Visit the live application: [Video Downloader](https://vd-frontend-beige.vercel.app/)

## 🛠 Tech Stack

- **Frontend**: Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Modern CSS with gradients, backdrop filters, and animations
- **Backend APIs**: Railway & Render hosted download services
- **Deployment**: Vercel (static hosting)
## 🎯 How to Use

1. **Paste URL**: Enter a YouTube or Facebook video URL
2. **Select Quality**: Choose your preferred video quality (144p - 1080p)
3. **Download**: Click the download button and watch the progress
4. **Save**: Browser will automatically save the file with the video's title

### Supported URL Formats

**YouTube:**
- `https://www.youtube.com/watch?v=VIDEO_ID`
- `https://youtu.be/VIDEO_ID`
- `https://m.youtube.com/watch?v=VIDEO_ID`
- `https://music.youtube.com/watch?v=VIDEO_ID`

**Facebook:**
- `https://www.facebook.com/username/videos/VIDEO_ID`
- `https://fb.watch/VIDEO_ID`
- `https://www.facebook.com/watch/?v=VIDEO_ID`

## 🔧 Installation & Setup

### Prerequisites
- Node.js 16+ (for development)
- Modern web browser

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/almas-syed05/vd-frontend.git
   cd vd-frontend
   ```

2. **Open in browser**
   ```bash
   # Simply open index.html in your browser
   open index.html
   
   # Or serve with a local server
   npx serve .
   ```

3. **Development**
   - No build process required - pure HTML/CSS/JS
   - Edit `index.html` directly
   - Refresh browser to see changes

### Deployment

**Vercel (Recommended)**
```bash
npm install -g vercel
vercel --prod
```

**Netlify**
1. Connect your GitHub repository
2. Set build command: (none)
3. Set publish directory: `/`

**GitHub Pages**
1. Go to repository Settings → Pages
2. Select source: Deploy from branch
3. Choose branch: `main`

## ⚙️ Configuration

### Backend URLs
The app uses multiple backend servers for reliability:

```javascript
const BACKENDS = [
  'https://vd-backend-production.up.railway.app',
  'https://vd-backend-f1vo.onrender.com'
];
```

### API Authentication
```javascript
const API_KEY = 'testing123'; // Configure in backend
```

## 🏗 Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend API    │    │   Video Source  │
│   (Vercel)      │───▶│   (Railway)      │───▶│   (YouTube/FB)  │
│                 │    │                  │    │                 │
│ • URL Input     │    │ • Video Fetch    │    │ • Video Stream  │
│ • Progress UI   │    │ • Format Extract │    │ • Metadata      │
│ • Multi-server  │    │ • Stream Proxy   │    │ • Title/Quality │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

## 🎨 Design System

### Colors
- **Primary**: Purple-blue gradient (`#667eea` → `#764ba2`)
- **Success**: Green (`#38a169`)
- **Error**: Red (`#e53e3e`)
- **Background**: Semi-transparent glass effect

### Typography
- **Font**: Segoe UI, system-ui, sans-serif
- **Weights**: 400 (regular), 600 (semibold), 700 (bold)

### Components
- Glass morphism cards
- Gradient buttons with hover effects
- Animated progress bars
- Responsive form layouts

## 📊 Performance

- **Load Time**: < 1s (lightweight vanilla JS)
- **Bundle Size**: ~15KB (no frameworks)
- **Mobile Optimized**: Responsive design
- **Progressive Enhancement**: Works without JavaScript for basic functionality

## 🔒 Privacy & Legal

- **No Data Collection**: URLs are processed server-side only
- **No Storage**: No cookies or local storage used
- **User Responsibility**: Users must own or have permission for downloaded content
- **Compliance**: Respects platform terms of service

## 🤝 Contributing

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

### Development Guidelines
- Keep it vanilla (no frameworks)
- Follow existing code style
- Test on multiple browsers
- Ensure mobile responsiveness

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Almas Syed**
- GitHub: [@almas-syed05](https://github.com/almas-syed05)
- Portfolio: [your-portfolio.com](https://almassyed-portfolio.netlify.app/)

## 🙏 Acknowledgments

- Icons from [Heroicons](https://heroicons.com)
- Design inspiration from modern web apps
- Backend powered by yt-dlp and FastAPI

## 📈 Roadmap

- [ ] Instagram support
- [ ] Batch download functionality
- [ ] Download history
- [ ] Custom quality presets
- [ ] Dark/light mode toggle
- [ ] PWA support

---

<div align="center">
  <p>Made with ❤️ by Almas</p>
  <p>
    <a href="https://github.com/almas-syed05/vd-frontend/issues">Report Bug</a>
    ·
    <a href="https://github.com/almas-syed05/vd-frontend/issues">Request Feature</a>
  </p>
</div>
