# 🌟 Mahmudur Rahman Supto - Portfolio Website

A modern, responsive personal portfolio website built with **Tailwind CSS** and optimized **JavaScript** for showcasing skills, education, achievements, and projects.

## 📋 Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Customization](#customization)
- [Performance Optimizations](#performance-optimizations)
- [Browser Support](#browser-support)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## ✨ Features

### 🎨 Design & UI
- **Modern Responsive Design** - Mobile-first approach with breakpoints for all devices
- **Tailwind CSS** - Utility-first CSS framework for rapid development
- **Smooth Animations** - Fade-in effects, hover transitions, and stagger animations
- **Interactive Navigation** - Hamburger menu with smooth transitions for mobile
- **Active Section Highlighting** - Navigation links highlight based on scroll position

### 🚀 Performance
- **Optimized JavaScript** - Throttled scroll events and debounced resize handlers
- **Lazy Loading** - Images load only when visible in viewport
- **DOM Caching** - Elements queried once and reused for better performance
- **Intersection Observer API** - Modern scroll detection without performance overhead
- **RequestAnimationFrame** - Smooth 60fps animations

### 📱 User Experience
- **Smooth Scroll** - Animated scrolling to sections with header offset
- **Form Validation** - Real-time email and required field validation
- **Back to Top Button** - Auto-appearing floating button for easy navigation
- **Body Scroll Lock** - Prevents background scrolling when mobile menu is open
- **Touch Optimized** - Enhanced mobile and tablet experience

## 🛠️ Technologies Used

| Technology | Purpose |
|-----------|---------|
| **HTML5** | Semantic markup structure |
| **Tailwind CSS** | Utility-first styling framework |
| **JavaScript (ES6+)** | Interactive functionality |
| **Google Fonts** | Open Sans typography |
| **Web3Forms** | Contact form submission |
| **YouTube Embed** | Video resume integration |

## 📦 Installation

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Basic text editor or IDE (VS Code, Sublime Text, etc.)
- Optional: Local server for testing (Live Server, XAMPP, etc.)

### Setup Instructions

1. **Clone or Download the Repository**
   ```bash
   git clone https://github.com/yourusername/portfolio.git
   cd portfolio
   ```

2. **Open with Live Server** (Recommended)
   - Install VS Code Live Server extension
   - Right-click on `index.html`
   - Select "Open with Live Server"

3. **Or Open Directly**
   - Simply double-click `index.html` to open in your default browser

## 📁 Project Structure

```
portfolio/
│
├── index.html              # Main HTML file
├── README.md              # Project documentation
│
├── images/                # Image assets
│   ├── mahmud_1.png       # Profile picture
│   ├── header_bg.png      # Header background
│   ├── aciv-1.png         # Achievement certificates
│   ├── achiv-2.jpg
│   ├── uta.jpg
│   ├── takeoff.jpg
│   └── icons/             # Social media and skill icons
│       ├── icons8-linkedin-30.png
│       ├── icons8-x-30.png
│       ├── icons8-instagram-30.png
│       ├── icons8-python-48.png
│       └── icons8-flutter-48.png
│
└── documents/
    └── MD. Mahmudur Rahman Supto.pdf  # CV/Resume PDF
```

## 🎨 Customization

### Personal Information

Update your personal details in the `index.html` file:

```html
<!-- Name -->
<h1 class="text-4xl lg:text-6xl font-bold">Your Name Here</h1>

<!-- Email -->
<p class="item-description">youremail@example.com</p>

<!-- Social Links -->
<a href="https://www.linkedin.com/in/yourprofile/">LinkedIn</a>
```

### Colors

The portfolio uses an orange color scheme. To change the primary color, replace all instances of:
- `bg-orange-500` → `bg-[yourcolor]-500`
- `text-orange-500` → `text-[yourcolor]-500`
- `hover:bg-orange-600` → `hover:bg-[yourcolor]-600`

Available Tailwind colors: `red`, `blue`, `green`, `purple`, `pink`, `yellow`, `indigo`, `teal`, etc.

### Skills Section

Add or modify skills in the "What I Do" section:

```html
<div class="p-8 rounded-lg shadow-lg hover:shadow-xl transition-shadow bg-white">
    <img src="images/icons/your-icon.png" alt="Skill Name" class="mb-4 h-16">
    <h3 class="text-xl font-bold text-gray-900 mb-3">Your Skill</h3>
    <p class="text-gray-600">Description of your skill...</p>
</div>
```

### Contact Form

The form uses Web3Forms. To use your own form:

1. Sign up at [https://web3forms.com](https://web3forms.com)
2. Get your access key
3. Replace the access key in the form:

```html
<input type="hidden" name="access_key" value="YOUR_ACCESS_KEY_HERE">
```

## ⚡ Performance Optimizations

### JavaScript Optimizations

1. **Throttling** - Scroll events limited to execute every 100ms
2. **Debouncing** - Resize events delayed by 250ms
3. **DOM Caching** - Elements stored in object for reuse
4. **Event Delegation** - Minimal event listeners
5. **IIFE Pattern** - Code encapsulated to prevent global pollution

### Best Practices Implemented

```javascript
// Throttle function for performance
function throttle(func, wait) {
    let timeout;
    return function executedFunction(...args) {
        const later = () => {
            clearTimeout(timeout);
            func(...args);
        };
        clearTimeout(timeout);
        timeout = setTimeout(later, wait);
    };
}

// Usage
window.addEventListener('scroll', throttle(highlightActiveNav, 100));
```

### Image Optimization Tips

1. Compress images using tools like:
   - [TinyPNG](https://tinypng.com/)
   - [Squoosh](https://squoosh.app/)
   - [ImageOptim](https://imageoptim.com/)

2. Use appropriate formats:
   - Photos: JPG (compressed)
   - Graphics/Icons: PNG or SVG
   - Large images: WebP format

3. Implement lazy loading (already included in JS):
   ```html
   <img data-src="images/large-image.jpg" alt="Description">
   ```

## 🌐 Browser Support

| Browser | Version |
|---------|---------|
| Chrome | ✅ Latest 2 versions |
| Firefox | ✅ Latest 2 versions |
| Safari | ✅ Latest 2 versions |
| Edge | ✅ Latest 2 versions |
| Opera | ✅ Latest 2 versions |

### Mobile Browsers
- iOS Safari 12+
- Chrome Mobile
- Samsung Internet
- Firefox Mobile

## 📱 Responsive Breakpoints

```css
/* Mobile First Approach */
Default: 320px - 767px (Mobile)
md: 768px+ (Tablet)
lg: 1024px+ (Desktop)
xl: 1280px+ (Large Desktop)
2xl: 1536px+ (Extra Large)
```

## 🐛 Troubleshooting

### Common Issues

**Issue: Images not loading**
- Solution: Check file paths are correct and images exist in the `images/` folder

**Issue: Form not submitting**
- Solution: Verify your Web3Forms access key is correct and active

**Issue: Animations not working**
- Solution: Ensure JavaScript is enabled in your browser

**Issue: Mobile menu not closing**
- Solution: Clear browser cache and reload

## 🚀 Deployment

### GitHub Pages

1. Push your code to GitHub
2. Go to Settings → Pages
3. Select branch (main) and folder (root)
4. Save and wait for deployment

### Netlify

1. Sign up at [Netlify](https://www.netlify.com/)
2. Drag and drop your project folder
3. Your site is live!

### Vercel

```bash
npm install -g vercel
vercel
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Create a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📞 Contact

**Mahmudur Rahman Supto**

- 📧 Email: mahmud102496@gmail.com
- 📧 University: supto23105101419@diu.edu.bd
- 💼 LinkedIn: [mahmudur-rahman-2a37a5307](https://www.linkedin.com/in/mahmudur-rahman-2a37a5307/)
- 🐦 Twitter/X: [@MDMahmud1231123](https://x.com/MDMahmud1231123)
- 📸 Instagram: [@mahmudur_rahman_supto_](https://www.instagram.com/mahmudur_rahman_supto_/)

## 🙏 Acknowledgments

- [Tailwind CSS](https://tailwindcss.com/) - For the amazing utility-first framework
- [Google Fonts](https://fonts.google.com/) - For the Open Sans font family
- [Web3Forms](https://web3forms.com/) - For the contact form service
- [Icons8](https://icons8.com/) - For the social media icons

---

**Made with ❤️ by Mahmudur Rahman Supto**

*Last Updated: December 2024*
