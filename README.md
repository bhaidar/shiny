# Shiny, Simulating Reflections for Mobile Websites

Add shiny reflections to **text**, **backgrounds**, and **borders** on devices that support the `DeviceMotion` event.

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/rikschennink/shiny/blob/gh-pages/LICENSE)
[![npm version](https://badge.fury.io/js/%40rikschennink%2Fshiny.svg)](https://badge.fury.io/js/%40rikschennink%2Fshiny)
[![Support on Patreon](https://img.shields.io/badge/support-patreon-salmon.svg)](https://www.patreon.com/rikschennink)

**Please note this library is still in development**


## Todo

- Fix landscape orientation rendering
- Reset origin when browser session resumes
- Test if correctly fails on older browsers
- Test on Android


## Usage

```html
<div class="my-shiny-element">Hello World</div>
<script>
shiny('.my-shiny-element', {
    // type of shiny to render, 
    // 'background', 'border', or 'text'
    type: 'background',
    gradient: {
        // type of gradient
        type: 'radial',

        // flip movement over axis
        flip: {
            x: true,
            y: false
        },

        // colors to use
        colors: [
            // offset, color, opacity
            [0, '#fff', 1],
            [1, '#fff', 0],
        ]
    },
    // optional pattern fill
    pattern: {
        type: 'noise',
        opacity: .5
    }
});
</script>
```