# TEIN Shaders

A number of custom shaders for modding the game [The End is Nigh](https://store.steampowered.com/app/583470/The_End_Is_Nigh/),
by Edmund McMillen and [Tyler Glaiel](https://github.com/tylerglaiel).

## Shader List

* 8-Bit
* 8-Bit Lighting
* Camera Scroll (Experimental)
* Chromatic
* Chromatic Pulse
* Lava Glow Lighting Heatwave
* Lava Glow Lighting
* Lava Glow Heatwave
* Lava Glow
* Static Pixelate
* Static Pixelate Pulse
* Pixelate
* Pixelate Pulse
* Vertical Flip
* Color Pulse
* Screenshake
* Red Alert

## Shaders

### 8-Bit

`8bit.shader`

Limits the visible color range to create an 8-bit color palette effect.

For best results, copy this into the given tileset:

```
fx_shader_mid 8bit
midfx_graphics ShadeBox
midfx_layer 2
```

### 8-Bit Lighting

Limits the visible color range to create an 8-bit color palette effect. It also
provides the default lighting effect to further the effect of the color limit.

For best results, copy this into the given tileset:

```
fx_shader_mid 8bit_lighting
midfx_graphics ShadeBox
midfx_layer 2
```

### Camera Scroll (Experimental)

`camerascroll.shader`

Simulates a camera that follows the player, rather than having a fixed position.
An example in the folder `.examples/camerascroll` has been included to
showcase how the shader is setup and used.

**How to Use:**
* Place the shader in the `shaders` folder and rename it `colormapped.shader`.
* Create a new level and set the camera bounds to be the size you want your
  scrolling camera to be *(not the size of the play area like usual)*.
* Make sure the camera bounds are out of the way of the level, otherwise there
  will be ugly GUI elements stuck on the screen.
* Always place the camera bounds to the bottom right of the play area so that
  the player will not be killed for "being off-screen".
* Use the editor to create levels bigger than 54x32 if need be to ensure the
  above two camera bounds rules can be met.

**Known Issues:**
* GUI elements will not be visible when playing like this (tumor count, level
  name, etc.) due to the camera bounds being fixed off-screen.
* Most shaders are not compatible with the scrolling camera so it is best to
  avoid applying `fx_shader` and `fx_shader_mid` to `tilesets.txt`.
* The scrolling camera is global and cannot be turned off for specific levels
  or area; it will apply to the entire game.

### Chromatic

`chromatic.shader`

Applies a chromatic aberration effect (splits the red, green, and blue color
channels). The intensity of the effect can be changed by going into the shader's
code and modifying the `intensity` variable to a lower or higher value.

For best results, copy this into the given tileset:

```
fx_shader_mid chromatic
midfx_graphics SolidBox
midfx_layer 2
```

## Chromatic Pulse

`chromatic_pulse.shader`

Applies a chromatic aberration effect (splits the red, green, and blue color
channels). However, this version pulses in and out of the effect. The intensity
of the effect can be changed by going into the shader's code and modifying the
`intensity` variable to a lower or higher value.

For best results, copy this into the given tileset:

```
fx_shader_mid chromatic_pulse
midfx_graphics SolidBox
midfx_layer 2
```

### Lava Glow Lighting Heatwave

`lavaglow_lighting_heatwave.shader`

A more intense effect for lava, which makes it glow vibrantly, as well as making
certain elements near the lava glow. The shader also combines the pre-existing
`lighting` and `heatwave` shaders as well, to complete the effect. The intensity
of the lighting shader can be controlled using `shader_param`.

For best results, copy this into the given tileset (with a `shader_param`):

```
fx_shader lavaripples
fx_shader_mid lavaglow_lighting_heatwave
midfx_graphics ShadeBox
midfx_layer 2
```

## Lava Glow Lighting

`lavaglow_lighting.shader`

The same as the `lavaglow_lighting_heatwave` shader but without the heatwave.

For best results, copy this into the given tileset (with a shader_param):

```
fx_shader lavaripples
fx_shader_mid lavaglow_lighting
midfx_graphics ShadeBox
midfx_layer 2
```

### Lava Glow Heatwave

`lavaglow_heatwave.shader`

The same as the `lavaglow_lighting_heatwave` shader but without the lighting.

For best results, copy this into the given tileset:

```
fx_shader lavaripples
fx_shader_mid lavaglow_heatwave
midfx_graphics ShadeBox
midfx_layer 2
```

### Lava Glow

`lavaglow.shader`

The same as the `lavaglow_lighting_heatwave` shader but without the lighting
and heatwave effects.

For best results, copy this into the given tileset:

```
fx_shader lavaripples
fx_shader_mid lavaglow
midfx_graphics ShadeBox
midfx_layer 2
```

### Static Pixelate

`staticpixel.shader`

Pixelates the entire screen and applies both a static and chromatic aberration
effect as well. The pixel density on screen can be changed in the shader's code
via the `pixel_density` variable. The intensity of the chromatic aberration can
be changed via the `intensity` variable in the shader's code.

For best results, copy this into the given tileset:

```
fx_shader_mid staticpixel
midfx_graphics SolidBox
midfx_layer 2
```

### Static Pixelate Pulse

`staticpixel_pulse.shader`

Pixelates the entire screen and applies both a static and chromatic aberration
effect as well. However, this version pulses in and out of the effect. The min
and max pixel densities that are pulsed between can be changed in the shader's
code via the `min_pixel_density` and `max_pixel_density` variables. The
intensity of the chromatic aberration can be changed via the `intensity`
variable in the shader's code.

For best results, copy this into the given tileset:

```
fx_shader_mid staticpixel_pulse
midfx_graphics SolidBox
midfx_layer 2
```

### Pixelate

`pixelate.shader`

Pixelates the entire screen. The pixel density on screen can be changed in the
shader's code via the `pixel_density` variable.

For best results, copy this into the given tileset:

```
fx_shader_mid pixelate
midfx_graphics SolidBox
midfx_layer 2
```

### Pixelate Pulse

`pixelate_pulse.shader`

Pixelates the entire screen. However, this version pulses in and out of the
effect. The min and max pixel densities that are pulsed between can be changed
in the shader's code via the `min_pixel_density` and `max_pixel_density`
variables.

For best results, copy this into the given tileset:

```
fx_shader_mid pixelate_pulse
midfx_graphics SolidBox
midfx_layer 2
```

### Vertical Flip

`verticalflip.shader`

Flips the entire screen upside down *(does not effect GUI elements)*.

For best results, copy this into the given tileset:

```
fx_shader_mid verticalflip
midfx_graphics SolidBox
midfx_layer 2
```

### Color Pulse

`colorpulse.shader`

Pulses between the standard palette and a specific color. To change the color
that gets pulsed between, go into the shader's code and modify `pulse_color`.

For best results, copy this into the given tileset:

```
fx_shader_mid colorpulse
midfx_graphics SolidBox
midfx_layer 2
```

### Screenshake

`screenshake.shader`

Shakes the screen in random directions. To change the intensity of the shake
go into the shader's code and edit the `intensity` variable.

For best results, copy this into the given tileset:

```
fx_shader_mid screenshake
midfx_graphics SolidBox
midfx_layer 2
```

### Red Alert

`redalert.shader`

Shakes the screen in random directions, pulses to the color red, and performs
a slight chromatic aberration during the pulse. Simulating some form of danger/
red alert. To change the intensity of the shake go into the shader's code and
edit the `shake_intensity` variable. `pulse_color` changes the color that will
be pulsed to (instead of red), and `chromatic_intensity` controls the intensity
of the chromatic aberration.

Note this shader also applies the default lighting shader.

For best results, copy this into the given tileset (with a shader param):

```
fx_shader_mid redalert
midfx_graphics ShadeBox
midfx_layer 2
```
