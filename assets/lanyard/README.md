# Interactive portrait badge

The model and original band texture come from [React Bits Lanyard](https://github.com/DavidHDev/react-bits/tree/main/src/assets/lanyard).
The component is adapted from the React Bits source supplied by the site owner. See LICENSE.md for the upstream license.

The website paints its own warm-colored badge artwork and band at runtime. The source portrait is `public/bio.jpg`; the introduction video is `public/assets/video/self-introduction.mp4` (copied from the owner's supplied video).

`preview-zh.webp` and `preview-en.webp` are transparent renders of this same GLB, lighting, portrait, and localized artwork, not a separately drawn badge. The page preloads the appropriate ~47 KB preview and displays it in the server-rendered HTML until the first 3D frame is ready. Reduced-motion and failed 3D rendering keep this same preview. The 3D simulation starts hanging vertically to match it.

If the portrait, name, model, materials, lighting, or camera framing changes, regenerate both previews: render `LanyardScene` at 410 × 760 CSS pixels with DPR 1.5, let the physics settle, and export the transparent canvas as WebP at quality 0.9 (615 × 1140 pixels). Temporarily enable `preserveDrawingBuffer` only while exporting; leave it disabled in production. The CSS preview uses the same 2.05 × 3.8 camera framing; its video overlay aligns to the rendered photo area.

Click/tap toggles playback in the card's photo region. Dragging more than seven pixels moves the badge without toggling video. Playback completion restores the portrait. Playback pauses when the badge leaves the viewport or the browser tab is hidden. The badge name follows the page locale. Keyboard playback, reduced-motion mode, and a non-WebGL fallback remain available.
