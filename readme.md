
``` r
library(showtext)
showtext_auto(enable = TRUE)
font_add("ShineTypewriter", regular = "./ShineTypewriter-lgwzd.ttf")
library(hexSticker)
library(magick)

sticker(
  subplot = "./complexity.png",
  s_x = 0.985,
  s_y = 0.995,
  s_width = .8,
  s_height = .8,
  package = "geocomplexity",
  p_family = "ShineTypewriter",
  p_size = 10,
  p_color = ggplot2::alpha("#8297a0",.85),#ggplot2::alpha("#3e3221",.75),
  p_x = 1.01,
  p_y = 1.05,
  dpi = 300,
  asp = 1,
  h_size = 1.75,
  h_color = ggplot2::alpha("#8297a0",.85),
  h_fill = ggplot2::alpha('#f0f9fe',0.75),
  white_around_sticker = F,
  filename = "geocomplexity_logo.png"
)

image_read('./geocomplexity_logo.png') |> 
  image_resize("256x256")|> 
  image_write('./geocomplexity_logo.png')
```

![](./geocomplexity_logo.png)
