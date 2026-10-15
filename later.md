# Later: before the next push

Work in progress is verified on the **web breakpoint only (1440 wide)**. Before each push, run the checks below in one pass.

## Done in the 2026-10-15 pre-push pass
- [x] Every section checked at 390, plus the hero at 768 and 1024: no horizontal scroll, nothing clipped.
- [x] Hero: the "Drag to spin" arrow now starts at the tipping corner at every width; the caption's `right:-30px` balance only applies from 1280px up (it touched the edge at 1024).
- [x] Solution scene: early entry, float, pills (mobile pills lifted clear of the scroll nudge), nudge and fly-out on mobile.
- [x] Pipeline: below 900px the Lead Score cards stack under the phone instead of covering it.
- [x] Communication: below 900px the phone comes first, then the channel cards.
- [x] About, Challenge, Earnings, Design system, AI layer (static on mobile), Results, Next steps, footer: fine at 390.
- [x] `prefers-reduced-motion`: every new animation (hero entrance, hint, scroll nudge, Shipped pulse, canvas fades) has a fallback (checked in code).
- [x] 3D model shrunk with `KHR_mesh_quantization` (16-bit positions/UVs/indices, 8-bit normals, no tangents) and a JPEG normal map: geometry 3.0 MB → 1.2 MB (1.67 MB → 661 KB gzipped), textures 412 KB → 160 KB. The loader dequantizes attributes before splitting off the screen. Originals kept locally in `_scratch/iphone14-orig/` (gitignored).

## Next time
- [x] 03 · The UX work: checked at 390 (board first, one column, no horizontal scroll) before the push on 2026-10-15.
- [ ] The UX work at 768.
- [ ] Design system: the two new rows (AI patterns; controls and tokens) at 390 / 768.
- [ ] Re-check any section changed since this pass at 390 / 768 / 1024.
- [ ] Optional further shrink: meshopt compression (gltfpack) would roughly halve the geometry again, but needs the meshopt decoder in the import map.
- [ ] On low-end phones, consider a lower pixel ratio for the two canvases if the hero or solution scene stutters.
