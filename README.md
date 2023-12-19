# Parallax Magic: Breathe Life into Your Webflow Site with Animations & Scrolling

Webflow lets you craft stunning websites, but adding depth and intrigue with parallax scrolling and animations takes things to the next level. Imagine text that shimmers as you scroll, or backgrounds that dance with your movement. Here's a peek into this enchanting world, with a clean code example to get you started:

**1. Parallax Scrolling: A Multi-Dimensional Canvas**

Think of parallax scrolling as a layered stage. As you scroll, different elements move at different speeds, creating an illusion of depth and movement. This can be subtle – like a background image shifting slightly – or dramatic, with foreground elements zooming past.

**2. Animation Magic: Bringing Your Design to Life**

Animations add a touch of magic, making your website feel alive and interactive. Imagine buttons that pulse when you hover over them, icons that pop onto the screen, or text that playfully animates as you scroll.

**3. Short & Clean Code Example:**

Let's create a simple parallax effect where the background image scrolls at half the speed of the foreground text:

**HTML:**
```
<div class="parallax-container">
  <img src="background.jpg" class="parallax-background" alt="Background image">
  <div class="parallax-foreground">
    <h1>Welcome to my website!</h1>
  </div>
</div>

```

**CSS:**
```
.parallax-container {
  height: 500px;
  overflow: hidden;
}

.parallax-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  background-position: center;
  transform: translate3d(0, -50%, 0); /* Initial scroll offset for background */
}

.parallax-foreground {
  position: relative;
  top: 50%;
  transform: translateY(-50%);
  text-align: center;
}
```

**JavaScript:**

```
const parallaxBackground = document.querySelector('.parallax-background');

window.addEventListener('scroll', () => {
  const scrollTop = window.scrollY;
  parallaxBackground.style.transform = `translate3d(0, ${scrollTop * 0.5}px, 0)`; // Update scroll offset for background with half the scroll amount
});
```

# Need help?
Stuck with custom css code? [Contact us](https://epyc.in/).
