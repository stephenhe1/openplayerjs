# UI Coverage (Progress: 10/10)
Legend: [ ] not yet tested  -  [x] test written and passing  -  [~] intentionally skipped (reason)

## Core API (no player UI shell)
- [x] /examples/core.html — registerPlugin() + HLS auto-attach; video element present, explainer paragraph, no .op-player wrapper

## Player UI — VOD
- [x] /examples/basic.html — HLS + VAST skippable preroll; play/pause, progress, settings (Speed submenu, back, Escape), fullscreen, no captions btn
- [x] /examples/ads.html — VMAP pre/mid/post-roll; player renders, play/settings/fullscreen, video element attached
- [x] /examples/captions.html — VAST preroll with VTT caption tracks; captions btn, track elements, play/pause cycle, settings CC submenu, volume slider, progress bar

## Player UI — Live
- [x] /examples/live.html — HLS live stream; play btn idle state, captions btn, settings panel + Speed, fullscreen, window.__core exposed
- [x] /examples/live-show-current-time.html — showLiveCurrentTime:true; current-time display, controls, window.__core exposed

## Player UI — Multi-plugin
- [x] /examples/multiplugin.html — chapters + chapterUi plugins + HLS; chapter banner injected, player structure, controls

## Player UI — Source management
- [x] /examples/source-fallback.html — broken first source triggers fallback; #status updates to "Fallback:", play/pause cycle, controls stay functional, window.__core
- [x] /examples/src-switch.html — dynamic source switching; btn-switch / btn-restore present and enabled, core.src updates on click and restores

## YouTube integration
- [x] /examples/youtube.html — YouTubeMediaEngine + AdsPlugin; iframe[src*=youtube] injected, correct video ID (dQw4w9WgXcQ), player wrapper + controls

## Spec files written (6 files, 126 tests)
- e2e/pages.spec.ts        — structural smoke test for all 10 pages (title, wrapper, controls, buttons)
- e2e/playback.spec.ts     — play/pause, center overlay, current time, settings panel navigation
- e2e/controls.spec.ts     — volume slider attrs, progress bar, fullscreen, settings (open/close/submenu), captions toggle
- e2e/ads.spec.ts          — ads.html + captions.html structure + track elements
- e2e/live.spec.ts         — live.html + live-show-current-time.html structure and control state
- e2e/source-management.spec.ts — fallback status text, src switch / restore, core.src values
- e2e/youtube.spec.ts      — YouTube iframe injection, video ID, controls
