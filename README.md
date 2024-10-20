# DAY_020 | Showcase Card Animation with Horizontal Parallax Scroll

## Project Overview

This project is part of my daily code challenge series, **DAY_020**, where I built a showcase card animation with a **horizontal parallax scroll animation**. I used **HTML**, **CSS**, **JavaScript**, **GSAP**, and **Lenis** to create smooth, interactive effects. The animation features a set of portfolio cards highlighting my client work in web design and visual arts.

The horizontal parallax scroll and animation techniques are inspired by the modern, smooth interactions seen in **Critical Danger’s** Awwwards-winning website.

### Inspiration from Awwwards Element from 
Check the site out here! [Critical Danger](https://www.criticaldanger.com/)

---

## Preview

![DAY_020 Preview](./assets/DAY_020_1.gif)

## Inspiration

![Critical Danger](./assets/DAY_020_2.gif)

---

## Key Features

- **Showcase Card Animation**: Interactive cards featuring client projects, with smooth animations and transitions.
- **Horizontal Parallax Scroll Animation**: A scrolling experience that moves elements horizontally based on the user’s scroll position.
- **Smooth Scrolling with Lenis**: Implemented smooth scrolling for a refined user experience.
- **GSAP Animations**: All animations are powered by **GSAP** for high-performance interactions.
- **Responsive Design**: Optimized for various screen sizes, ensuring a smooth experience across devices.

---

## GSAP in Action

**GSAP (GreenSock Animation Platform)** powers the smooth transitions and animations. Below are some key snippets of the animation setup:

### Horizontal Parallax Scroll Animation

```javascript
gsap.registerPlugin(ScrollTrigger);

gsap.to(".parallax-wrapper", {
  xPercent: -100 * (document.querySelectorAll('.parallax-item').length - 1),
  ease: "none",
  scrollTrigger: {
    trigger: ".parallax",
    pin: true,
    scrub: 1,
    snap: 1 / (document.querySelectorAll('.parallax-item').length - 1),
    end: "+=3000",
  },
});
```

**Explanation**:

- **Horizontal Parallax**: Elements scroll horizontally based on the user’s scrolling, creating a dynamic, immersive effect.
- **Smooth Pinning**: The `.parallax` section is pinned in place while the content moves horizontally.

---

### Card Animations with ScrollTrigger

```javascript
ScrollTrigger.create({
  trigger: stickySection,
  start: "top top",
  end: `+=${stickyHeight}px`,
  pin: true,
  pinSpacing: true,
  onUpdate: (self) => {
    const progress = self.progress;
    const maxTranslate = stickyHeader.offsetWidth - window.innerWidth;
    const translateX = -progress * maxTranslate;
    gsap.set(stickyHeader, { x: translateX });
  },
});
```

**Explanation**:

- **Card Movement**: Cards animate with the scroll, creating interactive and smooth effects as the user moves through the page.

---

## How to Run

1. **Clone the repository**:

   ```bash
   git clone https://github.com/thounny/DAY_020.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd DAY_020
   ```

3. **Open the `index.html` file** in your browser, or use a local development server like **Live Server** in VSCode.

---

## Project Structure

```bash
DAY_020/
├── assets/
├── fonts/
├── styles.css
├── index.html
├── script.js
```

---

## Features

- **Showcase Card Animation**: Interactive and engaging card animations.
- **Horizontal Parallax Scroll**: Smooth, interactive horizontal scrolling using GSAP and ScrollTrigger.
- **Lenis Smooth Scroll**: Enhances the user experience with smooth scrolling.
- **GSAP Animations**: High-performance animations that work seamlessly with the scroll effects.
- **Responsive Design**: Fully optimized for various screen sizes.

---

## Technologies Used

- **HTML5**: For the structure and layout.
- **CSS3**: Custom styling and responsiveness.
- **JavaScript (ES6)**: Interactivity and animation logic.
- **GSAP (GreenSock Animation Platform)**: Powers the animations and parallax effects.
- **Lenis**: Adds smooth scrolling behavior.

---

## Author

![Logo](./assets/index_dwn.gif)

**Thounny Keo**  
Creative Developer & Designer  
Frontend Development Student | Year Up United

---

![miku](./assets/miku.gif)