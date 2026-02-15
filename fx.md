# Color Correction Documentation \ FX Events

- b = Beat (time)
- t = Type (Type of event) [_ColorCorrection]
- d = {} (Table including the events data)

## Color Correction default values
- Brightness = 0,
- Contrast = 0.175,
- Saturation = 1,
- TintColor = Color3.fromRGB(255, 255, 255)


# Properties
- d.Duration = Number (length in beats) [0 for a instant event] [0 to 1 (clamped)]
- d.Brightness = Number or Array [[BrightnessValue : Number, PercentageCompleted : Number, Easing : string]]
- d.Contrast   = Number or Array [[ContrastValue   : Number, PercentageCompleted : Number, Easing : string]]
- d.Saturation = Number or Array [[SaturationValue : Number, PercentageCompleted : Number, Easing : string]]
- d.TintColor  = Array [[R : Number, G : Number, B : Number, PercentageCompleted : Number, Easing : string]]

Note when editing properties:
- when using arrays, percentage completeted is start beat to end beat (b + Duration)
- You do not always need to include a property, if you plan to only change the Contrast property then only include Contrast
- To reset back to the default value, Ex: d.Brightness = "DV"
- For easings, Check the easing documentation

-- Example taken from Comment te dire --

 ```{
  "b" : 1.25,
  "t" : "_ColorCorrection",
  "d" : {
    "Duration" : 39.75, -- duration in beats
    "Saturation" : [
      [ -0.6, 0 ],
      [ "DV", 1, "easeInExpo" ]
    ],
    
    "Brightness" : "DV"
  }
},```

Documentation of the actual object can be found here: https://create.roblox.com/docs/reference/engine/classes/ColorCorrectionEffect
