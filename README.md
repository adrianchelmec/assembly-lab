# Assembly Lab — Mobile Phone Browser Adaptation

## Mobile Adaptation & Interaction Improvements

- **Smooth Hardware-Accelerated Subparts Scrolling (`touch-action: pan-x`, `scroll-snap`):**
  - Uses `touch-action: pan-x;`, `-webkit-overflow-scrolling: touch;`, `scroll-behavior: smooth;`, and `scroll-snap-type: x proximity;` for native 60/120fps momentum flicking on mobile phones.
  - Automatically suppresses whole-page bounce with `overscroll-behavior-x: contain`.
  - Disambiguates touch scrolling from vertical drag gestures so horizontal swiping scrolls the subparts tray smoothly without accidental drags or false error buzzes.

- **Dual Interaction Modes (Drag-and-Drop or Tap-to-Place):**
  - **Drag-and-Drop:** Drag components upward from the tray onto the workbench with automatic `-52px` vertical finger lift offset and expanded `+14px` touch snap tolerance.
  - **Tap-to-Place:** Tapping a subpart highlights it with an active selection ring; tapping anywhere near its workbench blueprint target smoothly snaps it into place, eliminating long-distance dragging strain on mobile screens.

- **Visual Scroll Cues & Scroll Buttons:**
  - Adds left and right dynamic gradient fade masks (`can-scroll-left`, `can-scroll-right`) and sleek chevron controls (`‹` and `›`) so users instantly see when additional components are available offscreen.
  - Desktop wheel listener maps trackpad/mouse scroll wheels to smooth horizontal scrolling.
  - Automatically scrolls the tray to center the next unplaced subpart whenever a component is assembled.

- **Playful Cartoon Sound Effects (OK & NOK):**
  - **OK (Snap Success):** Rotates dynamically across 4 humorous cartoon audio effects — *Juicy Bubble Pop ("Bloop-POP!")*, *Spring Boing ("Boi-i-ing!")*, *Slide Whistle Up ("Wheee-Ding!")*, and *Playful Marimba Double-Pop ("Pip-Pop!")*.
  - **NOK (Misplacement / Fail):** Replaces harsh buzzes with 4 comedic cartoon fails — *Classic Sad Trombone ("Womp... WOMP...")*, *Spring Unwind ("Pwaaa-ooong!")*, *Balloon Squeak / Raspberry ("Pfffft-blrt!")*, and *Clown Horn ("Honk-Honk!")*.

- **AudioContext Autoplay Compliance:**
  - Lazily initializes Web Audio oscillators on the first user interaction, eliminating browser console autoplay policy warnings while ensuring immediate, reliable sound synthesis.

- **Local Progress & State Persistence (`localStorage`):**
  - Automatically stores completed level badges (`✓ Level N`) and restores the last active level upon reloading or reopening the browser tab.

- **Accessible Controls:**
  - Adds full keyboard navigation (`Tab`, `Enter`, `Space`, `R` for rotation) and ARIA attributes for screen readers and assistive devices.
