# Assembly Lab — Mobile Phone Browser Adaptation

## Mobile Adaptation Improvements
- **Viewport & Safe-Area Support (`100dvh`, `viewport-fit=cover`):** Adapts cleanly to mobile browser address bars and notched screens without clipping or accidental page bounce.
- **Responsive Header, Info Strip & HUD:** Stacks level navigation cleanly on narrow screens, condenses button labels on small viewports, and keeps level/progress cards compact so the assembly workbench stays tall and clear.
- **Horizontal Scrollable Component Tray:** Turns the bottom tray into a smooth touch-scrollable strip on phones (`≤ 768px`) with larger tap targets for the `↻` rotation button.
- **Touch Drag Precision:** Adds a slight vertical lift offset (`-52px`) and slightly expanded touch snap radius (`+14px`) on coarse-pointer/touch screens so your finger doesn't cover the drop zone while dragging parts or room objects.
