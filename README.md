# Lulu Dither Logo

An interactive canvas tool for generating dithered dot patterns from SVG artwork, with a wave grid animation mode and 3D model viewer.

Live: **[lulu-dither-logo.vercel.app](https://lulu-dither-logo.vercel.app)**

---

## Tabs

### Dither
Renders your SVG as a field of dots using Floyd-Steinberg or ordered dithering. Move your cursor over the canvas to push dots outward with a cubic falloff. Click to send a radial ripple through the dot field.

**Controls**
- **Algorithm** — Floyd-Steinberg, Ordered (Bayer 4×4), or Threshold
- **Scale** — dot density (higher = fewer, larger dots)
- **Repulsion Radius / Strength** — size and force of the cursor push
- **Return Speed** — how quickly dots spring back to their base positions
- **Dot Color / Background Color** — canvas palette
- **Dot Size / Shape** — radius and softness of each dot

**Animations**
- **Fall** — dots rain down from above into their final positions, with controls for curve, duration, stagger, and direction
- **Pop** — dots snap into view one by one in a staggered pattern

### Wave Grid
Same SVG-masked dot field, but each dot's opacity is driven by a travelling sine wave. The cursor repulsion and click ripple interactions carry over from Dither mode.

**Controls**
- Rows, Columns, Frequency, Phase Shift, Min/Max Opacity, Speed

### 3D
Loads a GLTF model (`model.gltf`) rendered with Three.js. Drag to rotate. Auto-rotates by default.

**Controls**
- Ambient Light, Key Light (intensity + color), Fill Light
- Exposure, Camera FOV, Background Color
- Scale, Roughness, Metalness
- Auto-Rotate + Rotate Speed

---

## SVG Upload
Click the **Image** field at the top of the controls panel to swap in any local SVG. The dot field regenerates immediately.

## Export
- **Export JSON** — downloads dot coordinates as a JSON array
- **Copy JS Code** — copies a JS snippet with the dot array to your clipboard
