# Expo Camera Preview Flickering/Freezing with Custom Overlay

This repository demonstrates a bug in Expo's `Camera` API where the preview flickers or freezes when a custom component overlays it. The bug is more pronounced on lower-end devices and when the overlay is complex.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app on a physical device (preferably an older one) or emulator.
4. Observe the camera preview – you'll likely see intermittent flickering or freezing.

## Solution

The solution involves optimizing the rendering performance of the overlay component.  Techniques like using `useMemo` or `React.memo` to memoize computationally expensive parts of the overlay can significantly improve performance.  Using more efficient rendering libraries or methods may be required for particularly intensive overlays. 

This example showcases how to improve rendering performance using `useMemo` and `React.memo`. 