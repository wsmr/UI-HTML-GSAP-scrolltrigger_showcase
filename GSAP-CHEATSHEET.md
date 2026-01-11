# GSAP ScrollTrigger Cheat Sheet

Quick reference guide for GSAP ScrollTrigger animations.

## 📚 Basic Setup

```javascript
// Import GSAP and ScrollTrigger
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>

// Register plugin
gsap.registerPlugin(ScrollTrigger);
```

## 🎯 Common Patterns

### 1. Fade In on Scroll

```javascript
gsap.from(".element", {
    opacity: 0,
    y: 100,
    duration: 1,
    scrollTrigger: {
        trigger: ".element",
        start: "top 80%",
        end: "top 50%",
        toggleActions: "play none none reverse"
    }
});
```

### 2. Pin Section

```javascript
gsap.to(".element", {
    x: 500,
    scrollTrigger: {
        trigger: ".section",
        pin: true,
        scrub: 1,
        start: "top top",
        end: "+=100%"
    }
});
```

### 3. Horizontal Scroll

```javascript
const panels = gsap.utils.toArray(".panel");

gsap.to(panels, {
    xPercent: -100 * (panels.length - 1),
    ease: "none",
    scrollTrigger: {
        trigger: ".container",
        pin: true,
        scrub: 1,
        snap: 1 / (panels.length - 1),
        end: () => "+=" + document.querySelector(".container").offsetWidth
    }
});
```

### 4. Parallax Effect

```javascript
gsap.to(".background", {
    y: (i, target) => -ScrollTrigger.maxScroll(window) * target.dataset.speed,
    ease: "none",
    scrollTrigger: {
        start: 0,
        end: "max",
        invalidateOnRefresh: true,
        scrub: 0
    }
});
```

### 5. Stagger Animation

```javascript
gsap.from(".item", {
    opacity: 0,
    y: 50,
    stagger: 0.2,
    duration: 1,
    scrollTrigger: {
        trigger: ".container",
        start: "top 70%"
    }
});
```

### 6. Counter Animation

```javascript
gsap.to(".counter", {
    innerText: 1000,
    duration: 2,
    snap: { innerText: 1 },
    scrollTrigger: {
        trigger: ".counter",
        start: "top 80%"
    }
});
```

### 7. Scale on Scroll

```javascript
gsap.fromTo(".element",
    { scale: 0.8, opacity: 0 },
    {
        scale: 1,
        opacity: 1,
        scrollTrigger: {
            trigger: ".element",
            scrub: true,
            start: "top bottom",
            end: "top center"
        }
    }
);
```

### 8. Text Reveal

```javascript
gsap.from(".word", {
    opacity: 0,
    y: 20,
    stagger: 0.1,
    scrollTrigger: {
        trigger: ".text-container",
        start: "top 80%"
    }
});
```

### 9. Progress Bar

```javascript
gsap.to(".progress-bar", {
    width: "100%",
    ease: "none",
    scrollTrigger: {
        trigger: "body",
        start: "top top",
        end: "bottom bottom",
        scrub: 0.3
    }
});
```

### 10. Rotation Effect

```javascript
gsap.to(".element", {
    rotation: 360,
    scrollTrigger: {
        trigger: ".section",
        pin: true,
        scrub: 1,
        start: "top top",
        end: "+=100%"
    }
});
```

## ⚙️ ScrollTrigger Parameters

### Essential Parameters

| Parameter | Type | Description | Example |
|-----------|------|-------------|---------|
| `trigger` | String/Element | Element that triggers animation | `".section"` |
| `start` | String | When animation starts | `"top center"` |
| `end` | String | When animation ends | `"bottom top"` |
| `scrub` | Boolean/Number | Links animation to scroll | `true` or `1` |
| `pin` | Boolean | Pins element during scroll | `true` |
| `markers` | Boolean | Shows debug markers | `true` |

### Start/End Values

```javascript
// Format: "trigger viewport"
start: "top top"      // Trigger's top hits viewport's top
start: "top center"   // Trigger's top hits viewport's center
start: "top bottom"   // Trigger's top hits viewport's bottom
start: "center center" // Trigger's center hits viewport's center
start: "bottom top"   // Trigger's bottom hits viewport's top

// With offset
start: "top top+=100" // 100px after trigger's top hits viewport's top
start: "top 80%"      // Trigger's top hits 80% down the viewport

// Dynamic
end: () => "+=" + element.offsetHeight
```

### Toggle Actions

Format: `"onEnter onLeave onEnterBack onLeaveBack"`

```javascript
toggleActions: "play none none reverse"
toggleActions: "play pause resume reset"
toggleActions: "play complete reverse reset"
```

Actions: `play`, `pause`, `resume`, `reset`, `restart`, `complete`, `reverse`, `none`

### Scrub Values

```javascript
scrub: true        // Immediate link to scrollbar
scrub: 0.5         // 0.5 second delay (smooth)
scrub: 1           // 1 second delay (very smooth)
```

### Snap

```javascript
snap: 1 / 4           // Snap to quarter points
snap: {
    snapTo: 0.1,      // Snap to 10% increments
    duration: 0.5,    // Snap duration
    ease: "power1.inOut"
}
```

## 🎨 Animation Properties

### Position

```javascript
x: 100              // Move 100px right
y: -50              // Move 50px up
xPercent: -100      // Move 100% of element width left
yPercent: 50        // Move 50% of element height down
```

### Transform

```javascript
rotation: 360       // Rotate 360 degrees
rotationX: 180      // 3D rotate on X axis
rotationY: 90       // 3D rotate on Y axis
scale: 1.5          // Scale to 150%
scaleX: 2           // Scale width only
scaleY: 0.5         // Scale height only
```

### Appearance

```javascript
opacity: 0          // Fade out
autoAlpha: 0        // opacity + visibility
backgroundColor: "#fff"
color: "#000"
```

### Advanced

```javascript
transformOrigin: "center center"
ease: "power2.out"
duration: 1
delay: 0.5
stagger: 0.2
```

## 🚀 Easing Functions

```javascript
// Power
ease: "power1.out"    // Gentle
ease: "power2.out"    // Medium
ease: "power3.out"    // Strong
ease: "power4.out"    // Very strong

// Back
ease: "back.out"      // Overshoots slightly
ease: "back.inOut"

// Elastic
ease: "elastic.out"   // Bouncy
ease: "bounce.out"    // Bounces at end

// Others
ease: "none"          // Linear
ease: "circ.out"      // Circular
ease: "expo.out"      // Exponential
```

## 🛠️ Utility Functions

```javascript
// Convert NodeList to Array
const items = gsap.utils.toArray(".item");

// Selector
const el = gsap.utils.selector(container);
el(".child"); // Finds .child within container

// Interpolate
gsap.utils.interpolate(0, 100, 0.5); // Returns 50

// Map Range
gsap.utils.mapRange(0, 100, 0, 1, 50); // Maps 50 from 0-100 to 0-1

// Clamp
gsap.utils.clamp(0, 100, 150); // Returns 100

// Random
gsap.utils.random(0, 100);          // Random number
gsap.utils.random([0, 50, 100]);    // Random from array
```

## 📱 Responsive Animations

```javascript
ScrollTrigger.matchMedia({
    // Desktop
    "(min-width: 800px)": function() {
        gsap.to(".element", {
            x: 500,
            scrollTrigger: { trigger: ".section", scrub: true }
        });
    },
    
    // Mobile
    "(max-width: 799px)": function() {
        gsap.to(".element", {
            x: 200,
            scrollTrigger: { trigger: ".section", scrub: true }
        });
    }
});
```

## 🔄 Refresh & Update

```javascript
// Refresh all ScrollTriggers
ScrollTrigger.refresh();

// After window resize
window.addEventListener("resize", () => {
    ScrollTrigger.refresh();
});

// Kill specific ScrollTrigger
const st = ScrollTrigger.create({...});
st.kill();

// Kill all
ScrollTrigger.getAll().forEach(st => st.kill());
```

## 🐛 Debugging

```javascript
scrollTrigger: {
    markers: true,              // Show start/end markers
    id: "my-animation",        // Label in console
    onEnter: () => console.log("entered"),
    onLeave: () => console.log("left"),
    onUpdate: (self) => console.log("progress:", self.progress)
}
```

## ⚡ Performance Tips

1. **Use transforms** instead of position properties
   ```javascript
   // ✅ Good - GPU accelerated
   gsap.to(el, { x: 100, y: 50 });
   
   // ❌ Bad - causes reflow
   gsap.to(el, { left: 100, top: 50 });
   ```

2. **Use `will-change` sparingly**
   ```javascript
   // Only on actively animating elements
   gsap.set(".element", { willChange: "transform" });
   ```

3. **Batch similar animations**
   ```javascript
   gsap.to(".items", {
       opacity: 1,
       stagger: 0.1  // Instead of individual animations
   });
   ```

4. **Use `invalidateOnRefresh`** for dynamic values
   ```javascript
   scrollTrigger: {
       invalidateOnRefresh: true
   }
   ```

## 📖 Additional Resources

- [GSAP Docs](https://greensock.com/docs/)
- [ScrollTrigger Docs](https://greensock.com/docs/v3/Plugins/ScrollTrigger)
- [GSAP Forum](https://greensock.com/forums/)
- [CodePen Examples](https://codepen.io/GreenSock)

---

Happy animating! 🎉
