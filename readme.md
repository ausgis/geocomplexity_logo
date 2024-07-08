
``` r
library(showtext)
showtext_auto(enable = TRUE)
font_add("ShineTypewriter", regular = "./ShineTypewriter-lgwzd.ttf")
library(hexSticker)
library(magick)

sticker(
  subplot = "./geocomplexity_plot.png",
  s_x = .99,
  s_y = .98,
  s_width = .68,
  s_height = .68,
  package = "geocomplexity",
  p_family = "ShineTypewriter",
  p_size = 16.5,
  p_color = ggplot2::alpha("#3e3221",.65),
  p_x = 1.02,
  p_y = 1,
  dpi = 300,
  asp = 1,
  h_size = 1.25,
  h_color = ggplot2::alpha("#3e3221",.75),
  h_fill = ggplot2::alpha('#e1f1f1',.75),
  white_around_sticker = F,
  filename = "geocomplexity_logo.png"
)

image_read('./geocomplexity_logo.png') |> 
  image_resize("256x256")|> 
  image_write('./geocomplexity_logo.png')
```

![](./geocomplexity_logo.png)
