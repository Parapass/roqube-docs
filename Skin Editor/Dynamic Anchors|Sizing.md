# Dynamic Anchors

Anchors can be used to keep an object origin where specified, though you may also set an object's Root Anchor to Dynamic Anchors. Below are dynamic anchors and their purposes.

---

## How to Set a Dynamic Anchor in a UIElement

To set a Dynamic Anchor, select the UIElement you want to set it for then go to **Edit Properties -> Dynamic Anchor -> then type any [Dynamic Anchor](#dynamic-anchor-types)**

---

## Dynamic Anchor Types (Ro!Qube Mania - 4K)

### NIndex0 (Left note)
Anchors a note to the left note lane. Most commonly used with the left column position.

**Example:** `NIndex0;X,Y;0.5,0.5` - Centers the note on the left note's center point

---

### NIndex1 (Down note)
Anchors a note to the down note lane. Most commonly used with the down column position.

**Example:** `NIndex1;X;1,0` - Anchors to the right edge of the down note's X axis

---

### NIndex2 (Up note)
Anchors a note to the up note lane. Most commonly used with the up column position.

**Example:** `NIndex2;Y;0,1` - Anchors to the bottom of the up note's Y axis

---

### NIndex3 (Right note)
Anchors a note to the right note lane. Most commonly used with the right column position.

**Example:** `NIndex3;X,Y;1,1` - Anchors to the bottom right corner of the right note

## Slightly advanced anchoring

### Syntax Breakdown for example **`NIndex0;X,Y;0.5,0.5`**
**NIndex0** - The dynamic anchor point to attach to (which note lane you're anchoring to)

**;** - Separator

**X,Y** - The axes to anchor on
- `X,Y` - Anchors to both X and Y axes (default)
- `X` - Only anchors horizontally
- `Y` - Only anchors vertically
- (blank) - Defaults to X,Y

**;** - Separator

**0.5,0.5** - The anchor point offset within the dynamic anchor (IAnchor)
- `0,0` - Top left corner of the dynamic anchor
- `1,0` - Top right corner
- `0,1` - Bottom left corner
- `1,1` - Bottom right corner
- `0.5,0.5` - Center of anchor (Default anchor when IAnchor is blank)
  
---

### To position a UIElement in between two [Dynamic Anchors](#dynamic-anchor-types)

To position a UIElement in between two [Dynamic Anchors](#dynamic-anchor-types), you must use two ``or more`` [Dynamic Anchors](#dynamic-anchor-types) seperated by '|'

**Example:** `NIndex0;X,Y;0.5,0.5|NIndex3;X,Y;0.5,0.5` - The UI will be anchored in between the Left and Right receptor

 ---
 
# Dynamic Sizing (Image UIElement **only**)

Dynamic sizing can be used to size an object in between two [Dynamic Anchors](#dynamic-anchor-types)

---

**Example:** `NIndex0;X;0.5,0.5|NIndex3;X;0.5,0.5` - The UI will be sized in between the Left and Right receptor on the X axis

**Note:** Size is normalized so it can never be negative
