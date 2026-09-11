# Interactive portrait badge

The model and original band texture come from [React Bits Lanyard](https://github.com/DavidHDev/react-bits/tree/main/src/assets/lanyard).
The component is adapted from the React Bits source supplied by the site owner. See LICENSE.md for the upstream license.

The website paints its own warm-colored badge artwork and band at runtime. The source portrait is `public/bio.jpg`; the introduction video is `public/assets/video/self-introduction.mp4` (copied from the owner's supplied video).

Click/tap toggles playback in the card's photo region. Dragging more than seven pixels moves the badge without toggling video. Playback completion restores the portrait. Playback pauses when the badge leaves the viewport or the browser tab is hidden. The badge name follows the page locale. Keyboard playback, reduced-motion mode, and a non-WebGL fallback remain available.
