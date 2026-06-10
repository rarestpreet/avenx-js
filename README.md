![Alternativtext](https://raw.githubusercontent.com/Avenx-JS/.github/refs/heads/main/media/core-header.jpeg)

# 🚀 Avenx-JS

A lightweight reactive JavaScript framework with a custom compiler, scoped styling, and built-in state management.
Avenx-JS is an experimental frontend framework designed to simplify UI development by reducing boilerplate and introducing a compiler-driven component system with reactive state, scoped CSS, and CLI tooling.

---

## ✨ Why Avenx?

Modern frontend stacks often come with:

- heavy tooling
- large dependency trees
- verbose state management
- framework lock-in complexity

Avenx explores a different approach:

> Minimal setup. Reactive by default. Compiler-driven components.

---

## ⚡ Features

### 🔄 Reactivity

State is automatically tracked and re-rendered using JavaScript Proxies.

### 🧩 Component System

Components combine template, logic, and state in a single `.component.js` file.

### 🎨 Scoped Styling

CSS is automatically scoped using hashed class generation to avoid conflicts.

### 🌐 Global State (Bridges)

Shared reactive state across components via `.bridge.js`.

### 🛠️ CLI Tooling

Built-in CLI for project scaffolding and development workflow.

---

## 🚀 Quick Start

```bash
npm install avenx-core

npx avenx init
npx avenx g component test
npx avenx build
npx avenx serve
```
**Your app will run at:**

```text
http://localhost:3000
```
---

## 🧠 Example

**Component**

```html
<state count="0" />

<h1 @click="count++">
    Count: {{ count }}
</h1>
```

That's it - fully reactive UI without additional state libraries.

**Styling**

```css
<@global>
    @def primary-color #ff3e00;
</@global>

<@css>
    h1 {
        color: var(--primary-color);
        cursor: pointer;
    }

    h1:hover {
        opacity: 0.8;
    }
</@css>
```

**Shared State (Bridges)**

```javascript
export default {
    isLoggedIn: false,
    username: ''
}
```

**Usage:**
```html
<p>User: {{ AuthBridge.username }}</p>
```

---

## 📦 Installation

```bash
npm install avenx-core
```

---

## 📁 Core Concept

Avenx-JS is built around 3 core ideas:
- **Components as unified files**
- **Reactivity via Proxy-based state tracking**
- **Compiler-driven DOM updates**

---

## 📌 Status

This project is currently a proof-of-concept framework and actively evolving.

---

## 📄 License

MIT

---

## ⭐ Support

If you find Avenx-JS useful, consider leaving a star on GitHub - it helps the project grow.