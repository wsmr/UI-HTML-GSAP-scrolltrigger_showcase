# GSAP ScrollTrigger Showcase

A comprehensive collection of scroll-triggered animations using GSAP ScrollTrigger. This showcase demonstrates 10 different scroll animation techniques with modern design and optimal performance.

![GSAP ScrollTrigger Showcase](https://img.shields.io/badge/GSAP-3.12.2-88CE02?style=flat-square&logo=greensock&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)

## 🎯 Features

### 10 Scroll Animation Techniques

1. **Fade In on Scroll** - Smooth fade and slide animations as elements enter the viewport
2. **Horizontal Scroll Pinning** - Apple-style horizontal panel sliding
3. **Parallax Effect** - Multi-layer parallax with different scroll speeds
4. **Pin & Rotate** - 360° rotation while section is pinned
5. **Text Reveal** - Progressive word-by-word text reveal
6. **Scale Animation** - Scale up/down effects on scroll
7. **Stagger Animation** - Sequential item animations
8. **Image Reveal** - Wipe effect for revealing images
9. **Counter Animation** - Animated number counters on scroll
10. **Progress Indicators** - Scroll progress bar and navigation dots

### Additional Features

- ✨ Modern, clean design with gradient aesthetics
- 📱 Fully responsive (desktop, tablet, mobile)
- 🚀 Optimized for 60fps performance
- 🎨 Easy to customize and extend
- 🧭 Interactive navigation with dots
- 📊 Visual scroll progress indicator
- 🌟 Animated starfield background

## 🚀 Quick Start

### View Demo

Simply open `index.html` in your browser - no build process required!

### Use in Your Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/wsmr/UI-HTML-GSAP-scrolltrigger_showcase.git
   cd UI-HTML-GSAP-scrolltrigger_showcase
   ```

2. **Open in browser**
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   
   # Or simply open index.html in your browser
   ```

3. **Start customizing!**

## 📖 Documentation

### Basic Usage

Each animation technique is self-contained and can be copied directly into your project. Here's a basic example:

```javascript
// Fade in animation
gsap.from(".your-element", {
    opacity: 0,
    y: 100,
    duration: 1,
    scrollTrigger: {
        trigger: ".your-element",
        start: "top 80%",
        toggleActions: "play none none reverse"
    }
});
```

### Customization Examples

#### Adjust Animation Speed

```javascript
scrollTrigger: {
    scrub: 1,  // Lower = faster, higher = slower
}
```

#### Change Pin Duration

```javascript
scrollTrigger: {
    end: "+=200%",  // Pin for 2x viewport height
}
```

#### Modify Stagger Timing

```javascript
gsap.from(".items", {
    opacity: 0,
    stagger: 0.2,  // Delay between each item
});
```

### ScrollTrigger Parameters

| Parameter | Description | Example |
|-----------|-------------|---------|
| `trigger` | Element that triggers the animation | `".my-section"` |
| `start` | When animation starts | `"top center"` |
| `end` | When animation ends | `"bottom top"` |
| `scrub` | Links animation to scrollbar | `1` or `true` |
| `pin` | Pins element during scroll | `true` |
| `snap` | Snaps to specific points | `1 / 4` |
| `toggleActions` | Actions on enter/leave | `"play none none reverse"` |

## 🎨 Customization Guide

### Colors & Gradients

All gradients are defined in the CSS. Find and replace these values:

```css
/* Example gradient */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Animation Timing

Adjust these values in the JavaScript:

```javascript
duration: 1,      // Animation duration in seconds
delay: 0.3,       // Delay before animation starts
stagger: 0.2,     // Stagger delay between items
```

### Section Heights

Control section heights in CSS:

```css
.section {
    min-height: 100vh;  /* Full viewport height */
}
```

## 🏗️ Project Structure

```
UI-HTML-GSAP-scrolltrigger_showcase/
├── index.html              # Main showcase file
├── README.md              # This file
├── LICENSE               # MIT License
└── .gitignore           # Git ignore rules
```

## 📦 Dependencies

- [GSAP 3.12.2](https://greensock.com/gsap/) - Animation library
- [ScrollTrigger](https://greensock.com/scrolltrigger/) - Scroll-based animations

Both are loaded via CDN in the HTML file. No installation required!

## 🌐 Browser Support

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers

## 💡 Use Cases

Perfect for:
- Product showcases (Apple-style presentations)
- Portfolio websites
- Landing pages
- Marketing sites
- Storytelling websites
- Interactive timelines
- Feature highlights
- Case studies

## 🔧 Performance Tips

1. **Use `will-change` sparingly** - Only on elements actively animating
2. **Prefer transforms over position** - `transform: translateX()` instead of `left`
3. **Enable GPU acceleration** - Use `transform: translate3d(0,0,0)`
4. **Optimize images** - Compress and use appropriate formats
5. **Use `scrub`** - Creates smooth, performant scroll-linked animations

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📬 Contact

Your Name - [@ywsmr](https://twitter.com/wsmr)

Project Link: [https://github.com/wsmr/UI-HTML-GSAP-scrolltrigger_showcase](https://github.com/wsmr/UI-HTML-GSAP-scrolltrigger_showcase)

## 🙏 Acknowledgments

- [GSAP](https://greensock.com/) - For the amazing animation library
- [GreenSock Forums](https://greensock.com/forums/) - For the helpful community
- Inspired by modern scroll-driven websites

## ⭐ Star This Repo

If you find this project helpful, please consider giving it a star!

---

Made with ❤️ and GSAP
