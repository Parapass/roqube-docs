# FX Events

**Last updated: October 29, 2025**

- FX (also known as Color Correction) events are events you can use to change environment lighting during a song. There are multiple different properties you can use to control these effects.
- At the moment, these effects can ONLY be used on VR maps, so this will not work on a Mania map or map made in the osu! editor.
- All color correction values are based off the values in Roblox Studio. Mess around with a ColorCorrectionEffect inside a Studio baseplate if you want a clear visual of the effect you're creating.

Below is a sample event taken from Professional Vengeance:
```json
{
  "b" : 40.922,
  "t" : "_ColorCorrection",
  "d" : {
    "_ColorCorrection" : {
      "bn" : 0,
      "ct" : 5,
      "st" : -2,
      "tc" : {
        "r" : 255,
        "g" : 255,
        "b" : 255
      },
      "_d" : 0,
      "_ft" : 0.5,
      "_es" : "nil",
      "_ed" : "nil"
    }
  }
}
```

- B: Beat: Time in beats
- T: Type: Type of event, should always be "_ColorCorrection" for Color Correction events
- D: Data
  - "_ColorCorrection": { - **THIS IS REQUIRED!!! OTHERWISE YOUR EVENT WILL NOT WORK**
    - BN: Brightness
    - CT: Contrast
    - ST: Saturation
    - TC: Tint Color
      - R, G, B: Red, Green, and Blue. Recommended to just leave these at 255 unless otherwise needed
    - _D: Duration, useful for creating long effects that last more than 5 or so seconds
    - _FT: Fade Time, useful for creating short-burst effects or a slow fade-out on a long effect. Duration should not be used if creating a short-burst effect.
    - _ES: Ease In, leave as "nil" and it will default to Linear. Easing documentation available at https://easings.net/
    - _ED: Ease Out, leave as "nil" and it will default to Linear. Easing documentation available at https://easings.net/
