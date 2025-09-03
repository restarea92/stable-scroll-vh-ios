# stable-scroll-vh-ios
A lightweight JavaScript utility to stabilize viewport height units (svh, lvh) on iOS and prevent scroll jitter. Some iOS in-app browsers or non-Safari browsers may incorrectly interpret svh and lvh similar to dvh, causing layout issues. This module ensures consistent viewport sizing for mobile web apps affected by these quirks.

## Features

- Stabilizes `lvh` values on iOS devices
- Updates CSS variable `--lvh` dynamically
- Handles scroll, touch, and resize events smoothly
- Lightweight and dependency-free

## Installation

> Coming Soon

## Usage

### JS Usage
```js
import stableScroll from 'stable-scroll-vh-ios';

// Initialize the module (uses lvh by default)
stableScroll.init();
```

### CSS Usage

```css
.fullscreen {
  /* Fallback order:
     1. Latest browsers: var(--lvh)
     2. If var() not supported: 1lvh
     3. Old browsers: 100vh
  */
  height: 100vh; /* fallback for very old browsers */
  height: calc(100 * var(--lvh, 1lvh));
}
```
