---
title: Pacote {patchwork}
author: Marcelo Avila
date: '2021-02-27'
slug: [/R/]
categories: [R]
tags: [R, ggplot, gráficos, pacote]
---

O objetivo do `{patchwork}` é tornar ridiculamente simples combinar ggplots separados no mesmo gráfico. Como tal, ele tenta resolver o mesmo problema que `gridExtra::grid.arrange()` e `cowplot::plot_grid`, mas usando uma API que incita exploração e iteração e escala para layouts arbitrariamente complexos. 

## Instalação 

```r
install.packages("patchwork")

# alternativa: versão de desenvolvimento direto do github
# devtools::install_github("thomasp85/patchwork")
```
## Uso básico 


```r
library(ggplot2)
library(patchwork)

p1 <- ggplot(mtcars) + geom_point(aes(mpg, disp))
p2 <- ggplot(mtcars) + geom_boxplot(aes(gear, disp, group = gear))

p1 + p2
```

<img src="{{< blogdown/postref >}}index_files/figure-html/usage-1.png" width="672" />
Para mais detalhes e exemplos, visite o [site do pacote](https://patchwork.data-imaginist.com/).


## Referências 

- Thomas Lin Pedersen (2021). patchwork: The Composer of Plots. https://patchwork.data-imaginist.com, https://github.com/thomasp85/patchwork.
