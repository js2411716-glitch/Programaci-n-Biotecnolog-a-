# Programacion Biotecnologia
Practicas de programación de primer semestre de biotecnología 

![bot](https://github.com/user-attachments/assets/b5589fac-d5f9-4540-b878-220909aff27e)

## LIBRERIAS NECESARIAS

 library(ggplot2)
 
 library(pheatmap)


## DATA FRAME PREEXISTENTE R

iris

##CODIGO
```
### REMOVER COLUMNAS DE UN DF

df=subset(iris, select = -c(Sepal.Length,Sepal.Width))
 View(df)
 head(df)

### SELECCIONAR SOLO ALGUNAS COLUMNAS DE UN DF

df=subset(iris, select = c(Sepal.Length,Sepal.Width))
 View(df)
 head(df)
 ggplot(iris, aes(x=Species, y=Sepal.Length)) +
 geom_col()
 a=ggplot(iris, aes(x=Species, y=Sepal.Length))
 a+geom_boxplot()
 a+geom_boxplot()
 a+labs(x= "especies de plantas", y= "largo del sepalo")
 a
 a2=a+geom_boxplot()
 a3=
 a3=a2+labs(x= "especies de plantas", y= "largo del sepalo")
 a3
 a3+ theme_gray()
 a3+ theme_dark()
 ggplot(iris, aes(x=Species, y=Sepal.Length, fill = Species)) 
 a4=ggplot(iris, aes(x=Species, y=Sepal.Length, fill = Species)) 
 a4
 a4+geom_boxplot()
 a4=ggplot(iris, aes(x=Species, y=Sepal.Length, fill = Species, alpha = 0.3)) 
 a4
 View(a4)
 View(a3)
 View(a4)
 a4=ggplot(iris, aes(x=Species, y=Sepal.Length, fill = Species, alpha =0.8)) 
 a4
 a4+geom_boxplot()
 a4+ geom_jitter()
 a5=a4+ geom_jitter()
 a6=a4+ geom_violin()
 a6
 a7=a4+geom_jitter(color="black", size=0.4, alpha=0.9)
 pheatmap(mtcars)
 str(mtcars)
 
#### CREATE HEATMAP
iris2 =subset(iris, select = -c(Species))
 iris2
 m6=as.matrix(iris2)
 heatmap(m6)

#####INSTALL TIDYVERSE

install.packages("tidyverse")
library(tidyverse)

