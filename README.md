# Retro CRT Shader (for Universal RP)
A shader graph which replicates some retro tv/monitor effects.<br />

![Retro](retro.gif)

Most effects can be toggled on and off, uses shader_feature keywords to create multiple shader variants. Only used variants will be included in build. If you want to be able to toggle effects at runtime (using material.EnableKeyword), switch them to multi_compile keywords in the shadergraph blackboard instead.<br />
<br />
Effects include : <br />
• CRT (cathode-ray tube) monitor warping<br />
• Scanlines<br />
• Image Distortion<br />
• Static<br />
• Scrolling glitchy static<br />
• Vertical RGB subpixel / phosphor stripes (aperture grille?)<br />
<br />
Example also includes a multi-camera setup to render the scene to a low-resolution render texture, to achieve a pixelated look. The main camera's culling mask is set to nothing, so the scene isn't rendered twice, and it uses a different forward renderer which uses the Retro CRT Shader/material in an **Blit render feature** to apply it as an image effect, before additional post processing (**Vignette, Film Grain, Chromatic Aberration**). It could likely be applied to a regular mesh renderer too though, e.g. if you wanted to use it for a tv monitor.<br />
<br />
@Cyanilux<br />
:)
