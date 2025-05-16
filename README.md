# MaxPatchforNoiseProduction
Este código fue desarrollado para el documento de memoria "Análisis de música Noise: Comparación y evaluación de estrategias cuantitativas y cualitativas" para optar al título de Ingeniería en Sonido, mención en Diseño y Producción Sonora.
Este patch básico consta de 5 módulos, con 4 de ellos buscando acercarse a componentes sonoros de 2 de las obras analizadas durante el proceso de investigación. Estos son:

Módulo 1: Se utilizó un granulador estereofónico simple con distorsión para imitar uno de los componentes intermitentes presentes durante la mayoría de "Turning Point" de Kevin Drumm. Para el granulador se utilizó como audio el archivo "prim.loop" de la librería de audio de Max, considerando la naturaleza percusiva del elemento a imitar.

Módulo 2: Similar al primer módulo, se utilizó esta vez un metrónomo y una envolvente con distorsión para imitar el mismo elemento percusivo durante la obra de Kevin Drumm, a modo de ofrecer otra aproximación.

Módulo 3: El único módulo que no busca imitar sonidos, este consta de un conjunto de funciones combinadas, encontradas durante la creación de otros módulos. Su estructura principal consta de un audio buffer ("prim.loop"), el que es leído aleatoriamente partiendo de diferentes muestras y a diferentes intervalos. Su lectura es sujeta a una constante variación de su frecuencia de muestreo. Finalmente, se envía una copia de la señal resultante al objeto round~, que aproxima las muestras recibidas a valores múltiplos de 0.9, los que se multiplican con la señal original. A lo largo de su estructura, la gran mayoría de parámetros se encuentran sujetos a diferentes funciones de aleatoriedad constante.

Módulo 4: Se utilizó un granulador monofónico con distorsión, posteriormente filtrando la señal, para imitar otro de los componentes intermitentes durante "Turning Point" de Kevin Drumm. Para el granulador, se utilizó como audio de origen el archivo "cello-f2", a modo de obtener el efecto de distorsión deseado en frecuencias medias bajas, aparte de cierto componente armónico.

Módulo 5: Se utilizó una señal entrante de ruido blanco a la que se le aplicaron posteriores filtros, a modo de obtener uno de los últimos componentes de "Takemitsu" de Merzbow, presente desde el minuto 5:04 en la obra.
