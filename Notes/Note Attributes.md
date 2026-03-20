# Note Attributes

## Visual Elements

### HasOverlay
**Type:** `Boolean`

Whether the note skin will have an overlayed sprite (image), usually used to add solid white colors or pre-baked colors.

---

### HeadImage
**Type:** `string`

The image id used for the head of a hold note.

---

### ReceptorSkin / ReceptorImage
**Type:** `string` (both)

The image id used for the receptors main image.

---

### ReceptorColor
**Type:** `Color3`

The color used for the non-active state of a receptor (when no key is being pressed).

---

## Rendering & Display

### Is2D
**Type:** `Boolean`

Indicates whether a note is 2D or 3D. 3D notes are handled differently than 2D ones.

---

### Resample_Pixel
**Type:** `Boolean`

Whether the note is rendered using precise pixels or a smooth image. Mainly used for pixel art notes.

---

## Rotation

### IgnoreRotation
**Type:** `Boolean`

Whether the notes will visually ignore the rotation logic or not (left, right, up, down).

---

### ReceptorsIgnoreRotation
**Type:** `Boolean`

Whether the receptors visually ignore the rotation logic or not (left, right, up, down).

---
