# The End is Nigh: Shaders

A number of custom shaders for the game **The End is Nigh**, developed by
**Edmund McMillen** and **Tyler Glaiel**. These shaders can be used by modders
to create unique looking worlds and levels, with a variety of different effects.

A complete list of all the shaders with links to more info on their effects:

| Name                                    | File                              | Description |
| :-------------------------------------- | :-------------------------------- | :---------- |
| 8-Bit                                   | 8bit.shader                       |             |
| 8-Bit with Lighting                     | 8bit_lighting.shader              |             |
| Scrolling Camera                        | camerascroll.shader               |             |
| Chromatic Aberration                    | chromatic.shader                  |             |
| Chromatic Aberration with Pulse         | chromatic_pulse.shader            |             |
| Color Change with Pulse                 | colorpulse.shader                 |             |
| Glowing Lava                            | lavaglow.shader                   |             |
| Glowing Lava with Heatwave              | lavaglow_heatwave.shader          |             |
| Glowing Lava with Lighting              | lavaglow_lighting.shader          |             |
| Glowing Lava with Heatwave and Lighting | lavaglow_lighting_heatwave.shader |             |
| Pixelate                                | pixelate.shader                   |             |
| Pixelate with Pulse                     | pixelate_pulse.shader             |             |
| Red Alert                               | redalert.shader                   |             |
| Screenshake                             | screenshake.shader                |             |
| Static Pixelation                       | staticpixel.shader                |             |
| Static Pixelation with Pulse            | staticpixel_pulse.shader          |             |
| Vertical Flip                           | verticalflip.shader               |             |


## 8-Bit

## 8-Bit with Lighting

## Scrolling Camera

## Chromatic Aberration

## Chromatic Aberration with Pulse

## Color Change with Pulse

Pulses between the current palette and a specific color.

**Variables:**
| Name                | Type  | Value                                         |
| :------------------ | :---- | :-------------------------------------------- |
| pulse_color         | vec4  | The color the shader should pulse towards.    |
| pulse_speed         | float | The speed at which the pulse will occur.      |
| max_color_intensity | float | How close the shader will get to pulse_color. |

**Tileset:**
```
fx_shader_mid colorpulse
midfx_graphics SolidBox
midfx_layer 2
```

## Glowing Lava

## Glowing Lava with Heatwave

## Glowing Lava with Lighting

## Glowing Lava with Heatwave and Lighting

## Pixelate

Pixelates the entire screen.

**Variables:**
| Name                | Type  | Value                                         |
| :------------------ | :---- | :-------------------------------------------- |
| pixel_density       | float | How much to pixelate the screen by.           |

**Tileset:**
```
fx_shader_mid pixelate
midfx_graphics SolidBox
midfx_layer 2
```

## Pixelate with Pulse

Pulses in and out of pixelating the entire screen.

**Variables:**
| Name                | Type  | Value                                         |
| :------------------ | :---- | :-------------------------------------------- |
| min_pixel_density   | float | The lower bound to pixelate by.               |
| max_pixel_density   | float | The upper bound to pixelate by.               |

**Tileset:**
```
fx_shader_mid pixelate_pulse
midfx_graphics SolidBox
midfx_layer 2
```

## Red Alert

Performs a slight chromatic aberration effect whilst shaking the screen and
pulsing to the color red (by default).

This shader also applies the lighting and glowing effects.

**Variables:**
| Name                | Type  | Value                                         |
| :------------------ | :---- | :-------------------------------------------- |
| light_color         | vec4  | Color of light above and on top of water.     |
| light_distance      | float | How far the glowing light will travel.        |
| glow_strength       | float | How strong the glow effect should be.         |
| pulse_color         | vec4  | The color the shader should pulse towards.    |
| pulse_speed         | float | The speed at which the pulse will occur.      |
| max_color_intensity | float | How close the shader will get to pulse_color. |
| chromatic_intensity | vec2  | The intensity of the chromatic aberration.    |
| shake_speed         | float | The speed at which to shake the screen.       |
| shake_intensity     | vec2  | The intensity of the screen shake.            |

**Tileset:**
```
fx_shader_mid redalert
midfx_graphics ShadeBox
midfx_layer 2
```

## Screenshake

Shakes the screen in random directions.

**Variables:**
| Name                | Type  | Value                                         |
| :------------------ | :---- | :-------------------------------------------- |
| speed               | float | The speed at which to shake the screen.       |
| intensity           | vec2  | The intensity of the screen shake.            |

**Tileset:**
```
fx_shader_mid screenshake
midfx_graphics SolidBox
midfx_layer 2
```

## Static Pixelation

Performs a slight chromatic aberration effect as well as a static effect whilst
pixelating the entire screen.

**Variables:**
| Name                | Type  | Value                                         |
| :------------------ | :---- | :-------------------------------------------- |
| pixel_density       | float | How much to pixelate the screen by.           |
| chromatic_intensity | vec2  | The intensity of the chromatic aberration.    |

**Tileset:**
```
fx_shader_mid staticpixel
midfx_graphics SolidBox
midfx_layer 2
```

## Static Pixelation with Pulse

Pulses in and out of performing a slight chromatic aberration effect as well as
a static effect whilst pixelating the entire screen.

**Variables:**
| Name                | Type  | Value                                         |
| :------------------ | :---- | :-------------------------------------------- |
| min_pixel_density   | float | The lower bound to pixelate by.               |
| max_pixel_density   | float | The upper bound to pixelate by.               |
| chromatic_intensity | vec2  | The intensity of the chromatic aberration.    |

**Tileset:**
```
fx_shader_mid staticpixel_pulse
midfx_graphics SolidBox
midfx_layer 2
```

## Vertical Flip

Flips the entire screen upside down (does not effect GUI elements).

**Tileset:**
```
fx_shader_mid verticalflip
midfx_graphics SolidBox
midfx_layer 2
```
