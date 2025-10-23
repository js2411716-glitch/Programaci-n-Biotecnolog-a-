# Programacion Biotecnologia
Practicas de programación de primer semestre de biotecnología 

![bot](https://github.com/user-attachments/assets/b5589fac-d5f9-4540-b878-220909aff27e)

## LIBRARYS 
<span style="color:#32a852;">library("nycflights13")</span><br>
<span style="color:#32a852;">library(tidyverse)</span><br>
<span style="color:#32a852;">library(dplyr)</span>




## CODIGO
```
 vuelos_sel <- select(flights, year, month, day, carrier, dep_delay, arr_delay)
 View(vuelos_sel)
 f=flights
 f
 vuelos_retrasados_mas_de_una_hora = vuelos_sel %>% filter(dep_delay==-1)
 vuelos_retrasados_mas_de_una_hora
 str(vuelos_retrasados_mas_de_una_hora)
 vuelos_sel
 diferencia= vuelos_sel%>% mutate(c= arr_delay-dep_delay)
 diferencia
 diferencia= vuelos_sel%>% mutate(retrasos= arr_delay-dep_delay)
 diferencia
 retrasados= filter(flights, dep_delay > 60)
 retrasado= arrange(retrasados, desc(dep_delay))
 head(retrasado)
 tail(retrasado)
 df_ordenado <- retrasado[order(-retrasado$arr_delay), ]
 df_ordenado
 flights= mutate(flights, duracion_horas = air_time /60)
 resumen = flights %>%
 group_by(carrier) %>%
 summarise(Promedio_duracion = mean(duracion_horas, na.rm = TRUE), Promedio_retraso = mean(dep_delay, na.rm = TRUE))
 print(resumen)
 aeroretraso <- resumen[order(-resumen$Promedio_retraso), ]
 aeroretraso
 colnames(flights) <- toupper(colnames(flights))
 head(flights)
 nombres= c("año", "mes", "dia", "hora de salida", "hora programada", "retraso de salida", "hora de llegada")
 colnames(flights) = nombres
 flights
 View(flights)
