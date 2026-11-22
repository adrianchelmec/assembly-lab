# Assembly Lab — Mobile Phone Browser Adaptation

## Mobile Adaptation Improvements
- **Viewport & Safe-Area Support (`100dvh`, `viewport-fit=cover`):** Adapts cleanly to mobile browser address bars and notched screens without clipping or accidental page bounce.
- **Responsive Header, Info Strip & HUD:** Stacks level navigation cleanly on narrow screens, condenses button labels on small viewports, and keeps level/progress cards compact so the assembly workbench stays tall and clear.
- **Horizontal Scrollable Component Tray:** Turns the bottom tray into a smooth touch-scrollable strip on phones (`≤ 768px`) with larger tap targets for the `↻` rotation button.
- **Touch Drag Precision:** Adds a slight vertical lift offset (`-52px`) and slightly expanded touch snap radius (`+14px`) on coarse-pointer/touch screens so your finger doesn't cover the drop zone while dragging parts or room objects.

- **Animated Workshop Apprentice Companion ("Joey"):**
  - Faithfully recreated from the hand-drawn character sketch (`character.jpg`) as a scalable, zero-dependency vector SVG mascot in the HUD and Victory Modal.
  - Features a real-time emotional state machine (`idle`, `curious`, `happy`, `puzzled`, `thinking`, `celebrate`) with expressive animations (gentle breathing, joyful hops, curious head-tilts, thinking lightbulb, and celebratory cheers) and interactive speech-bubble feedback.
  - Tapping or clicking Joey triggers a playful 360° spin and encouraging engineering quotes.

- **Playful Cartoon Sound Effects (OK & NOK):**
  - Rotates dynamically across 4 humorous cartoon success effects (*Bubble Pop*, *Spring Boing*, *Slide Whistle*, *Double Marimba Pop*) and 4 comedic misplacement effects (*Sad Trombone*, *Spring Unwind*, *Balloon Raspberry*, *Clown Horn*).
