# Unidad1
Introducción a la graficación por computadora.

## Contenido de la Unidad

### 1.1 Historia y evolución
### 1.2 Áreas de aplicación
### 1.3 Aspectos matemáticos de la graficación
### 1.4 Modelos del color: RGB, CMY, HSV y HSL
### 1.5 Representación y trazo de líneas y polígonos
### 1.6 Procesamiento de mapas de bits


### 1.1 Historia y evolución
La historia de la graficación por computadora es un relato de superación constante de las limitaciones físicas del hardware y la búsqueda de una representación visual más natural y eficiente. El campo surgió de la necesidad de enriquecer la presentación de la información generada por computadoras, que en sus inicios se limitaba a datos numéricos y textuales poco intuitivos.

Los inicios y la era experimental (1950-1960)
Durante la década de 1950, la graficación era una disciplina incipiente vinculada principalmente al control militar y la investigación académica. En 1950, Arthur Samuel desarrolló uno de los primeros programas capaces de aprender a jugar damas, lo que planteó la necesidad de visualizar estados lógicos en tableros virtuales.
Paralelamente, Ben Laposky realizó experimentos pioneros utilizando osciloscopios para generar imágenes electrónicas, lo que se considera un precursor directo del arte digital actual.
Un momento definitorio ocurrió en 1963 con la tesis doctoral de Ivan Sutherland en el MIT, quien presentó el sistema Sketchpad. Este software introdujo el concepto de interacción directa mediante un lápiz óptico, permitiendo al usuario dibujar líneas y construir polígonos sobre una pantalla. Sketchpad no solo fue el precursor de los sistemas modernos de Diseño Asistido por Computadora (CAD), sino que también estableció las bases para el uso de estructuras de datos jerárquicas y símbolos replicables en la representación de objetos gráficos.
La maduración técnica y comercial (1970-1980)
La década de 1970 fue testigo de la expansión de la graficación hacia el ámbito comercial y el entretenimiento. En 1973, Xerox PARC desarrolló el sistema Alto, que introdujo la primera interfaz de usuario gráfica (GUI) funcional y el uso del mouse, además de ser pionero en la gestión de gráficos en color. Durante este periodo, la Universidad de Utah se convirtió en el centro neurálgico de la investigación en renderizado, donde figuras como Ed Catmull y Fred Parke produjeron animaciones faciales realistas para películas como Futureworld (1976).
El desarrollo de algoritmos de sombreado también marcó hitos significativos. En 1971, Henri Gouraud inventó la técnica de sombreado que lleva su nombre, permitiendo que superficies poligonales se vieran suaves mediante la interpolación de colores en sus vértices.6 Poco después, Bui Tuong Phong perfeccionó este enfoque al introducir un modelo de reflexión que incluía brillos especulares, mejorando drásticamente el realismo de los materiales sintéticos.
La democratización y el surgimiento de la GPU (1980-2000)
En 1980, Apple lanzó el Apple II con capacidades gráficas avanzadas para el mercado personal, mientras que Autodesk presentaba en 1982 AutoCAD, transformando para siempre la arquitectura y la ingeniería. La fundación de Silicon Graphics en 1985 permitió a los profesionales acceder a estaciones de trabajo dedicadas que podían procesar gráficos 3D complejos en tiempo real.
Sin embargo, la transformación más profunda llegó a finales de los 90 con el nacimiento de la GPU (Unidad de Procesamiento Gráfico). En el año 2000, NVIDIA lanzó la primera GPU moderna, descargando el intenso trabajo de cálculo matemático de la CPU y permitiendo una aceleración sin precedentes en la renderización de polígonos. Este avance permitió que el CGI cinematográfico alcanzara niveles de fotorrealismo sorprendentes, ejemplificados por el software RenderMan de Pixar.
El presente y futuro de la graficación (2010-Actualidad)
Desde 2010, el enfoque se ha desplazado hacia la Realidad Virtual (VR) y la Realidad Aumentada (AR), exigiendo latencias extremadamente bajas y altas resoluciones para evitar la desorientación del usuario.3 La computación gráfica actual no solo se ocupa de polígonos masivos, sino de técnicas sofisticadas de texturizado, mapeado y trazado de rayos (Ray Tracing) en tiempo real, lo que ha llevado la calidad visual de los videojuegos y simuladores a niveles casi indistinguibles de la realidad.



## 1.2 Áreas de aplicación
- Ingeniería y arquitectura
- Medicina
- Entretenimiento
- Educación
- Ciencia y gestión
- Arte digital

### 1.3 Aspectos matemáticos
- Vectores
- Producto punto
- Matrices de transformación
- Coordenadas homogéneas

### 1.4 Modelos de color
- RGB
- CMY / CMYK
- HSV
- HSL

### 1.5 Representación de líneas y polígonos
- Algoritmo DDA
- Algoritmo de Bresenham

### 1.5.1 Formatos de imagen
Los formatos de imagen digital se dividen en dos categorías principales: mapas de bits (ráster) y vectores.

| Formato | Tipo      | Compresión    | Uso Recomendado                                                     |
|---------|-----------|--------------|---------------------------------------------------------------------|
| JPEG    | Ráster    | Con pérdida  | Fotografías web; equilibrio entre peso y detalle.                   |
| PNG     | Ráster    | Sin pérdida  | Imágenes con transparencia (canal alfa); alta fidelidad.            |
| GIF     | Ráster    | Sin pérdida  | Animaciones cortas; paleta limitada a 256 colores.                  |
| TIFF    | Ráster    | Variable     | Impresión profesional; soporta capas y alta profundidad de bits.    |
| SVG     | Vectorial | N/A          | Logotipos e iconos; escalable sin pérdida de calidad.               |


##Práctica de dibujo: Un polígono y la Flor de la Vida
Para comprender la geometría en la graficación, es esencial practicar la construcción manual de formas complejas.

###Construcción de un Pentágono Regular (Inscrito):
Paso 1: Limpiar y preparar la escena
•	Antes de dibujar, debemos asegurarnos de que el espacio esté vacío.
•	En Blender, esto se hace seleccionando todo con la tecla A y borrando con la tecla X.

Paso 2: Crear la estructura del Polígono
•	En lugar de dibujar línea por línea, usamos una "primitiva" de círculo como base.
•	Presiona Shift + A, ve a Mesh (Malla) y selecciona Circle (Círculo).
•	El "truco" del código: En cuanto aparece el círculo, verás una pequeña ventana abajo a la izquierda llamada "Add Circle". Allí, cambia el número de Vertices de 32 a 5.
•	Al decirle a Blender que solo use 5 puntos, el "círculo" se convierte automáticamente en un pentágono perfecto.

Paso 3: Ubicación exacta (Coordenadas)
Las coordenadas, el polígono se crea inicialmente en el centro exacto: X=0, Y=0, Z=0.

###Construcción de la Flor de la Vida:
Esta práctica utiliza coordenadas polares para posicionar círculos de forma perfecta alrededor de un centro.
1.	Paso 1: Preparación del Entorno
•	Abrir la Consola de Python: En Blender, cambia una de tus ventanas al editor de texto (Text Editor) para escribir el código.
•	Importar Librerías: Debes escribir import bpy (para que Python controle Blender) e import math (para hacer los cálculos de los ángulos).
•	Limpiar la Escena: Antes de empezar, el código debe borrar cualquier objeto existente para que no se amontonen.

3.	Paso 2: Definir las Reglas (Variables)
•	Debes establecer tres datos importantes en tu código:
•	Radio: El tamaño que tendrán todos tus círculos (por ejemplo, valor de 3).
•	Ángulo Inicial: Empezamos en 0 grados.
•	Paso Angular: Como queremos 6 círculos alrededor, dividimos 360° entre 6, lo que nos da 60° para cada paso.

4.	Paso 3: Crear el Círculo Base
•	El primer paso es dibujar un círculo justo en el centro de la pantalla, en las coordenadas (0, 0, 0).

5.	Paso 4: El Patrón Repetitivo (Los Círculos Periféricos)
•	Para que la flor sea perfecta, los centros de los demás círculos deben estar sobre el borde del primer círculo. La lógica es la siguiente:
•	Calcular la ubicación: Usamos matemáticas para convertir el ángulo en una posición derecha/izquierda (X) y arriba/abajo (Y) usando las fórmulas:
•	Colocar el círculo: Se le pide a Blender crear un nuevo círculo en esa posición calculada.
•	Girar el ángulo: Sumamos 60° al ángulo actual para prepararnos para el siguiente círculo.

6.	Paso 5: El Reto del Ciclo (Automatización)
•	Para no escribir el código muchas veces, se utiliza una estructura llamada while. El programa repetirá automáticamente los cálculos y la creación de círculos mientras el ángulo sea menor a 360°.
•	Esto asegura que los círculos se distribuyan uniformemente hasta completar la figura circular que ves en las imágenes de tu práctica.

•	Resultado Final: Al ejecutar este proceso, obtendrás una figura simétrica donde cada círculo se intersecta con el centro del anterior, formando el patrón armonioso de la Flor de la Vida.



### 1.6 Procesamiento de mapas de bits
El procesamiento de mapas de bits implica la manipulación de imágenes compuestas por una rejilla de píxeles.28 A diferencia de los vectores, estas imágenes pierden calidad al ser ampliadas, un fenómeno conocido como pixelación.
Resolución y Profundidad de Color
●	Resolución: Se refiere a la cantidad de píxeles por unidad de superficie (PPI o DPI). A mayor cantidad de píxeles, mayor detalle y nitidez.
●	Profundidad de Bits: Determina cuántos colores puede mostrar cada píxel. Un sistema de 1 bit es blanco y negro; 8 bits permiten 256 colores (color indexado); y 24 bits permiten 16.7 millones de colores (color verdadero).
●	Cuantización: Es el proceso de reducir el rango continuo de colores de una imagen a un conjunto discreto de valores. Si la cuantización es demasiado baja, aparecen "bandas de color" en los gradientes.
Operaciones Comunes en Mapas de Bits
Las herramientas modernas permiten realizar el remuestreo (resampling) para cambiar el tamaño de una imagen. El remuestreo a una resolución más baja elimina datos (submuestreo), mientras que aumentarla requiere interpolación, lo que puede difuminar la imagen.44 Además, la conversión de mapas de bits a vectores se conoce como vectorización (o autotrace), un proceso complejo que intenta encontrar fórmulas matemáticas que describan los bordes de los píxeles.


## Bibliografias
1.	1.1 Historia y Evolución de La Graficación Por Computadora | PDF | Pixar - Scribd, fecha de acceso: febrero 22, 2026, https://es.scribd.com/document/595159397/1-1-Historia-y-Evolucion-de-la-Graficacion-por-Computadora
3.	Marco Teórico - URBE, fecha de acceso: febrero 22, 2026, https://virtual.urbe.edu/tesispub/0054432/cap02.pdf
4.	Introducción a la graficación por computadora - Proyecto Descartes, fecha de acceso: febrero 22, 2026, https://proyectodescartes.org/iCartesiLibri/materiales_didacticos/GraficacionComputadora/index.html
5.	Aplicaciones Gráficas por Computadora - YouTube, fecha de acceso: febrero 22, 2026, https://www.youtube.com/watch?v=R1vI4VCKSEs
6.	Historia y la evolución de la graficación por computadora - Línea del tiempo - Prezi, fecha de acceso: febrero 22, 2026, https://prezi.com/p/t0p1yf8q2jof/historia-y-la-evolucion-de-la-graficacion-por-computadora-linea-del-tiempo/
7.	Computación gráfica - Wikipedia, la enciclopedia libre, fecha de acceso: febrero 22, 2026, https://es.wikipedia.org/wiki/Computaci%C3%B3n_gr%C3%A1fica
8.	La Fascinante Historia y Evolución de las Tarjetas Gráficas (GPU) - YouTube, fecha de acceso: febrero 22, 2026, https://www.youtube.com/watch?v=d2K1thETBx8
9.	Aplicaciones de las gráficas por computadora - UAEH, fecha de acceso: febrero 22, 2026, https://www.uaeh.edu.mx/docencia/P_Presentaciones/icbi/asignatura/aplicaciones_graf_comp_carmen_vera_marzo2014.pdf
10.	graficación por computadora en el software médico. - BINASSS, fecha de acceso: febrero 22, 2026, https://www.binasss.sa.cr/revistas/rcafss/v13n2/art6.pdf
11.	Gráficos de computadora - Ciencia y tecnología - SciTechnol, fecha de acceso: febrero 22, 2026, https://spanish.scitechnol.com/scholarly/computer-graphics-journals-articles-ppts-list.php
12.	Matrices y transformaciones lineales, fecha de acceso: febrero 22, 2026, https://www.matem.unam.mx/~max/GEA2/N5.pdf
13.	UAM1114.pdf, fecha de acceso: febrero 22, 2026, http://148.206.53.231/tesiuami/UAM1114.pdf
14.	Vector (matemáticas y física) - Wikipedia, la enciclopedia libre, fecha de acceso: febrero 22, 2026, https://es.wikipedia.org/wiki/Vector_(matem%C3%A1ticas_y_f%C3%ADsica)
15.	Vectores y notación (artículo) - Khan Academy, fecha de acceso: febrero 22, 2026, https://es.khanacademy.org/a/vectors-and-notation-mvc
16.	Matemáticas para Gráficos 3D con OpenGL - Código en Llamas, fecha de acceso: febrero 22, 2026, https://codigoenllamas.com/matematicas-para-graficos-3d-con-opengl
17.	Transformaciones en la graficación por computadora. Año 1. Número 1, fecha de acceso: febrero 22, 2026, https://www.aliatuniversidades.com.mx/conexxion/blog/conexxion/index.php/transformaciones-en-la-graficacion-por-computadora-ano-1-numero-1
18.	Modelos de Color RGB, CMY, HSV y HSL - Tema 1.4 | PDF - Scribd, fecha de acceso: febrero 22, 2026, https://es.scribd.com/document/599213324/Modelos-de-color-RGB-CMY-HSV-y-HSL-Tema-1-4
19.	Tema 1: INTRODUCCIÓN A LAS IMÁGENES DIGITALES, fecha de acceso: febrero 22, 2026, https://asignatura.us.es/imagendigital/Tema1.pdf
20.	Colorimetría III: La Objetividad del Color en RGB, HSV y HSL. - Artesolar, fecha de acceso: febrero 22, 2026, https://www.artesolar.com/colorimetria-espacios-rgb-hsv-hsl/


