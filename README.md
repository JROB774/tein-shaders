# The End is Nigh: Shaders

A number of custom shaders for the game **The End is Nigh**, developed by
**Edmund McMillen** and **Tyler Glaiel**. These shaders can be used by modders
to create unique looking worlds and levels, with a variety of effects.

A complete list of all the shaders with links to more info on their effects:

| Name                                    | File                              |
| --------------------------------------- | --------------------------------- |
| 8-Bit                                   | 8bit.shader                       |
| 8-Bit with Lighting                     | 8bit_lighting.shader              |
| Scrolling Camera                        | camerascroll.shader               |
| Chromatic Aberration                    | chromatic.shader                  |
| Chromatic Aberration with Pulse         | chromatic_pulse.shader            |
| Color Change with Pulse                 | colorpulse.shader                 |
| Glowing Lava                            | lavaglow.shader                   |
| Glowing Lava with Heatwave              | lavaglow_heatwave.shader          |
| Glowing Lava with Lighting              | lavaglow_lighting.shader          |
| Glowing Lava with Heatwave and Lighting | lavaglow_lighting_heatwave.shader |
| Pixelate                                | pixelate.shader                   |
| Pixelate with Pulse                     | pixelate_pulse.shader             |
| Red Alert                               | redalert.shader                   |
| Screenshake                             | screenshake.shader                |
| Static Pixelation                       | staticpixel.shader                |
| Static Pixelation with Pulse            | staticpixel_pulse.shader          |
| Vertical Flip                           | verticalflip.shader               |


## 8-Bit

## 8-Bit with Lighting

## Scrolling Camera

## Chromatic Aberration

## Chromatic Aberration with Pulse

## Color Change with Pulse

## Glowing Lava

## Glowing Lava with Heatwave

## Glowing Lava with Lighting

## Glowing Lava with Heatwave and Lighting

## Pixelate

## Pixelate with Pulse

## Red Alert

Performs a slight chromatic aberration effect whilst shaking the screen and
pulsing to the color red. This shader also applies the lighting effect.

**Variables:**
| Name                | Value                                      |
| ------------------- | ------------------------------------------ |
| shake_intensity     | The intensity of the screen shake.         |
| pulse_color         | The color to pulse to.                     |
| chromatic_intensity | The intensity of the chromatic aberration. |

**Tileset:**
```
fx_shader_mid redalert
midfx_graphics ShadeBox
midfx_layer 2
```

## Screenshake

## Static Pixelation

## Static Pixelation with Pulse

## Vertical Flip

Flips the entire screen upside down *(does not effect GUI elements)*.

**Tileset:**
```
fx_shader_mid verticalflip
midfx_graphics SolidBox
midfx_layer 2
```
