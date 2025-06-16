# 🌐 3D Web Creative Agency – Hybrid HTML & 3D Landing Page

This project showcases a modern landing page for a fictional **3D web development agency**, combining traditional HTML structure with immersive 3D experiences using **React Three Fiber** and **Drei**.

---

## 🚀 Live Demo

🔗 [https://your-agency.vercel.app](https://r3f-3d-web-creative-agency-demo.vercel.app/)

---

## 🎯 Project Overview

We've built many 3D scenes before—but typically one at a time, fully taking over the screen. In this project, we break that pattern by integrating **multiple 3D scenes within a single scrollable HTML page**, just like inserting videos or images.

This creates a **hybrid layout**:  
✅ Fully indexable & accessible content  
✅ Multiple performant 3D scenes  
✅ Smooth scroll-based interaction

---

## 🔍 Features

- 🧩 Multi-Section Layout with 3D Integration
  Home, Services, Team, Portfolio, and Contact sections.

Each section combines traditional HTML content with immersive 3D visuals.

- 🎥 Independent 3D Views with View
  Multiple View components allow rendering independent 3D scenes on one Canvas.

Views are bound to HTML containers, enabling flexible positioning and interactivity.

- 🎮 Individual Camera Controls per View
  Each view has its own dedicated camera to avoid shared movement issues.

Supports OrbitControls or CameraControls scoped to their respective scenes.

Implemented using <PerspectiveCamera makeDefault /> inside each view.

⚙️ Single WebGL Context
Uses a single <Canvas /> to render all scenes efficiently.

Reduces GPU overhead and improves performance, especially on mobile.

- ⚠️ Scroll Awareness
  Views respond to scroll, resize, touch and mouse events.

Minor gaps may appear when scrolling rapidly—known limitation of View.

- 📱 Responsive & Accessible
  Fully responsive layout.

HTML content is indexable for SEO and accessible by screen readers.

- 🎨 Clean and Modern Stack
  Built with:

react-three-fiber for 3D rendering

@react-three/drei for helper components like View, OrbitControls, PerspectiveCamera

Vite for lightning-fast development

React for UI

### 🧩 Sections

- **Home** – Hero section with branding and 3D background
- **Services** – Interactive 3D icons representing services
- **Team** – Floating avatars in 3D
- **Portfolio** – Scroll-triggered 3D showcases of projects
- **Contact** – Final call-to-action with 3D illustration

### 🧠 Technologies

- [React Three Fiber](https://github.com/pmndrs/react-three-fiber)
- [Drei](https://github.com/pmndrs/drei) – View, PresentationControls, etc.
- [React](https://reactjs.org/)
- [Vite](https://vitejs.dev/) – Fast build tool
- HTML/CSS – Semantic structure and styling

---

## 🎬 The View Component (from Drei)

We use Drei’s `View` component to render **multiple 3D scenes** with **only one WebGL canvas**, improving performance and user experience.

- One single `<Canvas />`, many `<View />` targets
- Each view is bound to a unique HTML container
- Supports scroll, touch, resize & mouse events
- Enables modular scene design

### ⚠️ Scroll Limitation

> View does not exist _within_ its container—it _tracks_ it.  
> This means it may slightly lag or misalign on fast scrolls.

✅ For most use cases this is fine.  
🛠️ For pixel-perfect alignment, consider using **multiple Canvas components** instead.

---

You now have the best of both worlds:

- 🎨 Beautiful 3D interactions powered by WebGL
- 🧾 SEO-ready content, accessible and responsive
- 🔁 Seamless hybrid UX using View-based rendering

This project is a great starting point for anyone building **immersive creative agency websites**, product portfolios, or interactive storytelling experiences.

---

## 🚀 Getting Started

### Clone the project

```bash
git clone https://github.com/delafuentej/r3f_staging.git
cd r3f_staging
yarn install
yarn dev
```
